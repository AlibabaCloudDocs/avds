# DescribeDomainAttackSurfacesFacets {#doc_api_avds_DescribeDomainAttackSurfacesFacets .reference}

You can call this operation to query the statistics of the domain names that are included in the corresponding attack surface of the task instance.

You can call this operation to query the statistics of the domain names that are included in the corresponding attack surface when the asset is scanned in the task instance.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeDomainAttackSurfacesFacets&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeDomainAttackSurfacesFacets|The operation that you want to perform. Set the value to DescribeDomainAttackSurfacesFacets.

 |
|Domain|String|Yes|test.com|The domain name.

 |
|TaskId|Integer|Yes|12345|The ID of the task. You can specify this parameter to obtain the data of the specific task.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CrawlerRequests|Integer|30|The number of crawler requests.

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795|The ID of the request.

 |
|WebPaths|Integer|10|The number of Web paths.

 |
|WebServers|Integer|10|The number of Web servers.

 |
|WebTechs|Integer|10|The number of Web applications.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DescribeDomainAttackSurfacesFacets
&<Common request parameters>

```

Sample success responses

`XML` format

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

`JSON` format

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

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

