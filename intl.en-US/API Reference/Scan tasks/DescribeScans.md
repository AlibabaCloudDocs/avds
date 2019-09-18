# DescribeScans {#doc_api_avds_DescribeScans .reference}

You can call this operation to query scan tasks.

This API supports pagination, which returns specific pages of the query results. This allows you to view information such as the progress of the scan.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeScans&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeScans| The operation that you want to perform. Set the value to DescribeScans.

 |
|CurrentPage|Integer|No|1| The page number of the scan task list.

 |
|Lang|String|No|zh| The language in which the list of scan tasks is returned. Valid values:

 -   **zh**: Chinese
-   **en**: English

 |
|PageSize|Integer|No|20| The number of scan tasks to return on each page.

 |
|ScanId|String|No|2019031816494923023| The ID of the scan task.

 |
|ScanType|String|No|vuln| The scan type of the task. Valid values:

 -   **vuln**: vulnerability type
-   **content**: content risk

 |
|Search|String|No|\*\*\*. \*\*\*.net| The query condition \(task name, IP address, or domain name\) for the task to be queried.

 |
|SourceIp|String|No|1.2.3.4| The source IP address of the request.

 |
|StatusList.N|RepeatList|No|\["finished"\]| The status of the scan task.

 -   **waiting**
-   **finished**
-   **running**
-   **aborted**
-   **invalid**
-   **disabled**

 |
|TriggerType|String|No|date| The trigger type of the scan task. Valid values:

 -   **date**: one time
-   **interval**: periodic

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Count|Integer|3| The number of returned scan tasks.

 |
|CurrentPage|Integer|1| The current page number of the returned task list.

 |
|List| | | The list of scan tasks.

 |
|CronActive|String|1| The scheduling status of the scan task.

 -   **1**: active, indicating that the scan task can be scheduled.
-   **0**: invalid, indicating that the scan task cannot be scheduled.

 |
|EndDate|Long|212212000000| The end time of the returned scan task.

 |
|FlowName|String|skynet\_vul\_scan| The vulnerability scan mode of the returned task.

 -   **assets**: asset scan
-   **general**: standard scan
-   **skynet\_vul\_scan**: full scan

 |
|IndexIntervalInMinute|Integer|5| The homepage detection interval of the returned task.

 |
|Interval|Integer|10| The scan interval of the returned task.

 |
|JobStatistics|String|running| The statistics of the returned task instance. Valid values:

 -   **running**
-   **finished**
-   **aborted**

 |
|KeyWords| |65084125-edc6-4ef3-931f-c3e87945631e| The ID of the appended keyword library.

 |
|LastSheduleDate|Long|1111000000| The timestamp of the last scheduled task.

 |
|Name|String|test\_0710-3| The name of the returned task.

 |
|NextRunDate|Long|1212100000| The expected start time of the next scan for each returned task.

 |
|Period|String|minute| The cycle of each scan task.

 -   **minute**: every minute
-   **hour**: every hour
-   **day**: every day
-   **week**: every week
-   **month**: every month

 |
|RefJobId|String|65084125-edc6-4ef3-931f-c3e87945631e| The ID of the scan task that is associated with the task.

 |
|ReportUrl|String|http://\*\*\*.com| The link of the generated report for each returned task.

 |
|RunPercent|Float|100.0| The progress \(in percentage\) of the task that is in the running state.

 |
|RuntimeEnd|String|1545972690000| The start time of the returned scan task.

 |
|RuntimeStart|String|1545972690000| The end time of the returned scan task.

 |
|ScanAll|Integer|1| Indicates whether all assets have been scanned.

 |
|ScanId|String|2018071010171127450| The task ID of the corresponding scan task.

 |
|ScanType|String|vuln| The scan type of the returned task.

 -   **vuln**: vulnerability type
-   **content**: content risk

 |
|SiteIntervalInDay|Integer|1| The site detection interval of the returned task. Unit: days.

 |
|StartDate|Long|111122200000| The start time of each returned task.

 |
|Status|String|running| The scan status of the returned task.

 -   **waiting**
-   **finished**
-   **running**
-   **aborted**
-   **invalid**
-   **disabled**

 |
|Targets| |\["demo.testfire.net"\]| The name of the asset \(IP address, domain name, or subdomain name\).

 |
|TargetsOriginal| |testtag| The original content of the asset when the scan task was created, that was, the group label of the scanned asset.

 |
|TriggerType|String|date| The trigger type of the returned task.

 -   **date**: one time
-   **interval**: periodic

 |
|PageCount|Integer|1| The number of returned pages.

 |
|PageSize|Integer|20| The number of entries returned per page.

 |
|RequestId|String|B92696EA-44DE-4DE4-B3B7-07655394DC7C| The ID of the request.

 |
|TotalCount|Integer|4| The number of returned scan tasks.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

