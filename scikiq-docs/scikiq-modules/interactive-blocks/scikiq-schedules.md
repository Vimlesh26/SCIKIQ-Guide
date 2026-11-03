---
icon: calendar-range
---

# SCIKIQ Schedules

***

### Instructions for Using this Page

* Click on an image to view it in a larger and clearer format.
* The inputs shown in the images are for example purposes only. You must enter the correct and actual data.

***

### Overview <a href="#id-3f4slw7a19lt" id="id-3f4slw7a19lt"></a>

This page describes the various activities that can be performed as part of managing schedules. The Scikiq Schedule module provides the management of schedules and the activities include **Viewing Scheduler Details, Updating Scheduler, Viewing Change History, Stopping Schedule,Viewing Logs, Viewing SLA History, Changing Permission, Running Scheduler Directly, Deleting Scheduler, Viewing Paused Schedulers, Viewing Scheduler Information, Downloading Scheduler List, Downloading Scheduler with Node Details,** and **Changing Version.**

***

### Procedure

Click on the below tabs to view step-by-step instructions:

{% tabs %}
{% tab title="Viewing Scheduler Details" %}
1. On the **SCIKIQ left navigation bar**, click **Scikiq Schedules** under **SCIKIQ CURATE.**

<figure><img src="../../.gitbook/assets/image (1721).png" alt=""><figcaption><p>SCIKIQ Orchestrator Menu Item</p></figcaption></figure>

The Scheduler List is displayed.

2. On the **Scheduler List** page, click the **View** ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAiACMDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1n5i7AMABjtRtf++P++aF/wBY/wCFctrviyaDWf7I0vyVnjQyXFxMCUhUDJ4HU4ppXE3Y6na/98f980h3Lj5gQSB0rh7Tx1Nay2k15NFeaZduY1uEiMUkTDruXJz1Fdy5yFI5BIptNAncdRRRUjGr/rH/AArC1vwqmo6hHqVlOLXUEG0uU3JKuMYZe/Fbm4LI2eM47UvmJ6/oaabQtzlrTwTvu7ebVZrd4rUlobW1h8uIN6kHkmupf+H/AHhR5iev6GkZ1baAcncO1DbYJWH0UUUhhRRRQAUUUUAFFFFAH//Z) icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1722).png" alt=""><figcaption><p>Scheduler List Page - View Icon</p></figcaption></figure>

The Scheduler details are displayed. See the image below

<figure><img src="../../.gitbook/assets/image (1723).png" alt=""><figcaption><p>Scheduler Details</p></figcaption></figure>
{% endtab %}

{% tab title="Updating Scheduler" %}
1. On the **Scheduler List** page, click  the **Edit** ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAjACUDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1g5aQjcQAB0pdh/vt+lA/1jfQf1pWYIpZiFUDJJ6AUAJsP99v0o2H++36VxV34nm8S6s+k6DLNCYiHW7QZUkHkMP7tdrGHEaCRgzgDcwGAT3NNqwk7hGSY1J6kUURf6pfpRSGA/1jfQf1rnPGmm6zrFrb2WksqQSMftLFwvHb3I9hXRbgsrZIHA6ml8xP7y/nTTs7iepm+H/D9p4d08W9quXPMkpHLn/D2rUpvmJ/eX86XzE/vr+dD1GJF/ql+lFEX+qX6UUgHYHpRgegoooAMD0FGB6CiigAooooA//Z)icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1724).png" alt=""><figcaption><p>Scheduler List Page - Edit Icon</p></figcaption></figure>

The scheduler page is displayed.

2. On the **Scheduler** page, make the required changes to the scheduler.

The scheduler is updated.
{% endtab %}

{% tab title="Viewing Change History" %}
1. On the **Scheduler List** page, click  the **Change History**![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAiACQDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD2JsmQDcQMZ4pdh/vt+lH/AC2H+7WP4m12PSbaOFbmGC6uXWONpDwgJ5bHfFNagbGw/wB9v0o2H++36VzK6apu5re11G+S+iiWVLiS5LCXOeqHjHHYVuaPftqek2906hXkX5lHQMODj8RQ0K5ajJMak8nFFEX+qX6UUhh/y2H+7UN7Yw3qL50UTvGd8TOm7Y3Y1KzBZQTnG30pfNX1P5GmBz81lr94yxzjTYioKi9jDGQA8Eqp4BP1xW5ZWkVhZQ2sAIjiUKuetSeavqfyNHmr6n8jQ2KwRf6pfpRRF/ql+lFIY+iiigAooooAKKKKAP/Z)icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1726).png" alt=""><figcaption><p>Scheduler List Page - Change History Icon</p></figcaption></figure>

The Resource Change Log page is displayed.

2. On the **Resource Change Log** page, view the change history either using **Filters** or **Quick Select**. For example, the last 3 Months.

