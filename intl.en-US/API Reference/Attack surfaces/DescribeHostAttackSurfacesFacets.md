# DescribeHostAttackSurfacesFacets {#doc_api_avds_DescribeHostAttackSurfacesFacets .reference}

You can call this operation to query the statistics of hosts that are included in the corresponding attack surface of the task instance.

You can call this operation to query the statistics of hosts that are included in the corresponding attack surface when the asset is scanned in the task instance.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeHostAttackSurfacesFacets&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeHostAttackSurfacesFacets|The operation that you want to perform. Set the value to DescribeHostAttackSurfacesFacets.

 |
|Host|String|Yes|1.2.3.4|The name of the host. You can specify this parameter to obtain the data of the specific host.

 |
|TaskId|Integer|Yes|123456|The ID of the task. You can specify this parameter to obtain the data of the specific task.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|CrawlerRequests|Integer|30|The number of crawler requests.

 |
|Hosts|Integer|10|The number of hosts.

 |
|Ports|Integer|10|The number of ports.

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795|The ID of the request.

 |
|WebPaths|Integer|10|The number of Web paths.

 |
|WebTechs|Integer|10|The number of Web applications.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DescribeHostAttackSurfacesFacets
&<Common request parameters>

```

Sample success responses

`XML` format

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

`JSON` format

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

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