/? Action=DescribeScans
&CurrentPage=1
&Lang=zh
&PageSize=20
&ScanType=vuln
&Search=***. ***.net
&SourceIp=1.2.3.4
&StatusList.1=["finished"]
&TriggerType=date
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeScans>
	  <requestId>B92696EA-44DE-4DE4-B3B7-07655394DC7C</requestId>
	  <data>
		    <PageCount>1</PageCount>
		    <Count>3</Count>
		    <TotalCount>3</TotalCount>
		    <PageSize>20</PageSize>
		    <CurrentPage>1</CurrentPage>
		    <List>
			      <Name>test_0710-3</Name>
			      <RefJobId>65084125-edc6-4ef3-931f-c3e87945631e</RefJobId>
			      <Status>finished</Status>
			      <ScanType>vuln</ScanType>
			      <EndDate>1531191010000</EndDate>
			      <RunPercent>100</RunPercent>
			      <StartDate>1531190450000</StartDate>
			      <ReportUrl>http://***.com/VUL_REPORT/d3ba039d-24cf-46e3-8ffb-ee56d8de40b0?Expires=1533555431&amp;OSSAccessKeyId=FGV18akrKbiBvLIU&amp;Signature=CmFMLzRIFOqETWWqj01mYpkKZIo%3D</ReportUrl>
			      <FlowName>skynet</FlowName>
			      <TriggerType>date</TriggerType>
			      <Targets>***. ***.net</Targets>
			      <ScanAll>0</ScanAll>
			      <ScanId>2018071010384940572</ScanId>
		    </List>
		    <List>
			      <Name>test_0710-2</Name>
			      <RefJobId>5c2d86bf-ace4-4c62-86e0-63f0b1e1413b</RefJobId>
			      <Status>finished</Status>
			      <ScanType>vuln</ScanType>
			      <EndDate>1531189680000</EndDate>
			      <RunPercent>100</RunPercent>
			      <StartDate>1531189151000</StartDate>
			      <ReportUrl>http://***.com/VUL_REPORT/29e66729-d571-489d-bc23-9d4cacf9e283?Expires=1533555431&amp;OSSAccessKeyId=FGV18akrKbiBvLIU&amp;Signature=x0BVqK%2B4BpKfZkGzYSaKJAWFLB4%3D</ReportUrl>
			      <FlowName>skynet</FlowName>
			      <TriggerType>date</TriggerType>
			      <Targets>***. ***.net</Targets>
			      <ScanAll>0</ScanAll>
			      <ScanId>2018071010171127450</ScanId>
		    </List>
		    <List>
			      <Name>test_0709-7</Name>
			      <RefJobId>6e504749-3ddc-47b5-a1e8-4e772a784122</RefJobId>
			      <Status>finished</Status>
			      <ScanType>vuln</ScanType>
			      <EndDate>1531139501000</EndDate>
			      <RunPercent>100</RunPercent>
			      <StartDate>1531138568000</StartDate>
			      <ReportUrl>http://***.com/VUL_REPORT/1a4415a0-ac30-4240-b6ae-7fe137152bdb?Expires=1533555431&amp;OSSAccessKeyId=FGV18akrKbiBvLIU&amp;Signature=WJ%2B5TWNQJ6CRshuGvFPPnvBifZc%3D</ReportUrl>
			      <FlowName>skynet</FlowName>
			      <TriggerType>date</TriggerType>
			      <Targets>***. ***.net</Targets>
			      <ScanAll>0</ScanAll>
			      <ScanId>2018070920140740337</ScanId>
		    </List>
	  </data>
	  <code>200</code>
	  <success>true</success>
    </DescribeScans>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"B92696EA-44DE-4DE4-B3B7-07655394DC7C",
	"data":{
		"PageCount":1,
		"Count":3,
		"TotalCount":3,
		"PageSize":20,
		"List":[
			{
				"ScanType":"vuln",
				"Name":"test_0710-3",
				"RefJobId":"65084125-edc6-4ef3-931f-c3e87945631e",
				"Status":"finished",
				"EndDate":1531191010000,
				"RunPercent":100,
				"StartDate":1531190450000,
				"ReportUrl":"http://***.com/VUL_REPORT/d3ba039d-24cf-46e3-8ffb-ee56d8de40b0?Expires=1533555431&OSSAccessKeyId=FGV18akrKbiBvLIU&Signature=CmFMLzRIFOqETWWqj01mYpkKZIo%3D",
				"FlowName":"skynet",
				"TriggerType":"date",
				"Targets":[
					"***. ***.net"
				],
				"ScanAll":0,
				"ScanId":"2018071010384940572"
			},
			{
				"ScanType":"vuln",
				"Name":"test_0710-2",
				"RefJobId":"5c2d86bf-ace4-4c62-86e0-63f0b1e1413b",
				"Status":"finished",
				"EndDate":1531189680000,
				"RunPercent":100,
				"StartDate":1531189151000,
				"ReportUrl":"http://***.com/VUL_REPORT/29e66729-d571-489d-bc23-9d4cacf9e283?Expires=1533555431&OSSAccessKeyId=FGV18akrKbiBvLIU&Signature=x0BVqK%2B4BpKfZkGzYSaKJAWFLB4%3D",
				"FlowName":"skynet",
				"TriggerType":"date",
				"Targets":[
					"***. ***.net"
				],
				"ScanAll":0,
				"ScanId":"2018071010171127450"
			},
			{
				"ScanType":"vuln",
				"Name":"test_0709-7",
				"RefJobId":"6e504749-3ddc-47b5-a1e8-4e772a784122",
				"Status":"finished",
				"EndDate":1531139501000,
				"RunPercent":100,
				"StartDate":1531138568000,
				"ReportUrl":"http://***.com/VUL_REPORT/1a4415a0-ac30-4240-b6ae-7fe137152bdb?Expires=1533555431&OSSAccessKeyId=FGV18akrKbiBvLIU&Signature=WJ%2B5TWNQJ6CRshuGvFPPnvBifZc%3D",
				"FlowName":"skynet",
				"TriggerType":"date",
				"Targets":[
					"***. ***.net"
				],
				"ScanAll":0,
				"ScanId":"2018070920140740337"
			}
		],
		"CurrentPage":1
	},
	"code":200,
	"success":true
}
```

## Error codes {#section_67y_rev_jnl .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