<figure><img src="../../.gitbook/assets/image (1727).png" alt=""><figcaption><p>Resource Change Log page</p></figcaption></figure>

The change history is displayed. See the image below.

<figure><img src="../../.gitbook/assets/image (1728).png" alt=""><figcaption><p>Change History</p></figcaption></figure>
{% endtab %}

{% tab title="Stopping Schedule" %}
1. On the **Scheduler List** page, click the Stop Schedule ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAgACADASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1kli2BgYGeRRh/VfyoH+sP0FZHiDWZtIl0xYY43F3dLA+/Pyg9xjvTSuBr4f1X8qAWDYODkZ4FZOkazNqOs6xZyxxqljKscbLnLAjvWsf9YPoaGrAA/1h+grP1fRY9YeyaSV4/sk4nXaB8xHY1oEMGyMHIxyaMv6L+dAFDTtGj07UtRvEld2vpBIykDCkDtV8/wCsH0NGX9F/OgBi2TgYGODQB//Z) icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1729).png" alt=""><figcaption><p>Scheduler List Page - Stop Schedule Icon</p></figcaption></figure>

The Scheduler is stopped and the Success message is displayed. See the image below.

<figure><img src="../../.gitbook/assets/image (1730).png" alt=""><figcaption><p>Scheduler Stopped Status</p></figcaption></figure>

3. If you want to restart the schedule again, click the **Start Schedule** ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAkACcDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1g5aQjcQAB0pdh/vt+lA/1rfQf1ptxKYLWaUDJjRmx64GaYDth/vt+lGw/wB9v0rD8PeMNO8QqEjfybofegkPP4HvW9Q00JajYyTGpPXFFEX+qX6UUhgP9a30H9aZdRtNaTxLjc8bKM+pGKduCytkgcDqadvT+8v50wOU8NeAbLRWS5uyLq9ByGI+SM+w/qa6yk3p/eX86N6f3l/OhtvcSSQkX+qX6UURf6pfpRSGOwD2owPQUUUAGB6CjA9BRRQAUUUUAf/Z) icon.

<figure><img src="../../.gitbook/assets/image (1731).png" alt=""><figcaption><p>Scheduler List Page -Start Schedule Icon</p></figcaption></figure>

The scheduler is restarted.
{% endtab %}

{% tab title="View Logs" %}
1. On the **Scheduler List** page, click the **Logs** ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAkACMDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1ksd2AM8Z60Zf+6P++qP+Wp/3f61j6hqOojVmstP+wIEiV2e6ZhuLEgAY+lOwGxl/7o/76o3MMZUYJx1rmptb1e2hedp9DuEiwZI4JXL4yAcfnXSvyq/UUNWFcdRRRSGN/wCWp/3f61ialY351aW4tYWdJYUQPHKisjKSejAjvW0WCyfMcfL/AFpfMT+8KewjmJ9M1KawktlsSHkG0yvNF6g5O1QeMV07cKv1FHmJ/eFIzq2AGBO4UXuFh9FFFIYUUUUAFFFFABRRRQB//9k=) icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1733).png" alt=""><figcaption><p>Scheduler List Page - Logs Icon</p></figcaption></figure>

The Scheduler Logs page is displayed.

2. To view the details of a log, click the **Expand** button corresponding to it.

<figure><img src="../../.gitbook/assets/image (1734).png" alt=""><figcaption><p align="center">Expand Button</p></figcaption></figure>

The log details are displayed. See the image below.

<figure><img src="../../.gitbook/assets/image (1735).png" alt=""><figcaption><p>Log Details</p></figcaption></figure>
{% endtab %}

{% tab title="Viewing SLA History" %}
1. On the Scheduler List page, click  the SLA History ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAjACQDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1klt+1cdM80fvP9j9aP8Alr/wH+tZ2qXdz9qt9P09kS5uAXaVxkRIOrY7nsKYGj+8/wBj9aCXAJ+Tj61gMNRtYZ7q01Ce7NoxWaC5RcSgAE7SoG04PFbkNwl3ZpcRHMcse9foRRYRKDkA+tFIv3V+lFIYn/LX/gP9azNVguYL+21OzhNw8KtFLApwzxnn5c9wR0rSJAl5IHy9/rTt6/3l/OmBzUt219JOujWmoR3NwCkpmjMcK5GC7Z6kD061v21stlp8VtGcrDGEB9cCpvMU/wAY/OkZ12N8y9D3ouIVfur9KKF+6v0opDFwD1AowPQflRRQAYHoPyowPQflRRQAUUUUAf/Z) icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1757).png" alt=""><figcaption><p>Scheduler List Page - SLA History Icon</p></figcaption></figure>

2. The SLA History is displayed. See the image below

