# DescribeScanSessions {#doc_api_avds_DescribeScanSessions .reference}

You can call this operation to query task instances generated for scan tasks.

You can call this operation to query task instances generated for scan tasks by pagination.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeScanSessions&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeScanSessions| The operation that you want to perform. Set the value to DescribeScanSessions.

 |
|CurrentPage|Integer|No|3| The number of the page to return.

 |
|PageSize|Integer|No|20| The number of entries to return on each page.

 |
|ScanId|String|No|66c07fa5-542b-47df-8501-e0401dc42d3e| The ID of the scan task for which the task instance is generated.

 |
|Search|String|No|1.2.\*. \*| The search field of the scan task for which the task instance is generated.

 |
|SourceIp|String|No|1.2.3.4| The source IP address of the request.

 |
|StatusList.N|RepeatList|No|waiting| The status of the subtask for which the task instance is generated.

 -   **waiting**
-   **finished**
-   **running**
-   **aborted**

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Count|Integer|20| The number of entries returned.

 |
|CurrentPage|Integer|5| The current page number.

 |
|List| | | The list of returned task instances.

 |
|CreatedAt|Long|1565690460000| The time at which the scan was created.

 |
|FinishedAt|Long|1565690260000| The time at which the scan was ended.

 |
|Interval|Integer|1| The interval between scan tasks.

 |
|JobStatus|String|waiting| The status of the subtask.

 -   **waiting**
-   **finished**
-   **running**
-   **aborted**

 |
|Name|String|test| The name of the returned scan task.

 |
|Period|String|hour| The cycle of each scan task.

 -   **minute**: every minute
-   **hour**: every hour
-   **day**: every day
-   **week**: every week
-   **month**: every month

 |
|ReportStatus|String|running| The status of the reports generated for the task instances.

 -   **failed**
-   **finished**
-   **running**
-   **inexistent**

 |
|ReportUrl|String|http://\*\*\*.com| The report link generated for the each task instance.

 |
|RunPercent|Float|10.21| The scan progress of the task instance.

 |
|ScanId|String|c0065a11-fe41-44f4-a5d2-b921316ddb52| The ID of the subtask for which the task instance is generated.

 |
|Targets| |\["1.2.3.5"\]| The targets, such as IP, domain name, and subdomain name, of the task instance.

 |
|TaskId|Long|1236984| The ID of the task instance.

 |
|TriggerType|String|date| The trigger type of the subtask for which the task instance is generated.

 -   **date**: one time
-   **interval**: periodic task

 |
|PageCount|Integer|20| The number of returned pages.

 |
|PageSize|Integer|20| The number of returned entries per page.

 |
|RequestId|String|F8955687-DDFC-4FE1-BC67-5C613657B8E5| The ID of the request.

 |
|TotalCount|Integer|30| The number of returned task instances.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DescribeScanSessions
&CurrentPage=1
&PageSize=20
&ScanId=1111
&Search=task name
&SourceIp=1.2.3.4
&StatusList.1="finished"
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeScanSessions>
      <code>200</code>
	  <requestId>F8955687-DDFC-4FE1-BC67-5C613657B8E5</requestId>
	  <success>true</success>
	  <data>
		    <List>
			      <TaskId>11</TaskId>
			      <ScanId>11111</ScanId>
			      <JobStatus>waiting</JobStatus>
			      <CreatedAt>111212121</CreatedAt>
			      <FinishedAt>12121</FinishedAt>
			      <name>test</name>
			      <targets>1.2.3.5</targets>
			      <triggerType>date</triggerType>
			      <period>hour</period>
			      <interval>1</interval>
			      <reportStatus>running</reportStatus>
			      <reportUrl>http://***.com</reportUrl>
		    </List>
		    <PageNumber>1</PageNumber>
		    <PageSize>20</PageSize>
		    <TotalCount>100</TotalCount>
	  </data>
</DescribeScanSessions>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"F8955687-DDFC-4FE1-BC67-5C613657B8E5",
	"data":{
		"PageNumber":1,
		"TotalCount":100,
		"PageSize":20,
		"List":[
			{
				"reportUrl":"http://***.com",
				"interval":1,
				"name":"test",
				"reportStatus":"running",
				"JobStatus":"waiting",
				"TaskId":11,
				"period":"hour",
				"triggerType":"date",
				"targets":[
					"1.2.3.5"
				],
				"FinishedAt":12121,
				"CreatedAt":111212121,
				"ScanId":11111
			}
		]
	},
	"code":"200",
	"success":true
}
```

## Error codes {#section_1mf_cq1_byt .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

