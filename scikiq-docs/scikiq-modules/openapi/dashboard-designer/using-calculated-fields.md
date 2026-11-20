---
icon: laptop-binary
---

# Using Calculated Fields

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview

This page describes how to use calculated fields in SCIKIQ. A **Calculated Field** is a new field created by applying a formula or expression to existing fields in a dataset or table. It enables users to derive new values from existing data for analysis, reporting, and dashboard visualization.

Calculated fields help dashboard designers transform raw data into meaningful business metrics, create customized calculations, and display information that may not be directly available in the source dataset.

***

### Using Calculated Fields

This section explains how to use calculated fields, covering key concepts and function categories available in SCIKIQ. The concepts include **Arguments, Data Types, Blanks, and Syntax**. The function categories include **Aggregation and Statistics, Math, Logical and Comparison, Text, Date and Time, Time Intelligence, Filter and Context, Information and Type Conversion, and Parameter Tables**.

Practical examples demonstrate how to apply calculated fields through scenarios such as **data grouping, gross margin calculation, share of total, filtered measures, date calculations, KPI creation,** and **parameter tables.**

The section also covers dashboard best practices and performance considerations.

{% tabs %}
{% tab title="Functions" %}
**Overview**

SCIKIQ provides different categories of functions to help performing various operations when creating calculated fields. Each category contains functions designed for a specific purpose, such as mathematical calculations, text manipulation, date and time operations, data aggregation, logical evaluations, and data type conversions.

Expand a category to view its available functions. Each function includes its syntax, arguments, return type, description, and examples to help users understand how to use it in calculated-field expressions.

> <mark style="color:red;">**Note:**</mark> To count the number of unique values in a field, select **Distinct Count** as the aggregation option in the Measure well instead of creating a calculated field.

**List of Functions**

<details>

<summary><strong>Arguments</strong></summary>

**Overview**

An **argument** is a value, field, or expression passed to a function to perform a specific operation. In simple terms, arguments provide the information that a function needs to calculate or return a result.

**Argument Types and Description**

| **Argument**  | **What to pass**                                                       | **Example**                      |
| ------------- | ---------------------------------------------------------------------- | -------------------------------- |
| **number**    | A number column, a numeric field, or a number.                         | `COL('project_revenue')`, `0.05` |
| **text**      | A text column, a text field, or text in quotes.                        | `COL('region_name')`, `'North'`  |
| **date**      | A date column, or a date built with `CREATE_DATE`. Not text in quotes. | `COL('order_date')`              |
| **datetime**  | A date-time column, one that holds hours and minutes.                  | `COL('created_at')`              |
| **condition** | Anything that is true or false.                                        | `project_revenue > 0`            |
| **value**     | One value of the same type as the column it is compared with.          | `'North'`, `100000`              |
| **list**      | Values in square brackets, all of one type.                            | `['North', 'South']`             |
| **measure**   | An aggregate formula.                                                  | `SUM(COL('project_revenue'))`    |
| **column**    | A column reference.                                                    | `COL('region_name')`             |

</details>

<details>

<summary><strong>Data Types</strong></summary>

The **Data Types** define the kind of values a field can store or process, such as text, numbers, dates, and Boolean values. They determine how SCIKIQ interprets data and which operations and functions can be applied to a field.

In dashboard designing, data types help users select appropriate fields for calculations, filtering, grouping, and visualisations. Using compatible data types also helps ensure accurate calculations and reliable dashboard results.

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> SCIKIQ strictly enforces data types and does not automatically convert values between types. A column retains the data type defined in the source dataset. For example, an account code stored as text remains a text value, even if all its values appear numeric.
>
> If the data types are incompatible, the entire calculated field fails rather than processing only the rows with compatible values.
>
> SCIKIQ supports specific data type conversions through the `TO_INT`, `CONVERT_TO_DATE`, and `CONCATENATE` functions.
>
> * **TO\_INT:** Converts a value to an integer. Decimal places are discarded. If the input cannot be interpreted as a number, the function returns a blank.
> * **CONVERT\_TO\_DATE:** Converts text in the `YYYY-MM-DD` format into a date value. If the input does not follow the specified format, the function returns a blank.
> * **CONCATENATE:** Joins two or more values into a single text value. Numeric values are automatically converted to text during concatenation.

**Mixing Types**

| **You write**                                                                 | **What happens**                                                                             | **Write this instead**                                             |
| ----------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------ |
| SUM(COL('region\_name')) , or AVG on any text column                          | <p>Fails: text</p><p>cannot be summed or averaged</p>                                        | COUNT, MIN and MAX do work on text                                 |
| SUM(COL('qty\_text')) where the text holds numbers such as '12'               | <p>Fails: it is still</p><p>Text</p>                                                         | SUM(TO\_INT(COL('qty\_text')))                                     |
| <p>TO_FLOAT(COL('amount_text'))</p><p>where one value is '1,200' or 'n/a'</p> | <p>Fails for the</p><p>whole column</p>                                                      | <p>TO_FLOAT(SEARCH_REPLACE(COL('amount_text'),</p><p>',', ''))</p> |
| COL('qty\_text') == 12                                                        | <p>Fails: text</p><p>compared with a number</p>                                              | COL('qty\_text') == '12'                                           |
| <p>project_revenue +</p><p>COL('qty_text')</p>                                | Fails: arithmetic on text                                                                    | Convert the text with TO\_INT or TO\_FLOAT first                   |
| <p>UPPER , LEFT , LEN or</p><p>SEARCH_REPLACE on a number column</p>          | Fails: text functions need text                                                              | <p>LEFT(CONVERT_TO_STRING(COL('postal_code')),</p><p>2)</p>        |
| YEAR(COL('date\_text')) on a date stored as text                              | Fails: date functions need a date                                                            | YEAR(CONVERT\_TO\_DATE(COL('date\_text')))                         |
| <p>COL('order_date') > '2026-01-</p><p>01'</p>                                | <p>Fails: a date</p><p>compared with text</p>                                                | <p>COL('order_date') > CREATE_DATE(2026, 1,</p><p>1)</p>           |
| IN(COL('units'), \['3', '5']) on a number column                              | <p>Fails: the list</p><p>type must match the column</p>                                      | IN(COL('units'), \[3, 5])                                          |
| You write                                                                     | What happens                                                                                 | Write this instead                                                 |
| COL('region\_name') == 'north'                                                | <p>Runs, but is</p><p>FALSE for</p><p>'North': text</p><p>comparisons are case sensitive</p> | UPPER(COL('region\_name')) == 'NORTH'                              |

</details>

<details>

<summary><strong>Blanks</strong></summary>

A **Blank** is a value that represents missing or unavailable data in a field or expression. It indicates that no actual value is available for that particular record.

In simple terms, a blank means that a field does not contain a usable value for a particular record.

**Function Behaviour and Examples**

| **Where the blank meets**              | **Result**                | **Example**                                           |
| -------------------------------------- | ------------------------- | ----------------------------------------------------- |
| Arithmetic: + - \* /                   | Blank                     | 80,000 minus a blank cost is blank                    |
| <p>SUM, AVG, MIN, MAX,</p><p>COUNT</p> | The blank is skipped      | AVG of 1,200, 300 and a blank is 750                  |
| COUNTROWS                              | Counted: every row counts | 3 rows give 3                                         |
| A comparison: == , > , EQ              | Blank                     |                                                       |
| IF with a blank condition              | The _else_ result         | IF(project\_revenue > 500, 'High', 'Low') gives 'Low' |
| AND, OR, NOT                           | Blank                     |                                                       |
| Text functions: UPPER, TRIM, LEFT      | Blank                     |                                                       |
| CONCATENATE                            | Treated as empty text     | <p>CONCATENATE('C', '-', blank) gives</p><p>'C-'</p>  |
| DIVIDE by 0                            | Blank                     | The / operator gives infinity instead                 |

</details>

<details>

<summary><strong>Syntax</strong></summary>

**Overview**

**Syntax** refers to the rules and structure used to write valid expressions in an expression language. It defines how functions, arguments, operators, and values must be arranged to perform calculations correctly.

In simple terms, syntax tells users how to write an expression so that SCIKIQ can understand and execute it.

**Referring to Fields**

| **To refer to**                         | **Write**                                           | **Example**           |
| --------------------------------------- | --------------------------------------------------- | --------------------- |
| <p>A column with a plain</p><p>name</p> | Its name, or COL('name')                            | project\_revenue      |
| A column with spaces or symbols         | COL('name')                                         | COL('Unit Price')     |
| Another calculated field                | Its name                                            | total\_revenue        |
| A parameter table column                | <p>Table['column'] or</p><p>COL('Table.column')</p> | kpi\_selector\['kpi'] |

> <mark style="color:red;">**Note:**</mark> A field can reference other fields, and SCIKIQ automatically determines the order in which they are evaluated. However, circular references are not allowed. If a field references itself, either directly or indirectly through other fields, SCIKIQ rejects the expression.

**Operators**

| **Kind**   | **Operators**                                         | **Example**                                    |
| ---------- | ----------------------------------------------------- | ---------------------------------------------- |
| Arithmetic | + - \* / , // floor division, % remainder, \*\* power | project\_revenue - project\_cost               |
| Comparison | == != > < >= <=                                       | project\_revenue >= 100000                     |
| Membership | in \[...] , not in \[...]                             | COL('region\_name') in \['North', 'South']     |
| Logic      | and , or , not                                        | (project\_revenue > 0) and (project\_cost > 0) |