<figure><img src="../../.gitbook/assets/image (1758).png" alt=""><figcaption><p>SLA History</p></figcaption></figure>
{% endtab %}

{% tab title="Changing Permission" %}
1. On the Scheduler List page, click the Permissions ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAjACIDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1nLFiF24GOtH7z/Y/Whf9Y/4Vh+KNSlt4orK0ju5Li4IZhapl1iB+Yg9j2ppXEbhEg67f1oJcEZ24JxxXMaFqJtNXexa31SG0uAPs321CSHAJYbiScYGa6d/4f94UNWBMdRRRSGNX/WP+FYmrvPaa1BdJZXdzC1q8JNqoZlJIPrW1uCyNuOM4pfMT+9TEcrpqTtPpNpHZasI7SV5HuL5QCQVI659TXVP/AA/7wo81P71IzqxUA5O4UN3BD6KKKQwooooAKKKKACiiigD/2Q==) icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1755).png" alt=""><figcaption><p>Scheduler List Page - Permissions Icon</p></figcaption></figure>

2. The Resource Permission dialogue box is displayed.
3. On the Resource Permission dialogue box, change the permission, and then click the Save button.

<figure><img src="../../.gitbook/assets/image (1756).png" alt=""><figcaption><p>Resource Permissions</p></figcaption></figure>

4. The Permission applied successfully message is displayed.
{% endtab %}

{% tab title="Running Scheduler Directly" %}
1. On the **Scheduler List** page, click  the **Direct Run** ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAiACEDASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1klt+Fx0zzR8/qv5Gj/lqf93+tZF7f341S6gtpbSKC2t1mdpomcnOc9CPSnYDX+f1X8jQS4IztwTjism1vNR+0WjzzWc1lcKzGWKJk28ZBySetaz/AMP+8KAHUUUUgG/8tT/u/wBay77RJ7nUHu7XVJ7NpI1jdEiRwwGcfe+tahOJM4JGOwo3/wCy35UwMx9Dae8SS7vZri2TawtmAC+YP4jjt3x0zWm/8P8AvCjf/st+VITuKgK3UdRQA+iiikAUUUUAFFFFABRRRQB//9k=)icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1753).png" alt=""><figcaption><p>Scheduler List Page - Direct Run Icon</p></figcaption></figure>

The Adhoc Job with Parameter dialogue box is displayed.

2. On the **Adhoc Job with Parameter** dialogue box, click the **Submit** button.

<figure><img src="../../.gitbook/assets/image (1754).png" alt=""><figcaption><p>Adhoc Job with Parameter Dialogue Box</p></figcaption></figure>
{% endtab %}

{% tab title="Deleting Scheduler" %}
1. On the **Scheduler List** page, click  the **Delete** ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAiACADASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1nLknG3AOOaPn9V/I0J/F/vGuM8e+Ir7Q7q1jtbp4UmQkhIlY5B9T9apK7sJuyOz+f1X8jQC27DY6Z4rmvAus3et6bcT3lw03lyBF3RqpHGe3Wul/5aj/AHaTVnYE7gn8X+8a5Dx14Tv/ABHPZyWDQDyVZWEr7epHTiuuB2lsq3XPApd/+y35UJtO6Bq5zvgjw/d+HdKnt75ojJJLvHltuAGMda6L/lqP92jf/st+VAOZM4IGO4obu7glYdRRRSGFFFFAH//Z)icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1751).png" alt=""><figcaption><p>Scheduler List Page - Delete Icon</p></figcaption></figure>

The Delete Notification is displayed.

2. On the **Delete Notification**, click the **Yes** button.

The scheduler is deleted.
{% endtab %}

{% tab title="Untitled" %}

{% endtab %}

{% tab title="Viewing Deleted Schedulers" %}
1. On the Scheduler List page, enable the **Show Deleted Resources** option.

<figure><img src="../../.gitbook/assets/image (1749).png" alt=""><figcaption><p>Show Deleted Resources option</p></figcaption></figure>

The deleted schedulers are displayed.

<figure><img src="../../.gitbook/assets/image (1750).png" alt=""><figcaption></figcaption></figure>


{% endtab %}

{% tab title="Viewing Paused Schedulers" %}
1. On the **Scheduler List** page, enable the Show Paused Resources option.

<figure><img src="../../.gitbook/assets/image (1748).png" alt=""><figcaption><p>Show Paused Resources Option</p></figcaption></figure>

The paused schedulers are displayed.
{% endtab %}

