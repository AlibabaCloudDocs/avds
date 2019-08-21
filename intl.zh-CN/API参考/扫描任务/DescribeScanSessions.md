# DescribeScanSessions {#doc_api_avds_DescribeScanSessions .reference}

调用本接口获取扫描任务实例列表。

该API可以分页查询扫描任务调度产生的任务实例列表信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeScanSessions&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeScanSessions|系统规定参数。取值：DescribeScanSessions。

 |
|CurrentPage|Integer|否|3|指定返回结果的当前页码。

 |
|PageSize|Integer|否|20|指定返回结果的每页显示数据条数。

 |
|ScanId|String|否|66c07fa5-542b-47df-8501-e0401dc42d3e|指定查询特定扫描任务ID的实例列表。

 |
|Search|String|否|1.2.\*.\*|指定待查询实例的任务搜索字段。

 |
|SourceIp|String|否|1.2.3.4|指定访问源IP地址。

 |
|StatusList.N|RepeatList|否|waiting|指定待查询实例中子任务状态。

 -   **waiting**：等待中
-   **finished**：已完成
-   **running**：运行中
-   **aborted**：暂停

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|20|指定当前页显示数据条数。

 |
|CurrentPage|Integer|5|指定返回结果的当前页码。

 |
|List| | |返回的任务实例列表。

 |
|CreatedAt|Long|1565690460000|扫描创建时间。

 |
|FinishedAt|Long|1565690260000|扫描结束时间。

 |
|Interval|Integer|1|返回结果中任务的扫描间隔时间。

 |
|JobStatus|String|waiting|返回结果中子任务扫描状态。

 -   **waiting**：等待中
-   **finished**：已完成
-   **running**：运行中
-   **aborted**：已暂停

 |
|Name|String|test|返回结果中任务名称。

 |
|Period|String|hour|返回结果中各任务的扫描周期。

 -   **minute**：每分钟
-   **hour**：每小时
-   **day**：每天
-   **week**：每周
-   **month**：每月

 |
|ReportStatus|String|running|返回结果中各任务实例生成报表状态。

 -   **failed**：生成失败
-   **finished**：生成完成
-   **running**：生成中
-   **inexistent**：不存在

 |
|ReportUrl|String|http://\*\*\*.com|返回结果中个任务实例生成的报告链接。

 |
|RunPercent|Float|10.21|返回结果中各任务实例的扫描进度。

 |
|ScanId|String|c0065a11-fe41-44f4-a5d2-b921316ddb52|返回结果中各实例下子任务的任务ID。

 |
|Targets| |\[\]|返回结果中各任务实例下扫描目标（IP/域名/子域名）。

 |
|TaskId|Long|1236984|返回结果中各任务实例的ID。

 |
|TriggerType|String|date|返回结果中各任务实例下子任务的任务触发类型。

 -   **date**：单次任务
-   **interval** ：周期任务

 |
|PageCount|Integer|20|返回任务实例列表总页数。

 |
|PageSize|Integer|20|返回任务实例列表中每页显示数据总条数。

 |
|RequestId|String|F8955687-DDFC-4FE1-BC67-5C613657B8E5|返回结果的请求ID。

 |
|TotalCount|Integer|30|返回任务实例列表的实例总数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeScanSessions
&CurrentPage=1
&PageSize=20
&ScanId=1111
&Search=任务名
&SourceIp=111
&StatusList.1="finished"
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeScanSessions>
      <code>200</code>
      <requestId>F8955687-DDFC-4FE1-BC67-5C613657B8E5</requestId>
      <success>true</success>
      <data>
            <List>
                  <TaskId>11</TaskId>
                  <ScanId>11111</ScanId>
                  <JobStatus></JobStatus>
                  <CreatedAt>111212121</CreatedAt>
                  <FinishedAt>12121</FinishedAt>
                  <name></name>
                  <triggerType></triggerType>
                  <period></period>
                  <interval>1</interval>
                  <reportStatus></reportStatus>
                  <reportUrl>http://***.com</reportUrl>
            </List>
            <PageNumber>1</PageNumber>
            <PageSize>20</PageSize>
            <TotalCount>100</TotalCount>
      </data>
</DescribeScanSessions>
```

`JSON` 格式

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
				"name":"",
				"reportStatus":"",
				"JobStatus":"",
				"TaskId":11,
				"period":"",
				"triggerType":"",
				"targets":[],
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

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