**Literals**

Text goes in single or double quotes. Numbers are plain: 100000 , 0.05 . Lists use square brackets. True and false are TRUE() and FALSE() . Dates are built with CREATE\_DATE(2026, 4, 1) .

**VAR and RETURN**

A long formula can name its steps. Each VAR starts its own line, a later step can use an earlier one, and RETURN gives the answer.

VAR revenue = SUM(COL('project\_revenue'))

VAR cost = SUM

RETURN DIVIDE(revenue - cost, revenue)

**Important Rules and Considerations**

* Function names are written in capitals, exactly as listed here.
* Membership uses lowercase in and square brackets. IN {'a', 'b'} with braces does not parse.
* 0 < x < 1 is refused. Write (x > 0) and (x < 1) .
* Put brackets around each comparison joined by AND or OR.

</details>

<details>

<summary><strong>Aggregation and Statistics</strong></summary>

**Overview**

**Aggregation and Statistics** functions summarise and analyse data by calculating totals, averages, counts, minimums, maximums, variance, and standard deviation.

In dashboard designing, these functions help derive meaningful business metrics and insights from detailed datasets. The results can be displayed in KPI cards, charts, and tables to monitor performance, compare results, and identify trends.

**List of Aggregate  Functions**&#x20;

The below listed functions are all aggregate functions that reduce a group of rows to a single value. Therefore, a calculated field that uses an aggregate function is treated as a measure.

Blank values are ignored during aggregation, except by COUNTROWS, which counts rows regardless of whether their values are blank.

| **Function**                                | **Returns**       | **Use**                                                                 |
| ------------------------------------------- | ----------------- | ----------------------------------------------------------------------- |
| SUM(number)                                 | Number            | Total                                                                   |
| <p>AVG(number) or</p><p>AVERAGE(number)</p> | Number            | Mean of the non-blank values                                            |
| MEDIAN(number)                              | Number            | Middle value; not pulled by a few very large values                     |
| MIN(value) , MAX(value)                     | Type of the input | Smallest or largest: numbers, dates (earliest, latest) or text (A to Z) |
| COUNT(column)                               | Number            | Number of non-blank values                                              |
| COUNTROWS()                                 | Number            | Number of rows, blank or not                                            |
| FIRST(value)                                | Type of the input | First value in the group, such as a manager's name                      |
| AVEDEV(number)                              | Number            | Average distance from the mean: how spread out the values are           |

</details>

<details>

<summary><strong>Math</strong></summary>

**Overview**

**Math** functions perform mathematical operations on individual rows of data. They accept numeric values or fields and return a numeric result for each row. These functions support operations such as rounding, calculating absolute values, and finding powers. If an input value is blank, the function returns a blank.

**List of Functions and their Use**

| **Function**                                     | **Use**                                                                                                                                          |
| ------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------ |
| ADD(number, number)                              | Same as a + b                                                                                                                                    |
| SUBTRACT(number, number)                         | Same as a – b                                                                                                                                    |
| MULTIPLY(number, number)                         | Same as a \* b                                                                                                                                   |
| DIVIDE(number, divisor)                          | Division that returns blank when the divisor is 0. Prefer it to / .                                                                              |
| ROUND(number, \[digits])                         | Round to the given decimals, 0 by default. digits must be a number, not a column.                                                                |
| <p>ROUNDUP(number) ,</p><p>ROUNDDOWN(number)</p> | Round up or down to a whole number. The decimals argument shown in the editor is not accepted on dashboards.                                     |
| CEILING(number) , FLOOR(number)                  | Next whole number up, or down                                                                                                                    |
| EVEN(number)                                     | Round up to the next even whole number                                                                                                           |
| ABS(number)                                      | Size of a value without its sign, such as a variance                                                                                             |
| NEGATE(number)                                   | Flip the sign                                                                                                                                    |
| MOD(number, divisor)                             | Remainder after division                                                                                                                         |
| QUOTIENT(number, divisor)                        | Whole part of a division                                                                                                                         |
| POWER(number, power)                             | Raise to a power, such as compound growth                                                                                                        |
| SQRT(number)                                     | Square root                                                                                                                                      |
| LOG(number) , LOG10(number)                      | Natural logarithm, or base-10 logarithm                                                                                                          |
| CUMSUM(number)                                   | Running total down the rows in data order. Rowlevel, so a grouped chart adds the running totals together: use it only in a table at order level. |

</details>

<details>

<summary><strong>Logical and Comparison</strong></summary>

**Overview**&#x20;

**Logical and Comparison Functions** evaluate conditions and compare values to determine whether specific criteria are met. They help dashboard designers classify data, create conditional metrics, and identify records based on defined conditions.

> <mark style="color:red;">**Note:**</mark> To replace blanks, write IF(ISNULL(x), 0, x) . FILL\_NA does not work on dashboards today.

**List of Functions**