{% tab title="Viewing Scheduler Information" %}
* On the **Scheduler List** page, click  the **Show Information** ![](data:image/png;base64,/9j/4AAQSkZJRgABAQEAeAB4AAD/2wBDAAoHBwkHBgoJCAkLCwoMDxkQDw4ODx4WFxIZJCAmJSMgIyIoLTkwKCo2KyIjMkQyNjs9QEBAJjBGS0U+Sjk/QD3/2wBDAQsLCw8NDx0QEB09KSMpPT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT09PT3/wAARCAAeAB8DASIAAhEBAxEB/8QAHwAAAQUBAQEBAQEAAAAAAAAAAAECAwQFBgcICQoL/8QAtRAAAgEDAwIEAwUFBAQAAAF9AQIDAAQRBRIhMUEGE1FhByJxFDKBkaEII0KxwRVS0fAkM2JyggkKFhcYGRolJicoKSo0NTY3ODk6Q0RFRkdISUpTVFVWV1hZWmNkZWZnaGlqc3R1dnd4eXqDhIWGh4iJipKTlJWWl5iZmqKjpKWmp6ipqrKztLW2t7i5usLDxMXGx8jJytLT1NXW19jZ2uHi4+Tl5ufo6erx8vP09fb3+Pn6/8QAHwEAAwEBAQEBAQEBAQAAAAAAAAECAwQFBgcICQoL/8QAtREAAgECBAQDBAcFBAQAAQJ3AAECAxEEBSExBhJBUQdhcRMiMoEIFEKRobHBCSMzUvAVYnLRChYkNOEl8RcYGRomJygpKjU2Nzg5OkNERUZHSElKU1RVVldYWVpjZGVmZ2hpanN0dXZ3eHl6goOEhYaHiImKkpOUlZaXmJmaoqOkpaanqKmqsrO0tba3uLm6wsPExcbHyMnK0tPU1dbX2Nna4uPk5ebn6Onq8vP09fb3+Pn6/9oADAMBAAIRAxEAPwD1kk7sAgcZ6UHcoJZ1AHUkcCl/5af8B/rXJeONcutGsvPtYJA0rm3JmAaIrjO4L3J6c+9NK7sJux1g3EZDKQfalUnLAkHHoK5nwXrNzrWmpd3UMvmMxhLR8QqF6EL2znHGeldMPvv+FDVtATuH/LT/AID/AFqpq+mxavpc9lMFKyDjcCQD2PBH86tlcnIJBxijaf75/IUDINPso9N0+C0hVVjhQKAowKnH33/Cjaf75/IUKuM8kk0gP//Z)icon corresponding to the required scheduler.

<figure><img src="../../.gitbook/assets/image (1745).png" alt=""><figcaption><p>Scheduler List Page - Show Information Icon</p></figcaption></figure>

The Scheduler Information screen is displayed.See the image below.

<figure><img src="../../.gitbook/assets/image (1746).png" alt=""><figcaption><p>Scheduler Information</p></figcaption></figure>
{% endtab %}

{% tab title="Downloading Scheduler List" %}
1. On the **Scheduler List** page, click the **Excel** button.

<figure><img src="../../.gitbook/assets/image (1740).png" alt=""><figcaption><p>Scheduler List Page - Excel Button</p></figcaption></figure>

The Scheduler List is downloaded in Excel format.

<figure><img src="../../.gitbook/assets/image (1741).png" alt=""><figcaption><p>Scheduler List In Excel</p></figcaption></figure>

**Download Scheduler List in CSV Format**

1. On the Scheduler List page, click the CSV button.

<figure><img src="../../.gitbook/assets/image (1742).png" alt=""><figcaption><p>Scheduler List Page - CSV Button</p></figcaption></figure>

The Scheduler List is downloaded in CSV format.

<figure><img src="../../.gitbook/assets/image (1743).png" alt=""><figcaption><p>Scheduler List Page - CSV Button</p></figcaption></figure>
{% endtab %}

{% tab title="Downloading Scheduler with Node Details" %}
1. On the Scheduler List page, click the Download with Node Details button.

<figure><img src="../../.gitbook/assets/image (1738).png" alt=""><figcaption><p>Download with Node Details Button</p></figcaption></figure>

2. The Scheduler List is downloaded with node details.

<figure><img src="../../.gitbook/assets/image (1739).png" alt=""><figcaption></figcaption></figure>
{% endtab %}

{% tab title="Changing Version" %}
1. On the **Scheduler List** page, click the **Version** drop-down box, and then enter the **version number** in the search field.

<figure><img src="../../.gitbook/assets/image (1736).png" alt=""><figcaption><p>Version Drop-down Box</p></figcaption></figure>

The Version Change Confirmation message box is displayed.

2. On the **Version Change** **Confirmation** message box, click the **Yes** button.

<figure><img src="../../.gitbook/assets/image (1737).png" alt=""><figcaption></figcaption></figure>

The required version is displayed
{% endtab %}
{% endtabs %}

***

### **Related Topics**

* [**Data Profiling**](data-profiling-1/)
* [**SCIKIQ Orchestrator** ](scikiq-orchestrator.md)

