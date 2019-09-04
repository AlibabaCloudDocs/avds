# DescribeAttackSurfacesFacets {#doc_api_avds_DescribeAttackSurfacesFacets .reference}

调用DescribeAttackSurfacesFacets查询任务实例攻击面数据统计信息。

调用DescribeAttackSurfacesFacets接口，可查询任务实例对资产进行扫描时，获取的任务实例的攻击面统计信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeAttackSurfacesFacets&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAttackSurfacesFacets|系统规定参数。取值：DescribeAttackSurfacesFacets。

 |
|TaskId|Integer|是|12345|任务ID。获取指定任务ID数据。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|CrawlerRequests|Integer|30|爬虫流量数量。

 |
|DNSMap|Integer|10|DNS解析记录数量。

 |
|Domains|Integer|10|域名数量。

 |
|Hosts|Integer|10|主机数量。

 |
|Ports|Integer|10|端口数量。

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795|返回结果的请求ID。

 |
|Subdomains|Integer|10|子域名数量。

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

http(s)://[Endpoint]/?Action=DescribeAttackSurfacesFacets
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeAttackSurfacesFacets>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <Domains>10</Domains>
		    <Subdomains>20</Subdomains>
		    <DNSMap>20</DNSMap>
		    <Hosts>40</Hosts>
		    <Ports>30</Ports>
		    <WebTechs>40</WebTechs>
		    <WebServers>30</WebServers>
		    <WebPaths>20</WebPaths>
		    <CrawlerRequests>40</CrawlerRequests>
	  </data>
</DescribeAttackSurfacesFacets>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"DNSMap":20,
		"CrawlerRequests":40,
		"WebPaths":20,
		"WebServers":30,
		"Subdomains":20,
		"WebTechs":40,
		"Hosts":40,
		"Domains":10,
		"Ports":30
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