| **Function**                                        | **Returns**              | **Use**                                                                                 |
| --------------------------------------------------- | ------------------------ | --------------------------------------------------------------------------------------- |
| IF(condition, if\_true, if\_false)                  | Type of the results      | Two-way choice. A blank condition takes if\_false .                                     |
| SWITCH(value, match, result, ..., \[default])       | Type of the results      | <p>Map each value to a result; the last argument is used when</p><p>nothing matches</p> |
| SWITCH(TRUE(), condition, result, ..., default)     | Type of the results      | Multi-way IF: the first true condition wins                                             |
| AND(condition, condition, ...)                      | True/false               | TRUE when all are true                                                                  |
| OR(condition, condition, ...)                       | True/false               | TRUE when any is true                                                                   |
| NOT(condition)                                      | True/false               | Reverse a condition                                                                     |
| XOR(condition, condition)                           | True/false               | TRUE when exactly one is true                                                           |
| TRUE() , FALSE()                                    | True/false               | The two constants                                                                       |
| ISNULL(value)                                       | True/false               | TRUE for a blank                                                                        |
| SETNULL() , SETNULLDATE()                           | Blank number, blank date | <p>Return a blank on purpose, as in</p><p>IF(x &#x3C; 0, SETNULL(), x)</p>              |
| EQ(value, value)                                    | True/false               | Same as ==                                                                              |
| GT , GTE , LT , LTE (value, value)                  | True/false               | Same as > , >= , < , <=                                                                 |
| <p>IN(column, list) or</p><p>ISIN(column, list)</p> | True/false               | TRUE when the value is in the list; replaces a chain of OR                              |
| ISNOTIN(column, list)                               | True/false               | TRUE when the value is not in the list                                                  |

</details>

<details>

<summary><strong>Text</strong></summary>

**Overview**

**Text** functions manipulate, combine, extract, and format text values in a dataset. They help dashboard designers standardise text, create meaningful labels, and organise information for better presentation and analysis in dashboard visualisations.

**Usage and Behaviour**

* All text functions operate at the row level.
* Text arguments must be text columns or quoted text values. Numeric columns must first be converted to text using `CONVERT_TO_STRING`. `CONCATENATE` is an exception and accepts numeric values directly.
* Text matching is case-sensitive.

**List of Functions**

| **Function**                                                     | **Returns** | **Use**                                                                      |
| ---------------------------------------------------------------- | ----------- | ---------------------------------------------------------------------------- |
| CONCATENATE(value, value, ...)                                   | Text        | Join labels. Numbers are accepted; a blank joins as empty text.              |
| LEFT(text, count) , RIGHT(text, count)                           | Text        | First or last characters, such as a code prefix                              |
| MID(text, start, count)                                          | Text        | Characters from a position; the first character is 1                         |
| SUBSTR(text, start, count)                                       | Text        | Like MID; a negative start counts from the end                               |
| <p>UPPER(text) , LOWER(text) ,</p><p>PROPER(text)</p>            | Text        | Make spelling consistent before grouping                                     |
| TRIM(text)                                                       | Text        | Remove spaces at the start and end                                           |
| LEN(text) or LENGTH(text)                                        | Number      | Number of characters                                                         |
| SEARCH\_REPLACE(text, find, replace)                             | Text        | Replace text                                                                 |
| REPLACE(text, find, replace)                                     | Text        | Same as SEARCH\_REPLACE on dashboards                                        |
| SUBSITUTE(text, find, replace, \[nth])                           | Text        | Replace text; spelled SUBSITUTE in the editor                                |
| REMOVE\_CHARACTERS(text, characters)                             | Text        | <p>Remove the given characters: 'O101' becomes 'O101' without '-</p><p>'</p> |
| REMOVE\_REGEX(text, pattern)                                     | Text        | Remove what a regular expression matches                                     |
| <p>STARTS_WITH(text, prefix) ,</p><p>ENDS_WITH(text, suffix)</p> | True/false  | Test the start or end                                                        |
| CONTAINS\_TEXT(text, pattern)                                    | True/false  | TRUE when a regular expression matches anywhere                              |
| EXACT(text, text)                                                | True/false  | Exact, case-sensitive match                                                  |
| REPT(text, times)                                                | Text        | Repeat text                                                                  |
| CHAR(number)                                                     | Text        | <p>Character for a code: CHAR(65) is</p><p>'A'</p>                           |
| Function                                                         | Returns     | Use                                                                          |
| FORMAT(value, pattern)                                           | Text        | A number or date as formatted text                                           |

**Common Format Patterns**

| Pattern        | 120000 or 12 Apr 2026 becomes |
| -------------- | ----------------------------- |
| '#,##0'        | 120,000                       |
| '#,##0.00'     | 120,000.00                    |
| '#,##0,"K"'    | 120K                          |
| '0.0%' on 0.25 | 25.0%                         |
| 'MMM yyyy'     | Apr 2026                      |

</details>

<details>

<summary><strong>Date and Time</strong></summary>

**Overview**

**Date and Time** functions manipulate, extract, and calculate values from date and time fields. They help to analyse time-based data, calculate date differences, and derive information such as years, months, and days.

In dashboard designing, these functions help track performance over time, identify trends, monitor deadlines, and create time-based metrics for data visualisation.

**Usage and Behaviour**

* All Date and Time functions operate at the row level.
* Date arguments must reference actual date columns or valid date values. Text columns containing dates must first be converted into date values using `CONVERT_TO_DATE`.

**List of Functions**

| **Function**                                                      | **Returns**    | **Use**                                                                                        |
| ----------------------------------------------------------------- | -------------- | ---------------------------------------------------------------------------------------------- |
| <p>YEAR(date) , MONTH(date) ,</p><p>DAY(date)</p>                 | Number         | Parts of a date, for year and month buckets                                                    |
| MONTH\_NAME(date)                                                 | Text           | <p>Full month name, such as 'April'.</p><p>Sorts A to Z, so sort by MONTH.</p>                 |
| WEEKDAY(date)                                                     | Number         | <p>Day of the week: 1 is Monday, 7 is</p><p>Sunday</p>                                         |
| <p>HOUR(datetime) , MINUTE(datetime) ,</p><p>SECOND(datetime)</p> | Number         | Parts of a time. A date column has no time, so these fail on it.                               |
| TODAY() , NOW()                                                   | Date, datetime | The current date, or date and time                                                             |
| CREATE\_DATE(year, month, day)                                    | Date           | <p>Build a date, for comparisons:</p><p>COL('order_date') >=</p><p>CREATE_DATE(2026, 4, 1)</p> |
| Function                                                          | Returns        | Use                                                                                            |
| ADD\_DAY(date, days)                                              | Date           | Move a date by days, such as a due date                                                        |
| EDATE(date, months)                                               | Date           | Same day, some months later; negative goes back. EDATE(d, 12) is one year later.               |
| EOMONTH(date, \[months])                                          | Date           | Last day of the month, months away; 0 by default                                               |
| DATEDIF(start, end)                                               | Number         | Days from start to end                                                                         |
| MONTH\_DIFF(start, end)                                           | Number         | Calendar months from start to end ; the day of the month is ignored                            |
| <p>IS_MONTH_START(date) ,</p><p>IS_QUARTER_START(date)</p>        | True/false     | TRUE on the 1st of a month, or of a quarter                                                    |
| IS\_LEAP\_YEAR(date)                                              | True/false     | TRUE in a leap year                                                                            |
| ADD\_YEAR(date, years)                                            | Date           | Adds 365 days per year, so it drifts a day across a leap year. Prefer EDATE.                   |
| TO\_JULIAN\_DATE(date)                                            | Text           | The date as year and day of year: 12 Apr 2025 is '25102'                                       |
| PARSE\_JULIAN\_DATE(text)                                         | Date           | The reverse of TO\_JULIAN\_DATE                                                                |

> <mark style="color:red;">**Note:**</mark>
>
> * To identify the last day of a month, use the following expression:
>
> `COL('order_date') == EOMONTH(COL('order_date'), 0)`
>
> * &#x20;`IS_MONTH_END` and `IS_QUARTER_END` currently return incorrect results because they compare each row with the next row instead of evaluating the date value itself.

</details>

<details>

<summary><strong>Time intelligence</strong></summary>

**Overview**

**Time Intelligence** functions perform aggregate calculations across specific time periods, such as months, quarters, and years. They help to analyse business performance, track progress, and compare results across different periods in dashboard visualisations.

**List of Functions**

| **Function**                                           | **Returns the measure for**                                                                        |
| ------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| TOTALMTD(measure, date)                                | Month to date                                                                                      |
| TOTALQTD(measure, date)                                | Quarter to date                                                                                    |
| TOTALYTD(measure, date)                                | Calendar year to date                                                                              |
| TOTAL\_PM(measure, date)                               | The previous month, in full                                                                        |
| TOTAL\_PYCM(measure, date)                             | The same month last year                                                                           |
| TOTALYTD\_PYCM(measure, date)                          | Last year's year to date, up to the same month                                                     |
| CALCULATE(measure, DATESBETWEEN(date, 'start', 'end')) | A fixed range, both ends included, whatever the date filter says. Dates are written '2026-04-01' . |

> <mark style="color:red;">**Note:**</mark>
>
> Example: TOTALYTD(SUM(COL('project\_revenue')), COL('order\_date'))
>
> **Important Considerations**
>
> **1. Create Time Intelligence Fields Separately**
>
> Always save a Time Intelligence calculation as a separate calculated field. Do not nest it within another arithmetic expression, as this may cause the calculation to fail.
>
> **Example:**
>
> Instead of nesting the calculation:
>
> * DIVIDE(SUM(x) - TOTAL\_PYCM(...), TOTAL\_PYCM(...))
> * Save  `revenue_ly` as the `TOTAL_PYCM` field.
> * Write DIVIDE(revenue\_cm - revenue\_ly, revenue\_ly) in a second field.

</details>

<details>

<summary><strong>Filter and Context</strong></summary>

bfunctions control the data considered during calculations by applying, modifying, or removing filters. They help users calculate measures based on specific conditions and filter selections.

In dashboard designing, these functions enable dynamic calculations, support comparisons across different data selections, and display relevant metrics based on dashboard filters and slicers.

**Usage and Behaviour**

* All Filter and Context functions are aggregate functions.
* `CALCULATE` evaluates a measure under modified filter conditions.
* Other Filter and Context functions are used within `CALCULATE` as its second and subsequent arguments.

**List of Functions**

| Function                                | Use                                                                                                                                                      |
| --------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CALCULATE(measure, filter, ...)         | The measure for a subset of rows, or with a filter removed                                                                                               |
| FILTER(condition)                       | Inside CALCULATE: keep only the rows where the condition is TRUE                                                                                         |
| ALL(column, ...)                        | Inside CALCULATE: ignore the filter and grouping on these columns, for share of total                                                                    |
| ALL()                                   | Inside FILTER\_TABLE: ignore every filter                                                                                                                |
| Function                                | Use                                                                                                                                                      |
| FILTER\_TABLE(ALL(), condition)         | Inside CALCULATE: test the condition over all rows, whatever the page filters say                                                                        |
| TREATAS(VALUES(column), target\_column) | Inside CALCULATE: apply one column's values as a filter on another column. Both must be in tables joined in the data model, with the same kind of value. |
| VALUES(column)                          | The distinct values of a column; used as TREATAS's first argument                                                                                        |
| USERELATIONSHIP(column, column)         | Inside CALCULATE: join on a second relationship between two tables, such as ship date instead of order date                                              |

> <mark style="color:red;">**Note:**</mark> See the below examples.
>
> **Laptop revenue:** CALCULATE(SUM(COL('project\_revenue')),
>
> FILTER(EQ(COL('product\_name'), 'Laptop')))
>
> **Revenue of all regions, for share of total:** CALCULATE(SUM(COL('project\_revenue')), ALL(COL('region\_name')))

> <mark style="color:red;">**Note:**</mark>&#x20;
>
> **1. Save CALCULATE Expressions as Separate Fields**
>
> Save each `CALCULATE` expression as a separate calculated field before using it in other expressions.
>
> **2. Avoid Nesting CALCULATE with Other Functions**
>
> Nesting `CALCULATE` with `FILTER` inside functions such as `DIVIDE` or arithmetic operators (such as subtraction) currently causes the expression to fail. Create separate calculated fields and combine them in a subsequent expression instead.

</details>

<details>

<summary><strong>Information and Type Conversion</strong></summary>

**Overview**

**Information and Type Conversion** functions retrieve information about data values, check their characteristics, and convert values between supported data types. They help users identify blank values, validate data, and convert values into the required formats.

In dashboard designing, these functions help prepare and standardise data for accurate calculations, reporting, and visualisation.

**List of Information Functions**

| **Function**                        | **Returns**        | **Use**                                                                                                                       |
| ----------------------------------- | ------------------ | ----------------------------------------------------------------------------------------------------------------------------- |
| HASONEVALUE(column)                 | True/false         | Aggregate. TRUE when exactly one value is left after filters and grouping.                                                    |
| SELECTEDVALUE(column, \[alternate]) | Type of the column | <p>Aggregate. The one value left, or alternate when there is not</p><p>exactly one. Used for titles and parameter tables.</p> |
| ISEVEN(number) , ISODD(number)      | True/false         | Even or odd                                                                                                                   |
| Function                            | Returns            | Use                                                                                                                           |
| IS\_ALPHA(text)                     | True/false         | TRUE when the text holds letters only                                                                                         |

> <mark style="color:red;">**Note:**</mark> The below is an example:
>
> IF(\
> HASONEVALUE(COL('region\_name')), SELECTEDVALUE(COL('region\_name')),\
> 'All regions'\
> )
>
> This expression displays the region name when a single region is selected or represented in the chart. When multiple regions are included, it displays **'All regions'** instead.
>
> For example:
>
> * **Chart grouped by region:** Displays the respective region name for each data point.
> * **KPI card showing multiple regions:** Displays 'All regions'.

**List of Type  Conversion Functions**

| **Function**               | **Returns** | **Use**                                                                                                                         |
| -------------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------- |
| TO\_INT(value)             | Number      | Whole number. Lenient: a value it cannot read becomes blank, decimals are cut.                                                  |
| TO\_FLOAT(text)            | Number      | Decimal number. Strict: one unreadable value fails the field.                                                                   |
| CONVERT\_TO\_NUMERIC(text) | Number      | Same as TO\_FLOAT                                                                                                               |
| CONVERT\_TO\_STRING(value) | Text        | A number or date as text. A decimal keeps its '.0': 120000.0 becomes '120000.0', so wrap it in TO\_INT first for whole numbers. |
| CONVERT\_TO\_DATE(text)    | Date        | Reads YYYY-MM-DD text; any other format becomes blank                                                                           |
| COL('name')                | The column  | A column whose name has spaces or symbols                                                                                       |

> <mark style="color:red;">**Note:**</mark> Clean text before converting it: TO\_FLOAT(SEARCH\_REPLACE(COL('amount\_text'), ',', '')) turns '1,200' into 1200.

</details>

<details>

<summary><strong>Parameter Table</strong></summary>

**Overview**

**Parameter Table** stores predefined values that can be referenced in calculated-field expressions. It allows users to manage and reuse parameter values in calculations instead of specifying them directly in expressions.

In dashboard designing, parameter tables can support flexible calculations, business thresholds, and performance comparisons. Where supported, they can also enable users to explore dashboard results using different parameter values.

> <mark style="color:red;">**Note:**</mark> These are written in the calculated-field editor with the Parameter table switch **ON** in the dashboard designer.

**List of Functions**

| **Function**                                          | **Use**                                                                                                                            |
| ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| PARAM\_TABLE({column: \[values], ...}, ...)           | A list of choices, written by column. It can also be written by row, \[{...}, {...}] , or as columns=\[...], rows=\[\[...], ...] . |
| PARAM\_RANGE(start, end, step, \[column], \[default]) | Evenly spaced numbers for a what-if slider; at most 10,000 values. column is 'value' when left out.                                |
| Table\['column'] or COL('Table.column')               | A column of a parameter table                                                                                                      |
| SELECTEDVALUE(Table\['column'], alternate)            | The viewer's pick, or alternate when there is not exactly one                                                                      |
| HASONEVALUE(Table\['column'])                         | TRUE when exactly one choice is picked                                                                                             |

**Optional Arguments of PARAM\_TABLE**

| **Argument**            | **Use**                                                                 |
| ----------------------- | ----------------------------------------------------------------------- |
| sort\_by="order"        | The column that sets the slicer's order; a number or date column        |
| default={"kpi": "Cost"} | The choice the slicer opens on                                          |
| format\_by="fmt"        | A column of number formats, one per choice                              |
| field\_by="field"       | The columns whose values are field names; every name is checked on save |

</details>
{% endtab %}

{% tab title="Use Cases" %}
**Overview**

Each use case starts from the same eight sample orders, shows the formula, and shows the result SCIKIQ's engine returns for it. The results were computed by the engine; a few group totals add up rows the engine returned.

**Use Cases**

<details>

<summary><strong>Sample Data</strong></summary>

**Description**

The below sample data contains eight orders recorded over a two-year period, with a total revenue of 710,000 and a total cost of 456,000.

> <mark style="color:red;">**Note:**</mark> Each of the below use case uses the same set of eight sample orders and shows the formula along with the result returned by the SCIKIQ engine. The results are calculated by the engine, while some group totals are obtained by adding the individual row results returned by the engine.

See below for the [**Sample Data**](using-calculated-fields.md#sample-data) and also for description on  [**Row-level or Aggregate**](using-calculated-fields.md#row-level-or-aggregate) and [**Aggregate: One Value per Group**](using-calculated-fields.md#aggregate-one-value-per-group)**.**

#### **Sample Data**

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th><th valign="top"></th><th valign="top"></th><th valign="top"></th><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>Order Id</strong></td><td valign="top"><strong>Order Date</strong></td><td valign="top"><strong>Region Name</strong></td><td valign="top"><strong>Product Name</strong></td><td valign="top"><strong>Customer Name</strong></td><td valign="top"><strong>Project Revenue</strong></td><td valign="top"><strong>Project Cost</strong></td></tr><tr><td valign="top">O-101</td><td valign="top">2025-04-12</td><td valign="top">North</td><td valign="top">Laptop</td><td valign="top">Acme Corp</td><td valign="top">120,000</td><td valign="top">90,000</td></tr><tr><td valign="top">O-102</td><td valign="top">2025-05-03</td><td valign="top">North</td><td valign="top">Phone</td><td valign="top">Beta Ltd</td><td valign="top">45,000</td><td valign="top">30,000</td></tr><tr><td valign="top">O-103</td><td valign="top">2025-05-20</td><td valign="top">South</td><td valign="top">Laptop</td><td valign="top">Acme Corp</td><td valign="top">150,000</td><td valign="top">100,000</td></tr><tr><td valign="top">O-104</td><td valign="top">2026-04-08</td><td valign="top">South</td><td valign="top">Tablet</td><td valign="top">Delta Inc</td><td valign="top">60,000</td><td valign="top">48,000</td></tr><tr><td valign="top">O-105</td><td valign="top">2026-04-25</td><td valign="top">East</td><td valign="top">Phone</td><td valign="top">Beta Ltd</td><td valign="top">30,000</td><td valign="top">33,000</td></tr><tr><td valign="top">O-106</td><td valign="top">2026-05-14</td><td valign="top">East</td><td valign="top">Laptop</td><td valign="top">Gamma Co</td><td valign="top">200,000</td><td valign="top">140,000</td></tr><tr><td valign="top">O-107</td><td valign="top">2026-05-30</td><td valign="top">North</td><td valign="top">Tablet</td><td valign="top">Delta Inc</td><td valign="top">80,000</td><td valign="top"><em>blank</em></td></tr><tr><td valign="top">O-108</td><td valign="top">2026-06-02</td><td valign="top">North</td><td valign="top">Phone</td><td valign="top">acme corp</td><td valign="top">25,000</td><td valign="top">15,000</td></tr></tbody></table>

Three rows are there on purpose, because real data has them too:

O-105 sold at a loss.

O-107 has no cost recorded.

O-108 spells the customer with stray spaces and in lower case.

#### **Row-level or Aggregate**

The same question, gross margin, can be computed per row or per group. The two answers differ, and the difference decides where a field can go.

Row-level: a new value on every row gross\_margin = project\_revenue - project\_cost

| **Order\_Id** | **Gross Margin**                   |
| ------------- | ---------------------------------- |
| O-101         | 30,000                             |
| O-102         | 15,000                             |
| O-103         | 50,000                             |
| O-104         | 12,000                             |
| O-105         | -3,000                             |
| O-106         | 60,000                             |
| O-107         | _blank_, because the cost is blank |
| O-108         | 10,000                             |

A row-level field can group a chart, filter it, or feed a slicer. In a measure well it is rolled up:

with Sum, this field shows 174,000 on a card.

#### **Aggregate: One Value per Group**

total\_revenue = SUM(COL('project\_revenue')) and total\_cost =

SUM(COL('project\_cost')) total\_gross\_margin = total\_revenue - total\_cost is built on those two, so it is computed per group too.

| **Region**      | **Total Revenue** | **Total Cost** | **Total Gross Margin** |
| --------------- | ----------------- | -------------- | ---------------------- |
| East            | 230,000           | 173,000        | 57,000                 |
| North           | 270,000           | 135,000        | 135,000                |
| South           | 210,000           | 148,000        | 62,000                 |
| Card, no region | 710,000           | 456,000        | 254,000                |

An aggregate field is recomputed for every bar, row or cell, so it is a measure only.

> <mark style="color:red;">**Note:**</mark> **Why the two cards differ**
>
> The card shows 174,000 for the row-level field and 254,000 for the aggregate field. O-107 explains the gap. Row by row, its margin is blank and drops out. As a total, its 80,000 of revenue counts while its blank cost adds nothing. Neither is wrong; they answer different questions. Use case 2 shows how to choose on purpose.

</details>

<details>

<summary><strong>1: Creating a New Data Grouping</strong></summary>

A row-level field placed on a chart axis, a legend or a slicer creates a new way to group. The engine computes each field row by row; the tables show what a bar chart grouped by the field adds up to.

#### Size bands with SWITCH(TRUE(), ...)

The conditions are tested in order, so 120,000 stops at 'Large' and never reaches 'Medium'.

| **Size Band** | **Orders**              | **Revenue** |
| ------------- | ----------------------- | ----------- |
| Large         | 3 (O-101, O-103, O-106) | 470,000     |
| Medium        | 2 (O-104, O-107)        | 140,000     |
| Small         | 3 (O-102, O-105, O-108) | 100,000     |

#### Product groups with SWITCH

SWITCH(COL('product\_name'), 'Laptop', 'Computing', 'Tablet', 'Computing',

'Mobile')

Computing gets 5 orders and 610,000; Mobile, the default, gets 3 orders and 100,000.

#### Focus regions with IF and IN

IF(IN(COL('region\_name'), \['North', 'South']), 'Focus regions', 'Other regions')

Focus regions show 480,000 and Other regions 230,000.

#### Clean labels with PROPER and TRIM

Grouped by the raw customer\_name , the chart shows five customers, because acme corp (O-108) is a different value from Acme Corp . Clean it first:

PROPER(TRIM(COL('customer\_name')))

| **Customer** | **Raw Grouping** | **Cleaned Grouping**  |
| ------------ | ---------------- | --------------------- |
| Acme Corp    | 270,000          | 295,000               |
| acme corp    | 25,000           | merged into Acme Corp |
| Beta Ltd     | 75,000           | 75,000                |
| Delta Inc    | 140,000          | 140,000               |
| Gamma Co     | 200,000          | 200,000               |

</details>

<details>

<summary><strong>2: Calculating Gross Margin Percentage by Region</strong></summary>

A ratio must be computed from totals, never added up from per-row ratios. Here are three ways to put margin % on a bar chart by region; only one gives the true margin.

**Wrong**: A row-level ratio in the measure well. DIVIDE(project\_revenue project\_cost, project\_revenue) gives each order's margin, and the well then adds them up or averages them.

**Right:** A ratio of totals. gross\_margin\_pct = DIVIDE(total\_gross\_margin, total\_revenue) , built on the aggregate fields from the previous section.

| **Region** | **Row ratio, Sum** | **Row Ratio, Average** | **Ratio of Totals** |
| ---------- | ------------------ | ---------------------- | ------------------- |
| East       | 20.0%              | 10.0%                  | 24.8%               |
| North      | 98.3%              | 32.8%                  | 50.0%               |
| South      | 53.3%              | 26.7%                  | 29.5%               |
| Card       |                    |                        | 35.8%               |

The sum adds percentages, so it means nothing. The average gives a 30,000 order the same weight as a 200,000 one. Only the ratio of totals matches the business number:

East's 57,000 margin divided by its 230,000 revenue.

#### The blank cost

North's 50.0% is too high. O-107 brings 80,000 of revenue and no recorded cost, so it looks like pure margin. To count only orders that have a cost, save two fields:

revenue\_with\_cost = CALCULATE(SUM(COL('project\_revenue')),                               FILTER(NOT(ISNULL(COL('project\_cost')))))

gross\_margin\_pct\_costed = DIVIDE(revenue\_with\_cost - total\_cost, revenue\_with\_cost)

| **Region** | **revenue\_with\_cost** | **gross\_margin\_pct\_costed** |
| ---------- | ----------------------- | ------------------------------ |
| East       | 230,000                 | 24.8%                          |
| North      | 190,000                 | 28.9%                          |
| South      | 210,000                 | 29.5%                          |

Decide which question the card answers, and say it in the field's name and description. Replacing the blank with 0 through IF(ISNULL(...), 0, ...) does not help: North stays at 50.0%.

</details>

<details>

<summary><strong>3: Calculating Share of Total, Filtered Measures, and Average Order Value</strong></summary>

All four are aggregate fields, so the same field is right on a card and on every bar.

<table data-header-hidden><thead><tr><th></th><th></th><th></th><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td colspan="2"><strong>Field</strong></td><td colspan="4"><strong>Formula</strong></td><td> </td></tr><tr><td colspan="2">revenue_share</td><td colspan="4"><p>DIVIDE(SUM(COL('project_revenue')), CALCULATE(SUM(COL('project_revenue')),</p><p>ALL(COL('region_name'))))</p></td><td> </td></tr><tr><td colspan="2">laptop_revenue</td><td colspan="4"><p>CALCULATE(SUM(COL('project_revenue')),</p><p>FILTER(EQ(COL('product_name'), 'Laptop')))</p></td><td> </td></tr><tr><td colspan="2">laptop_share</td><td colspan="4">DIVIDE(laptop_revenue, total_revenue)</td><td> </td></tr><tr><td colspan="2">avg_order_value</td><td colspan="4">DIVIDE(SUM(COL('project_revenue')), COUNTROWS())</td><td> </td></tr><tr><td><strong>Region</strong></td><td colspan="2"><strong>revenue_share</strong></td><td><strong>laptop_revenue</strong></td><td><strong>laptop_share</strong></td><td colspan="2"><strong>avg_order_value</strong></td></tr><tr><td>East</td><td colspan="2">32.4%</td><td>200,000</td><td>87.0%</td><td colspan="2">115,000</td></tr><tr><td>Region</td><td colspan="2">revenue_share</td><td>laptop_revenue</td><td>laptop_share</td><td colspan="2">avg_order_value</td></tr><tr><td>North</td><td colspan="2">38.0%</td><td>120,000</td><td>44.4%</td><td colspan="2">67,500</td></tr><tr><td>South</td><td colspan="2">29.6%</td><td>150,000</td><td>71.4%</td><td colspan="2">105,000</td></tr><tr><td>Card</td><td colspan="2"> </td><td>470,000</td><td>66.2%</td><td colspan="2">88,750</td></tr></tbody></table>

**How they work:**

**revenue\_share:** ALL(COL('region\_name')) drops the region grouping inside CALCULATE, so every bar is divided by 710,000.

**laptop\_revenue:** FILTER keeps only Laptop rows inside CALCULATE. The chart's own filters still apply on top.

**laptop\_share** reads laptop\_revenue from its own saved field. Writing the CALCULATE inside DIVIDE directly fails today.

</details>

<details>

<summary><strong>4: Working with Date Calculations</strong></summary>

Date parts are row-level, so they make good dimensions.

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th><th valign="top"></th><th valign="top"></th><th valign="top"></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>order_id</strong></td><td valign="top"><strong>order_date</strong></td><td valign="top"><strong>Year</strong></td><td valign="top"><strong>Month Name</strong></td><td valign="top"><strong>Week Day</strong></td><td valign="top"><strong>Days to 30 Jun 2026</strong></td></tr><tr><td valign="top">O-101</td><td valign="top">2025-04-12</td><td valign="top">2025</td><td valign="top">April</td><td valign="top">6 (Sat)</td><td valign="top">444</td></tr><tr><td valign="top">O-102</td><td valign="top">2025-05-03</td><td valign="top">2025</td><td valign="top">May</td><td valign="top">6 (Sat)</td><td valign="top">423</td></tr><tr><td valign="top">O-103</td><td valign="top">2025-05-20</td><td valign="top">2025</td><td valign="top">May</td><td valign="top">2 (Tue)</td><td valign="top">406</td></tr><tr><td valign="top">O-104</td><td valign="top">2026-04-08</td><td valign="top">2026</td><td valign="top">April</td><td valign="top">3 (Wed)</td><td valign="top">83</td></tr><tr><td valign="top">O-105</td><td valign="top">2026-04-25</td><td valign="top">2026</td><td valign="top">April</td><td valign="top">6 (Sat)</td><td valign="top">66</td></tr><tr><td valign="top">O-106</td><td valign="top">2026-05-14</td><td valign="top">2026</td><td valign="top">May</td><td valign="top">4 (Thu)</td><td valign="top">47</td></tr><tr><td valign="top">O-107</td><td valign="top">2026-05-30</td><td valign="top">2026</td><td valign="top">May</td><td valign="top">6 (Sat)</td><td valign="top">31</td></tr><tr><td valign="top">O-108</td><td valign="top">2026-06-02</td><td valign="top">2026</td><td valign="top">June</td><td valign="top">2 (Tue)</td><td valign="top">28</td></tr></tbody></table>

The last column is DATEDIF(COL('order\_date'), CREATE\_DATE(2026, 6, 30)) . Use TODAY() in place of CREATE\_DATE for an age that updates every day.

#### Revenue by year and by month

YEAR(COL('order\_date')) on the axis gives 2025: 315,000 and 2026: 395,000.

MONTH\_NAME(COL('order\_date')) gives April: 210,000, May: 475,000 and June: 25,000. Sorted by the name, the axis reads April, June, May. Add MONTH(COL('order\_date')) to the sort well to get calendar order.

Month names merge years: April here is April 2025 and April 2026 together. For one bar per month of each year, put YEAR and MONTH\_NAME on the axis together.

#### Other date fields

<table data-header-hidden><thead><tr><th valign="top"></th><th valign="top"></th><th></th></tr></thead><tbody><tr><td valign="top"><strong>Goal</strong></td><td valign="top"><strong>Formula</strong></td><td><strong>O-101 gives</strong></td></tr><tr><td valign="top">Renewal date one year later</td><td valign="top">EDATE(COL('order_date'), 12)</td><td><p>2026-04-</p><p>12</p></td></tr><tr><td valign="top">Month end</td><td valign="top">EOMONTH(COL('order_date'), 0)</td><td><p>2025-04-</p><p>30</p></td></tr><tr><td valign="top">Due in 30 days</td><td valign="top">ADD_DAY(COL('order_date'), 30)</td><td><p>2025-05-</p><p>12</p></td></tr><tr><td valign="top">Months open</td><td valign="top">MONTH_DIFF(COL('order_date'), CREATE_DATE(2026, 6, 30))</td><td>14</td></tr><tr><td valign="top">Label for a title</td><td valign="top">FORMAT(COL('order_date'), 'MMM yyyy')</td><td>Apr 2025</td></tr></tbody></table>

</details>

<details>

<summary><strong>5: Creating a KPI Dashboard with MTD, YTD, Previous Month, and Year Metrics</strong> </summary>

The page has a date filter set to May 2026. Time-intelligence fields read that filter: the latest date left is 30 May 2026, and every period is measured from it.

{% stepper %}
{% step %}
**Step 1: One saved field per period**

| **Field**        | **Formula**                                                      | **Card shows**                             |
| ---------------- | ---------------------------------------------------------------- | ------------------------------------------ |
| revenue\_cm      | SUM(COL('project\_revenue'))                                     | <p>280,000 (O-106 + O-</p><p>107)</p>      |
| revenue\_mtd     | TOTALMTD(SUM(COL('project\_revenue')), COL('order\_date'))       | 280,000                                    |
| revenue\_qtd     | TOTALQTD(SUM(COL('project\_revenue')), COL('order\_date'))       | <p>370,000 (April + May</p><p>2026)</p>    |
| revenue\_ytd     | TOTALYTD(SUM(COL('project\_revenue')), COL('order\_date'))       | <p>370,000 (January to</p><p>May 2026)</p> |
| revenue\_pm      | TOTAL\_PM(SUM(COL('project\_revenue')), COL('order\_date'))      | 90,000 (April 2026)                        |
| Field            | Formula                                                          | Card shows                                 |
| revenue\_ly      | TOTAL\_PYCM(SUM(COL('project\_revenue')), COL('order\_date'))    | 195,000 (May 2025)                         |
| revenue\_ytd\_ly | TOTALYTD\_PYCM(SUM(COL('project\_revenue')), COL('order\_date')) | <p>315,000 (January to</p><p>May 2025)</p> |
{% endstep %}

{% step %}
**Step 2: Growth fields built on them**

| **Field**      | **Formula**                                    | **Card shows** |
| -------------- | ---------------------------------------------- | -------------- |
| growth\_vs\_ly | DIVIDE(revenue\_cm - revenue\_ly, revenue\_ly) | 43.6%          |
| growth\_vs\_pm | DIVIDE(revenue\_cm - revenue\_pm, revenue\_pm) | 211.1%         |

Written as one formula, DIVIDE(SUM(...) - TOTAL\_PYCM(...), TOTAL\_PYCM(...)) fails. Splitting it into named fields is the fix, and it also lets each piece be checked on its own card.
{% endstep %}
{% endstepper %}

**The same fields in a table by region**

| **Region** | **revenue\_cm** | **revenue\_ly** | **growth\_vs\_ly** |
| ---------- | --------------- | --------------- | ------------------ |
| North      | 80,000          | 45,000          | 77.8%              |
| East       | 200,000         | _blank_         | _blank_            |
| South      | _blank_         | 150,000         | _blank_            |

East sold nothing in May 2025 and South sold nothing in May 2026, so their growth is blank, not 0% and not infinite.

</details>

<details>

<summary><strong>6: Building a Measure Step by Step</strong></summary>

There are three ways to build gross margin %, and on the sample all three give 35.8% on a card and East 24.8%, North 50.0%, South 29.5% by region.

{% stepper %}
{% step %}
**Fields that read fields (Recommended)**

| **Step** | **Field**            | **Formula**                                  |
| -------- | -------------------- | -------------------------------------------- |
| 1        | total\_revenue       | SUM(COL('project\_revenue'))                 |
| Step     | Field                | Formula                                      |
| 2        | total\_cost          | SUM(COL('project\_cost'))                    |
| 3        | total\_gross\_margin | total\_revenue - total\_cost                 |
| 4        | gross\_margin\_pct   | DIVIDE(total\_gross\_margin, total\_revenue) |

Each step can be put on a card and checked, and every later field can reuse it. This is the only way to combine CALCULATE and time-intelligence results.
{% endstep %}

{% step %}
**One formula with VAR and RETURN**

VAR revenue = SUM(COL('project\_revenue'))

VAR cost = SUM(COL('project\_cost'))

RETURN DIVIDE(revenue - cost, revenue)

Good for a measure used once. Each VAR is written into the RETURN line, so a VAR used twice is computed twice.
{% endstep %}

{% step %}
**Functions nested in one line**

DIVIDE(SUM(COL('project\_revenue')) - SUM(COL('project\_cost')), SUM(COL('project\_revenue')))

Fine when short. The innermost functions run first.
{% endstep %}
{% endstepper %}

#### Rules for nesting

1. Wrap every column in an aggregate inside an aggregate formula. project\_revenue / SUM(COL('project\_revenue')) has a bare column beside SUM, so each region returns a list of values instead of one, and the chart cannot draw it.
2. Save each CALCULATE and each time-intelligence function as its own field, then combine the fields.
3. Prefer SWITCH(TRUE(), ...) to IF inside IF. It reads top-down and is tested in order.
4. A field that reads an aggregate field is a measure, even with no aggregate of its own: gross\_margin\_pct cannot be a dimension.
5. &#x20;A field built only on row-level fields stays row-level: IF(gross\_margin < 0, 'Loss', 'Profit') can group a chart. On the sample it marks O-105 as a loss, and puts O-107, whose margin is blank, under 'Profit', because a blank condition takes the else branch.

</details>

<details>

<summary><strong>7: Working with Parameter Tables</strong></summary>

A parameter table lets the viewer choose what a chart shows. The examples use the same eight sample orders: by region, revenue is East 230,000, North 270,000 and South 210,000.

#### What a parameter table is

A parameter table is a small list of choices, such as three KPIs, that the viewer picks from. It is never joined to the data. Picking a choice does not filter any rows; it changes which field the chart uses.

**Four pieces work together:**

1. The parameter table holds the choices: Revenue, Cost, Gross Margin.
2. A slicer on one of its columns shows the choices to the viewer.
3. A chart slot or a calculated field turns the picked word into a real field: Cost becomes total\_cost.
4. The chart reads the data with that field. Its title and number format can follow the pick too.

#### **On the sample data, one bar chart by** **region shows:**

| **Viewer picks** | **East** | **North** | **South** |
| ---------------- | -------- | --------- | --------- |
| Revenue          | 230,000  | 270,000   | 210,000   |
| Cost             | 173,000  | 135,000   | 148,000   |
| Gross Margin     | 57,000   | 135,000   | 62,000    |
|                  |          |           |           |

#### Creating a Parameter Table

1. In the **Dashboard Designer**, open **Calculated Field** and turn on **Parameter Table**.&#x20;

The switch exists only in the Dashboard Designer.

2. **Name the table.**&#x20;

Formulas reach its columns by this name: kpi\_selector\['kpi'] .

3. **Fill the Grid with one row per choice, or type it on the Expression tab.**&#x20;

Both tabs show the same table.

4. **Set Order by, Starts on, Format by and Field by as needed.**
5. **Save.**

#### **A list of choices: kpi\_selector**

| **kpi**      | **Field**            | **fmt**    | **order** |
| ------------ | -------------------- | ---------- | --------- |
| Revenue      | total\_revenue       | $#,##0,"K" | 1         |
| kpi          | Field                | fmt        | order     |
| Cost         | total\_cost          | $#,##0,"K" | 2         |
| Gross Margin | total\_gross\_margin | #,##0      | 3         |

* kpi is what the viewer sees in the slicer.
* field names the measure each choice stands for. Marked with Field by, so every name is checked when the table is saved.
* fmt gives each choice its own number format (Format by): Revenue shows as $230K, Gross Margin as 57,000.     order sets the slicer's order (Order by).

#### The same table on the Expression tab:

<figure><img src="../../../.gitbook/assets/image (3259).png" alt=""><figcaption></figcaption></figure>

> <mark style="color:red;">**Note:**</mark> Column names are yours to choose. A column holds one kind of value, and a column name cannot contain a dot.

#### **A what-if number: discount and target**

* Set the Grid's Kind to Range, or write PARAM\_RANGE. A slicer on a range column is drawn as a slider.
* PARAM\_RANGE(start=0, end=0.5, step=0.05, column="pct", default=0.1).
* Saved as discount, this makes discount\['pct'] : 0, 0.05, 0.10 ... 0.50, opening at 0.10.
* PARAM\_RANGE(100000, 300000, 50000, column="target", default=250000).
* Saved as target, this makes target\['target'] : 100,000, 150,000 ... 300,000, opening at 250,000.

#### Read the pick: SELECTEDVALUE and HASONEVALUE

SELECTEDVALUE(kpi\_selector\['kpi'], 'Revenue') asks what the viewer picked. The second argument, the alternate, is what it returns when there is not exactly one pick, so a chart is never blank.

<table data-header-hidden><thead><tr><th valign="top"></th><th></th><th valign="top"></th></tr></thead><tbody><tr><td valign="top"><strong>The viewer picks</strong></td><td><p><strong>SELECTEDVALUE(kpi_selector['kpi'],</strong></p><p><strong>'Revenue')</strong></p></td><td valign="top"><strong>HASONEVALUE(kpi_selector['kpi'])</strong></td></tr><tr><td valign="top">Cost</td><td>'Cost'</td><td valign="top">TRUE</td></tr><tr><td valign="top">Nothing</td><td>'Revenue', the alternate</td><td valign="top">FALSE</td></tr><tr><td valign="top">Revenue and Cost</td><td>'Revenue', the alternate</td><td valign="top">FALSE</td></tr><tr><td valign="top">A choice since removed from the table</td><td>'Revenue', the alternate</td><td valign="top">FALSE</td></tr></tbody></table>

**A dynamic title that names the pick:**

IF(HASONEVALUE(kpi\_selector\['kpi']), SELECTEDVALUE(kpi\_selector\['kpi']), 'All

KPIs')

It reads 'Cost' when Cost is picked and 'All KPIs' when two are picked.

SCIKIQ replaces SELECTEDVALUE with the picked value before it reads any data. The rest of the formula then runs as if you had typed that value.

#### Switch the KPI a chart shows

There are two ways. Both use the same slicer on kpi\_selector\['kpi'] , both make the chart, title and number format follow the pick, and both compute only the picked measure.

{% stepper %}
{% step %}
**Way 1: The field column straight in the slot**

Drop kpi\_selector\['field'] into the chart's measure slot. No formula is needed. The pick Cost swaps the slot to total\_cost , so a bar chart by region shows East $173K, North $135K, South $148K in Cost's format.

The field column holds names, not formulas. To switch to a formula, save it as a calculated field first and put its name in the table.
{% endstep %}

{% step %}
**Way 2: SWITCH in a calculated field**

Save this as selected\_kpi and use it like any measure:

Before reading data, SCIKIQ resolves the pick and keeps only the matching branch:
{% endstep %}
{% endstepper %}

Before reading data, SCIKIQ resolves the pick and keeps only the matching branch:

| **The viewer picks**         | **Selected\_kpi becomes**      | **Card on the sample** |
| ---------------------------- | ------------------------------ | ---------------------- |
| Cost                         | total\_cost                    | 456,000                |
| Gross Margin                 | total\_gross\_margin           | 254,000                |
| Nothing, or Revenue and Cost | total\_revenue (the alternate) | 710,000                |

#### **Which way to use**

<table data-header-hidden><thead><tr><th valign="top"></th><th></th><th></th></tr></thead><tbody><tr><td valign="top"> </td><td><strong>Way 1: Field column</strong></td><td><strong>Way 2: SWITCH</strong></td></tr><tr><td valign="top">What you build</td><td>Only the parameter table</td><td>The table and a calculated field</td></tr><tr><td valign="top">Logic per choice</td><td>A straight swap to an existing field</td><td>Any formula per choice, and your own fallback</td></tr><tr><td valign="top">Nothing or several picked</td><td>The first choice by Order by, with a warning</td><td>The SELECTEDVALUE alternate</td></tr><tr><td valign="top">Best for</td><td>A simple KPI switch</td><td>Custom logic, VAR steps or a fallback</td></tr></tbody></table>

#### Switch the grouping, and what-if values

| **The viewer picks** | **The bar chart of revenue shows**              |
| -------------------- | ----------------------------------------------- |
| Region               | East 230,000 · North 270,000 · South 210,000    |
| Product              | Laptop 470,000 · Phone 100,000 · Tablet 140,000 |

A second slicer on column , with Slicer type set to Values of the named field, lists the regions or the products, whichever is picked, and filters by them. Date columns cannot be switched into a dimension slot.

#### **What-if discount**

With the discount range from above, save:

discounted\_revenue = MULTIPLY(total\_revenue, SUBTRACT(1,

SELECTEDVALUE(discount\['pct'], 0)))

| **Slider at**        | **Card** | **East** | **North** | South   |
| -------------------- | -------- | -------- | --------- | ------- |
| 0.10, where it opens | 639,000  | 207,000  | 243,000   | 189,000 |
| 0.20                 | 568,000  | 184,000  | 216,000   | 168,000 |

#### **Gap to a target**

With the target range, save:

gap\_to\_target = SUBTRACT(total\_revenue, SELECTEDVALUE(target\['target'],

250000\))

On a card, the gap is 460,000 at the opening value of 250,000, and 510,000 with the slider at 200,000.

Build what-if fields on an aggregate field such as total\_revenue , not on the raw column. On a raw column the subtraction happens row by row, and a chart then subtracts the target once per order.

#### The slicer and the rules

#### **How the slicer looks**

Drop a parameter-table column into a slicer, then choose its look under Presentation.

| **Look**                      | **Best for**                                    |
| ----------------------------- | ----------------------------------------------- |
| Buttons or chips              | A few KPIs, one click each                      |
| Drop-down (Collapse to a bar) | Saving canvas: one bar that opens over the page |
| Checkbox list                 | Long lists; adds search and Select all          |
| Slider                        | A PARAM\_RANGE column; chosen automatically     |

#### **Selection**

* Single value is what a KPI switch needs. The slicer opens on the table's Starts on choice, and Clear is off, so the chart always has a KPI.
* Multiple values adds Select all, search and Apply. It suits a parameter column placed on a table or pivot axis. With several picks, SELECTEDVALUE returns its alternate.
* Default selection sets what the slicer opens with: none, the last saved selection, the first or last value, or a fixed pick.

#### **Rules**

* A parameter column can go in four places only: a slicer, inside SELECTEDVALUE or HASONEVALUE, a measure slot, or a dimension slot (axis, pivot rows or columns, table column). Anywhere else is refused on save.
* With nothing picked, a switched slot shows the first choice by Order by, and SELECTEDVALUE returns its alternate. A chart is never blank by default.
* A picked number is shown as it is, never added up across rows; total rows show it too. FORMAT text is left blank in totals.
* With a parameter column on an axis, grand totals are not shown.
* Date columns cannot be switched into a dimension slot.
* Field by names are checked on save. A name that two tables share is written Table.column.
* One column holds one kind of value. A column name cannot contain a dot. A PARAM\_RANGE holds at most 10,000 values.

</details>
{% endtab %}

{% tab title="Key Aspects of Dashboard Design" %}
**Overview**

Designing effective dashboards involves more than selecting visualisations and arranging components. It is equally important to understand how different types of calculated fields behave, where they can be used, and how they affect the accuracy and performance of dashboard components.

This section covers three key aspects of dashboard design in SCIKIQ:

1. **Field Classification and Well Compatibility:** Understand the different types of calculated fields and where each type can be used within a dashboard component.
2. **Calculation Accuracy and Best Practices:** Avoid common expression and configuration mistakes that can produce incorrect results or unexpected behaviour.
3. **Dashboard Performance:** Apply best practices to reduce unnecessary data processing and keep dashboard components responsive.

Following these guidelines helps ensure that dashboard calculations produce reliable results, visualisations display data appropriately, and components perform efficiently.

**Key Aspects of Dashboard Design**

{% stepper %}
{% step %}
**Field Classification and Well Compatibility**

<details>

<summary><strong>Which Well accepts which field?</strong></summary>

This section explains where calculated fields can be placed within dashboard components.

A _well_ is a designated area within a dashboard component where users place fields to configure the visualisation.

SCIKIQ automatically classifies each calculated field into one of three types based on its formula. Users do not need to assign the type manually. The field type determines which component wells accept it.

To identify a field's type, evaluate its formula using the following two questions.

**Question 1: Does the formula contain an aggregate or filter function?**

Examples include `SUM`, `AVG`, `COUNT`, `MAX`, `CALCULATE`, and `TOTALYTD`.

* If yes, the field is classified as **Aggregate**.
* If no, proceed to Question 2.

**Question 2: Does the formula reference another field classified as Aggregate or Built on Aggregates?**

* If yes, the field is classified as **Built on Aggregates**.
* If no, the field is classified as **Row-Level**.

Field classification: two questions, three possible outcomes.

</details>

<details>

<summary><strong>Understanding field classification</strong></summary>

The following examples from the [sample data](using-calculated-fields.md#sample-data-1) illustrate the three classifications.

| Field and expression                                           | Aggregate in formula?          | References an aggregate field?   | Field type              |
| -------------------------------------------------------------- | ------------------------------ | -------------------------------- | ----------------------- |
| `gross_margin = project_revenue - project_cost`                | No                             | No; reads source columns         | **Row-Level**           |
| `total_revenue = SUM(COL('project_revenue'))`                  | Yes; SUM                       | Not applicable                   | **Aggregate**           |
| `gross_margin_pct = DIVIDE(total_gross_margin, total_revenue)` | No; DIVIDE is not an aggregate | Yes; references aggregate fields | **Built on Aggregates** |

**Important:** The third example often causes confusion. Although `gross_margin_pct` does not contain an aggregate function, it references fields that are aggregates. Therefore, SCIKIQ classifies it as Built on Aggregates, making it measure-only.

</details>

<details>

<summary><strong>Why only row-level fields can group a chart?</strong></summary>

A row-level field contains a value for each record. For example, each order has its own gross margin: O-101 has 30,000, O-102 has 15,000, and so on. A chart can use these individual values to group records.

An aggregate field calculates one value for each group after the chart determines the grouping. A field built on aggregates also depends on these group-level calculations.

Therefore, Aggregate and Built on Aggregates fields cannot be used to group or filter records. They can only be used as measures.

</details>

<details>

<summary><strong>Where can each field type be used?</strong></summary>

The following table shows which dashboard component areas accept each field type and how the fields behave.

| Dashboard component area               | Row-Level                           | Aggregate                  | Built on Aggregates        |
| -------------------------------------- | ----------------------------------- | -------------------------- | -------------------------- |
| Axis, legend, series                   | Yes                                 | No                         | No                         |
| Pivot rows and columns                 | Yes                                 | No                         | No                         |
| Slicer                                 | Yes                                 | No                         | No                         |
| Measure well (bar, line, table, pivot) | Yes, aggregated by the well         | Yes                        | Yes                        |
| Card, KPI tile, gauge                  | Yes, aggregated over filtered rows  | Yes                        | Yes                        |
| Grand totals                           | Sum or other applicable aggregation | Recalculated over all data | Recalculated over all data |
| Dynamic title                          | No                                  | Yes                        | Yes                        |
| Sort well                              | Yes                                 | Yes                        | Yes                        |

</details>

<details>

<summary><strong>Understanding how fields behave in dashboard components</strong></summary>

The following examples use the [sample data](using-calculated-fields.md#sample-data) mentioned in the Use Case tab.

**1. Axis, Legend, Pivot Rows and Columns, and Slicers**

These areas group or filter records and therefore require a value for each row. Only row-level fields can be used here.

For example:

`YEAR(COL('order_date'))`

This expression can be used to group records by year. An aggregate field such as `total_revenue` cannot be used for this purpose.

**2. Measure Well**

Both row-level and aggregate fields can be used in a measure well, but they behave differently.

* **Row-level fields:** The expression is evaluated for each record. The measure well then applies its selected aggregation (Sum, Average, Count, etc.) to calculate the value for each group.
* **Aggregate fields:** The expression is evaluated once per group. The measure well's aggregation setting does not change the result.
* **Built on Aggregates fields:** These fields are also evaluated using their underlying aggregate calculations and are treated as measures.

For example, summing a row-level margin ratio by region produces 98.3% for North, whereas the aggregate `gross_margin_pct` produces the correct ratio of 50.0%.

**3. Cards, KPI Tiles, and Gauges**

Without a dimension, all filtered records form a single group.

For example:

* Row-level `gross_margin` with Sum returns 174,000.
* Aggregate `total_gross_margin` returns 254,000.

The difference is due to order O-107. Its cost is blank, so its row-level margin is blank and is excluded from the row sum. However, its revenue of 80,000 is included in `total_revenue`.

**4. Grand Totals**

Row-level fields are aggregated across the underlying records. Aggregate fields are recalculated over the entire filtered dataset.

For example, the grand total for a margin percentage is the overall ratio of 35.8%, not the sum of the regional percentages (24.8% + 50.0% + 29.5%).

**5. Dynamic Titles**

Dynamic titles require a single value. A row-level field contains multiple values (one per record) and therefore cannot be used directly as a title. Aggregate and Built on Aggregates fields can return a single value.

**6. Sort Well**

Both row-level and aggregate fields can be used for sorting. For example, regions can be sorted by `total_revenue.`

</details>

<details>

<summary><strong>Default aggregation for row-level fields</strong></summary>

When a row-level field is placed in a measure well without an aggregation being explicitly selected, SCIKIQ applies an aggregation based on the field's data type:

* **Numbers:** Summed.
* **Boolean values:** Summed, which counts the TRUE records.
* **Text and dates:** Counted. Therefore, a text field placed in a measure well displays a count rather than the actual text values.

</details>

<details>

<summary><strong>Key takeaways</strong></summary>

1. **For grouping and filtering:** Use row-level fields. Avoid aggregate functions in the field or in any field it references.
2. **For ratios, percentages, and averages of totals:** Use aggregate fields to ensure correct results across charts, cards, and grand totals.
3. **Check field dependencies:** A field without an aggregate function can still be measure-only if it references aggregate fields.
4. **Check field classification before placement:** Use the two-question approach to determine which dashboard wells accept the field.

</details>
{% endstep %}

{% step %}
**Dashboard Best Practices**

Most incorrect dashboard calculations result from using a row-level calculation where a group-level calculation is required. Follow these recommendations when creating and using calculated fields.

<details>

<summary><strong>Recommended practices</strong></summary>

| Avoid                                                                                                                    | Recommended approach                                                                                     |
| ------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------- |
| Using a row-level ratio, such as `project_revenue / project_cost`, in a measure well when a ratio of totals is required. | Calculate the ratio of totals using `DIVIDE(total_gross_margin, total_revenue)`. See Part 2, Use Case 2. |
| Using the `/` operator when the divisor can be zero. It may return infinity.                                             | Use `DIVIDE(a, b)`, which returns blank when the divisor is zero.                                        |
| Referencing a bare column alongside an aggregate, such as `project_revenue / SUM(...)`.                                  | Wrap every column reference in an appropriate aggregate function.                                        |
| Nesting `CALCULATE` or a time-intelligence function inside other arithmetic expressions.                                 | Save the calculation as a separate field and combine the fields in a subsequent expression.              |
| Using `CUMSUM` on a grouped chart, which adds running totals together.                                                   | Use `TOTALMTD`, `TOTALQTD`, or `TOTALYTD` on a card with a date filter.                                  |
| Placing an aggregate field in a dimension well or slicer.                                                                | Use a row-level field.                                                                                   |
| Using `FORMAT` on a measure that must be charted, sorted, or totalled, because it returns text.                          | Use the measure's Format setting or `format_by` on a parameter table.                                    |
| Sorting month names alphabetically (April, June, May).                                                                   | Sort using `MONTH(COL('order_date'))`.                                                                   |
| Using `ADD_YEAR(date, 1)`, which can shift dates incorrectly across leap years.                                          | Use `EDATE(date, 12)`.                                                                                   |
| Using numbers or dates stored as text without conversion.                                                                | Convert them using `TO_INT`, `TO_FLOAT`, or `CONVERT_TO_DATE`, as appropriate.                           |
| Comparing a date with a text value, such as `order_date > '2026-01-01'`.                                                 | Use a date value: `order_date > CREATE_DATE(2026, 1, 1)`.                                                |
| Grouping raw text containing extra spaces or inconsistent letter cases.                                                  | Standardise the text using `PROPER(TRIM(...))` first.                                                    |
| Placing a text field in a measure well to display a label. It will be counted instead.                                   | Use `FIRST(...)` or a dynamic title.                                                                     |
| Using a dimension with thousands of distinct values, such as an order ID.                                                | Use a band, Top-N filter, or table.                                                                      |
| Building a What-If field directly on a raw column.                                                                       | Build it on an aggregate field, such as `total_revenue`.                                                 |

</details>

<details>

<summary><strong>Habits that keep a dataset healthy</strong></summary>

**Use meaningful field names**

Use lowercase names with underscores that describe the field's purpose, such as `gross_margin_pct` rather than `calc1`. Add a description for each field, as required by the editor.

**Build once, Reuse everywhere**

Calculated fields are saved at the dataset level and can be reused across dashboards that use the same dataset. Check the existing field list before creating duplicates.

**Avoid unnecessary calculated fields**

Basic aggregations do not require calculated fields. A column placed in a measure well already provides options such as Sum, Average, Count, Distinct Count, Min, and Max.

**Handle blank values carefully**

Understand how blank values affect calculations before using a field in a dashboard. [Use Case 2](using-calculated-fields.md#id-2-calculating-gross-margin-percentage-by-region) illustrates how a blank cost affects the margin calculation, changing the result from 28.9% to 50.0%.

**Validate before visualising**

Place a newly created field in a table alongside its source fields. Check a few records manually to verify the results before using it in charts or KPI components.

**Remove replaced fields**

Delete outdated calculated fields that are no longer required to prevent users from selecting obsolete versions accidentally.

</details>
{% endstep %}

{% step %}
**Performance**

The performance of a dashboard component containing calculated fields depends on three main factors:

1. Which calculation engine processes the component.
2. How many records are processed by the formulas.
3. Whether the formulas require data outside the current filter context.

<details>

<summary><strong>Use the dashboard-supported engine</strong></summary>

If any field in a component uses a function from the older engine (_Not available on dashboards now_), SCIKIQ routes the entire component to that engine, not just the field containing the function.

In the current build, this route fails. Use the alternatives.

</details>

<details>

<summary><strong>Reduce the number of records processed</strong></summary>

Page, dashboard, and component filters are applied before calculated fields are evaluated. Reducing the number of records through filters reduces the amount of data that formulas must process.

Consider the following practices:

* **Apply date filters:** Add a date filter at the page level when users do not need to view the entire history.
* **Keep row-level calculations lightweight:** Row-level fields are evaluated for every record processed by each component, whereas aggregate fields are evaluated once per group.
* **Perform heavy transformations upstream:** Handle complex text cleaning, parsing, and data type conversions in the dataset rather than repeatedly performing them in dashboard calculated fields.

</details>

<details>

<summary><strong>Use filter functions only when necessary</strong></summary>

Measures using `CALCULATE`, `FILTER`, `FILTER_TABLE`, `ALL`, `TREATAS`, `USERELATIONSHIP`, or time-intelligence functions require additional data processing.

In the current implementation, these calculations cause the component to read and join data twice: once with the current filters and once using the broader data required by the calculation.

Use these functions when the calculation requires data outside the current filter context, such as previous-year comparisons or share-of-total calculations.

For example, a simple `SUM(...)` with a page filter is less expensive than:

`CALCULATE(SUM(...), FILTER(...))`

when the additional filter logic is not required.

</details>

<details>

<summary><strong>Additional performance recommendations</strong></summary>

**Reuse saved fields**

A saved calculated field is computed once per component, even when multiple other fields reference it. A `VAR` used multiple times within an expression, however, is computed multiple times.

**Keep dimensions small**

Prefer dimensions with a limited number of values, such as bands or years. Avoid dimensions with thousands of distinct values, such as individual order IDs, where possible.

**Use SWITCH for parameter selection**

`SWITCH` on a parameter selection is inexpensive. SCIKIQ evaluates only the selected branch before performing the calculation.

**Identify slow calculated fields**

If a dashboard component loads slowly, remove its calculated fields one at a time to identify which field is affecting performance.

</details>
{% endstep %}
{% endstepper %}
{% endtab %}
{% endtabs %}



### **Related Topics**

* [**Creating Dashboard**](creating-dashboard.md)
