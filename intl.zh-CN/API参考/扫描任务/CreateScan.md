# CreateScan

调用CreateScan创建漏洞扫描任务和内容检测任务。

## 调试

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=CreateScan&type=RPC&version=2017-11-29)

## 请求参数

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|CreateScan|要执行的操作。取值：**CreateScan**。 |
|Name|String|是|单次任务|设置扫描任务名称。 |
|ScanType|String|是|vuln|指定扫描任务的扫描资产的检测类型。取值：

 -   **vuln**：漏洞类型
-   **content**：内容风险
-   **asset**：资产发现 |
|SourceIp|String|否|1.2.3.4|指定访问者源IP地址。 |
|Targets.N|RepeatList|否|\["\*\*\*.testfire.net"\]|指定待扫描目标资产列表。 |
|ScanAll|Integer|否|1|扫描所有资产。 |
|FlowName|String|否|assets|指定扫描任务的扫描模式。取值：

 -   **assets**：资产模式
-   **general**：标准模式
-   **skynet\_vul\_scan**：深度模式 |
|EnableAssetDiscover|Integer|否|1|漏洞扫描任务是否开启资产发现。取值：

 -   **0**：开启
-   **1**：不开启 |
|TriggerType|String|否|date|指定扫描任务的触发类型。取值：

 -   **date**：单次任务
-   **interval**：周期任务 |
|Period|String|否|day|指定扫描任务的扫描周期。取值：

 -   **day**：每天一次
-   **week**：每周一次
-   **month**：每月一次 |
|Interval|Integer|否|5|指定扫描任务的扫描间隔，即距离上一次任务扫描的时间。 |
|StartDate|Long|否|111122200000|指定扫描任务执行的开始时间。 |
|EndDate|Long|否|212212000000|指定扫描任务执行的结束时间。 |
|Qps|Integer|否|16|指定扫描任务的扫描速度。取值：

 -   **16**：慢速
-   **32**：常速
-   **64**：快速 |
|RuntimeStart|String|否|00:00:00|指定扫描任务扫描开始的时间。 |
|RuntimeEnd|String|否|08:00:00|指定扫描任务扫描结束的时间 。 |
|IndexIntervalInMinute|Integer|否|5|首页检测间隔（分钟）。取值：

 -   **5**：间隔5分钟
-   **30**：间隔30分钟
-   **60**：间隔60分钟 |
|SiteIntervalInDay|Integer|否|1|全站检测间隔（天）。取值：

 -   **1**：每1天一次
-   **7**：每7天一次 |
|EnableAssetLoginScan|Integer|否|1|漏洞扫描任务是否开启登录扫描。取值：

 -   0：不开启
-   1：开启 |
|TargetAssetTags.N|RepeatList|否|\[\]|指定待扫描目标资产的标签列表。 |
|KeyWords.N|RepeatList|否|\[\]|附加词库列表。 |
|URLs.N|RepeatList|否|https://www.aliyun.com|Web路径列表。 |
|OrgIds.N|RepeatList|否|\[1, 2, 3\]|组织机构ID列表。 |

## 返回数据

|名称|类型|示例值|描述|
|--|--|---|--|
|Data|String|\{ "Data": "2018080617471590979" \}|返回的结果数据。 |
|RequestId|String|76F297E0-D4C2-442A-AEAD-AABA97975060|返回结果的请求ID。 |

## 示例

请求示例

```
http(s)://[Endpoint]/?Action=CreateScan
&FlowName=assets
&Name=单次任务
&Qps=16
&RuntimeEnd=08:00:00
&RuntimeStart=00:00:00 
&ScanType=vuln
&StartDate=111122200000
&TriggerType=date
&<公共请求参数>
```

正常返回示例

`XML` 格式

```
<CreateScanResponse>
	  <requestId>76F297E0-D4C2-442A-AEAD-AABA97975060</requestId>
	  <data>
		    <Data>2018080617471590979</Data>
	  </data>
	  <code>200</code>
	  <success>true</success>
</CreateScanResponse>
```

`JSON` 格式

```
{
  "requestId": "76F297E0-D4C2-442A-AEAD-AABA97975060",
  "data": {
    "Data": "2018080617471590979"
  },
  "code": 200,
  "success": true
}
```

## 错误码

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

