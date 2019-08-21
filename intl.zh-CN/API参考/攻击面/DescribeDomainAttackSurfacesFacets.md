# DescribeDomainAttackSurfacesFacets {#doc_api_avds_DescribeDomainAttackSurfacesFacets .reference}

调用DescribeDomainAttackSurfacesFacets接口，查询任务实例对应攻击面数据项中的域名攻击面统计信息。

调用DescribeDomainAttackSurfacesFacets接口，可查询任务实例对资产进行扫描时，获取的攻击面数据项中的域名攻击面统计信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeDomainAttackSurfacesFacets&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeDomainAttackSurfacesFacets|系统规定参数。取值：DescribeDomainAttackSurfacesFacets。

 |
|Domain|String|是|test.com|域名。

 |
|TaskId|Integer|是|12345|任务ID。获取指定任务ID数据。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|CrawlerRequests|Integer|30|爬虫流量数量。

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795|返回结果的请求ID。

 |
|WebPaths|Integer|10|Web路径数量。

 |
|WebServers|Integer|10|Web服务器数量。

 |
|WebTechs|Integer|10|Web应用数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeDomainAttackSurfacesFacets
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeDomainAttackSurfacesFacets>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <CrawlerRequests>20</CrawlerRequests>
		    <WebPaths>22</WebPaths>
		    <WebServers>0</WebServers>
		    <WebTechs>0</WebTechs>
	  </data>
</DescribeDomainAttackSurfacesFacets>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"CrawlerRequests":20,
		"WebPaths":22,
		"WebServers":0,
		"WebTechs":0
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

