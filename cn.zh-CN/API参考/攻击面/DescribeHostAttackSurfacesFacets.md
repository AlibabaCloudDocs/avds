# DescribeHostAttackSurfacesFacets {#doc_api_avds_DescribeHostAttackSurfacesFacets .reference}

调用DescribeHostAttackSurfacesFacets接口，查询任务实例对应攻击面数据项中的主机攻击面统计信息。

调用DescribeHostAttackSurfacesFacets接口，可查询任务实例对资产进行扫描时，获取的攻击面数据项中的主机攻击面统计信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeHostAttackSurfacesFacets&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeHostAttackSurfacesFacets|系统规定参数。取值：DescribeHostAttackSurfacesFacets。

 |
|Host|String|是|1.2.3.4|主机名。获取指定主机下数据。

 |
|TaskId|Integer|是|123456|任务ID。获取指定任务ID数据。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|CrawlerRequests|Integer|30|爬虫流量数量。

 |
|Hosts|Integer|10|主机数量。

 |
|Ports|Integer|10|端口数量。

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795|返回结果的请求ID。

 |
|WebPaths|Integer|10|Web路径数量。

 |
|WebTechs|Integer|10|Web应用数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeHostAttackSurfacesFacets
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeHostAttackSurfacesFacets>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <Facets>
			      <CrawlerRequests>0</CrawlerRequests>
			      <Ports>304</Ports>
			      <WebPaths>14</WebPaths>
			      <WebServers>14</WebServers>
			      <WebTechs>2</WebTechs>
		    </Facets>
		    <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  </data>
    </DescribeHostAttackSurfacesFacets>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
		"Facets":{
			"CrawlerRequests":0,
			"WebPaths":14,
			"WebServers":14,
			"WebTechs":2,
			"Ports":304
		}
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

