# OP\_11705JoinIssueOuerySQLQuery

OP-11705 [Bug: Join issue on Query Input (#11705) | Scikiq | OpenProject](https://project.scikiq.com/openproject/projects/scikiq/work_packages/11705/activity) .\
**Issue :** in Join condition the \_id which is common in both Query Input is not coming in second one cause pipeline failing to process data.\
**Behaviour now works as follows:**

When a user drags multiple "Query Input" nodes and clicks on the "Get Columns" button, the name of the node is updated automatically.

**For example:**

(i)If one "Query Input" node is dragged, a connection is selected, and then the SQL query is provided. After clicking "Get Columns," the node is named "SQL Query\_0."

(ii)If the same node is dragged again, after selecting the connection and providing the SQL query, clicking "Get Columns" will rename the node to "SQL Query\_1." This continues with "SQL Query\_2," and so on.  ![](<../../.gitbook/assets/0 (4).png>)

Additionally, you can manually change the node names if necessary.

**For an existing pipeline,** if the user edits a pipeline that contains two nodes with the same name, user must manually update the node name. Otherwise, the task name cannot be saved. When the user tries to save the pipeline, an alert message will appear prompting **'There is some configuration error in nodes , please check error messages.’ Or ‘Duplicate Table names found :SQL Query"** at particular Node.![](<../../.gitbook/assets/1 (7).png>)

![](<../../.gitbook/assets/2 (4).png>)
