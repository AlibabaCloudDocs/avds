# DescribeScans {#doc_api_avds_DescribeScans .reference}

调用本接口获取扫描任务列表。

该API可以分页查询所有扫描任务列表，查看扫描进度等信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeScans&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeScans|系统规定参数。取值：DescribeScans。

 |
|CurrentPage|Integer|否|1|指定待查询的扫描任务列表当前页码。

 |
|Lang|String|否|zh|指定返回任务列表的语言环境。可选：

 -   **zh**：中文
-   **en**：英文

 |
|PageSize|Integer|否|20|指定待查询的扫描任务列表每页显示数据条数。

 |
|ScanId|String|否|2019031816494923023|指定待查询扫描任务的任务ID。

 |
|ScanType|String|否|vuln|指定待查询扫描任务的扫描类型。 可选：

 -   **vuln**：漏洞类型
-   **content**：内容风险

 |
|Search|String|否|\*\*\*.\*\*\*.net|指定待查询扫描任务的搜索条件（任务名称、IP、域名）。

 |
|SourceIp|String|否|1.2.3.4|指定访问者源IP地址。

 |
|StatusList.N|RepeatList|否|\["finished"\]|指定待查询任务的扫描状态。

 -   **waiting**：等待中
-   **finished**：已完成
-   **running**：运行中
-   **aborted**：已中止
-   **invalid**：已无效
-   **disabled**：已失败

 |
|TriggerType|String|否|date|指定待查询扫描任务的触发类型。 可选

 -   **date**：单次任务
-   **interval**：周期任务

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|3|返回任务列表的扫描任务数量。

 |
|CurrentPage|Integer|1|返回任务列表的当前页码。

 |
|List| | |扫描任务列表。

 |
|CronActive|String|1|任务的调度状态。

 -   **1**：活跃，表示任务可调度
-   **0**：无效，表示任务不可调度

 |
|EndDate|Long|212212000000|返回任务列表中的任务扫描结束时间。

 |
|FlowName|String|skynet\_vul\_scan|返回任务列表中任务的漏洞扫描模式。

 -   **assets**：资产模式
-   **general**：标准模式
-   **skynet\_vul\_scan**：深度模式

 |
|IndexIntervalInMinute|Integer|5|返回任务列表中的任务首页检测间隔时间。

 |
|Interval|Integer|10|返回任务列表中扫描任务的扫描间隔。

 |
|JobStatistics|String|running|任务实例的统计情况。

 -   **1**：running，表示扫描任务运行中
-   **2**：finished，表示扫描任务已完成
-   **3**：aborted，表示扫描任务已停止

 |
|KeyWords| |65084125-edc6-4ef3-931f-c3e87945631e|附加词库的ID。

 |
|LastSheduleDate|Long|1111000000|上次调度任务的时间戳。

 |
|Name|String|test\_0710-3|返任务列表中的任务名称。

 |
|NextRunDate|Long|1212100000|返回任务列表中显示的各任务下次扫描预计开始时间。

 |
|Period|String|minute|返回任务列表中个任务的扫描周期。

 -   **minute**：每分钟
-   **hour**：每小时
-   **day**：每天
-   **week**：每周
-   **month**：每月

 |
|RefJobId|String|65084125-edc6-4ef3-931f-c3e87945631e|返回任务列表中个任务所关联扫描任务的ID。

 |
|ReportUrl|String|http://\*\*\*.com|返回任务列表中各扫描任务生成的任务报告链接。

 |
|RunPercent|Float|100.0|返回任务列表中显示的运行中扫描任务的扫描进度百分比。

 |
|RuntimeEnd|String|1545972690000|返回任务列表中扫描任务的扫描开始时间。

 |
|RuntimeStart|String|1545972690000|返回任务列表中扫描任务的扫描结束时间。

 |
|ScanAll|Integer|1|返回任务列表中显示是否扫描了全部资产。

 |
|ScanId|String|2018071010171127450|返回任务列表中对应扫描任务的任务ID。

 |
|ScanType|String|vuln|任务列表中显示的任务扫描类型。

 -   **vuln**：漏洞类型
-   **content**：内容风险

 |
|SiteIntervalInDay|Integer|1|任务列表中显示的对应任务在全站检测的间隔（天）时间。

 |
|StartDate|Long|111122200000|返回任务列表中个任务的开始时间。

 |
|Status|String|running|返回任务列表中各任务的扫描状态。

 -   **waiting**：等待中
-   **finished**：已完成
-   **running**：运行中
-   **aborted**：已暂停
-   **invalid**：已无效
-   **disabled**：已禁用

 |
|Targets| |\["demo.testfire.net"\]|返回任务列表中的扫描目标（IP/域名/子域名）名称。

 |
|TargetsOriginal| |testtag|创建扫描任务时，扫描目标的原始内容，即扫描资产的分组标签。

 |
|TriggerType|String|date|返回任务列表中的各任务触发类型。

 -   **date**：单次任务
-   **interval** ：周期任务

 |
|PageCount|Integer|1|返回任务列表的页数。

 |
|PageSize|Integer|20|返回任务列表每页显示数据的条数。

 |
|RequestId|String|B92696EA-44DE-4DE4-B3B7-07655394DC7C|返回结果的请求ID。

 |
|TotalCount|Integer|4|返回任务列表的总任务条数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

/?Action=DescribeScans
&CurrentPage=1
&Lang=zh
&PageSize=20
&ScanType=vuln
&Search=***.***.net
&SourceIp=1.2.3.4
&StatusList.1=["finished"]
&TriggerType=date
&<公共请求参数>

```

正常返回示例

`XML` 格式

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
			      <Targets>***.***.net</Targets>
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
			      <Targets>***.***.net</Targets>
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
			      <Targets>***.***.net</Targets>
			      <ScanAll>0</ScanAll>
			      <ScanId>2018070920140740337</ScanId>
		    </List>
	  </data>
	  <code>200</code>
	  <success>true</success>
    </DescribeScans>
```

`JSON` 格式

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
					"***.***.net"
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
					"***.***.net"
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
					"***.***.net"
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

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

