# DescribeCrawlerRequests {#doc_api_avds_DescribeCrawlerRequests .reference}

You can call this operation to query the crawler traffic data about the corresponding attack surface of the task instance.

You can call this operation to query the crawler traffic data about the corresponding attack surface when the asset is scanned in the task instance.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeCrawlerRequests&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeCrawlerRequests|The operation that you want to perform. Set the value to DescribeCrawlerRequests.

 |
|TaskId|Integer|Yes|12345|The ID of the task. You can specify this parameter to obtain the data of the specific task.

 |
|Asset|String|No|foo.com|The name of the asset. You can specify this parameter to query detection data of the specific asset.

 |
|CurrentPage|Integer|No|1|The number of the page to return. Default value: 1.

 |
|PageSize|Integer|No|10|The number of entries to return on each page. Default value: 10. This is the maximum value.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Records| | |The list of returned records.

 |
|Cookies|String|\{"JSESSIONID": "3A6FA438DDB20E860F64FB4F57F315DC"\}|Cookies

 |
|Data|String|foo=bar|The request body.

 |
|Index|Integer|1|The index number of the returned record.

 |
|Method|String|GET|The request method.

 |
|URL|String|http:///\*\*\*.com|The URL.

 |
|UpdatedAt|Long|1561392000000|The timestamp of the scan.

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795|The ID of the request.

 |
|Total|Integer|120|The number of returned entries.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DescribeCrawlerRequests
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeCrawlerRequests>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <Total>123</Total>
		    <Records>
			      <Index>1</Index>
			      <Method>GET</Method>
			      <URL>http://***. ***.com/user/login?username=admin</URL>
			      <Cookies>
				        <JSESSIONID>3A6FA438DDB20E860F64FB4F57F315DC</JSESSIONID>
			      </Cookies>
			      <Data></Data>
			      <UpdatedAt>1561392000000</UpdatedAt>
		    </Records>
		    <Records>
			      <Index>2</Index>
			      <Method>GET</Method>
			      <URL>http://***. ***.com/user/login?username=admin</URL>
			      <Cookies>
				        <JSESSIONID>3A6FA438DDB20E860F64FB4F57F315DC</JSESSIONID>
			      </Cookies>
			      <Data></Data>
			      <UpdatedAt>1561392000000</UpdatedAt>
		    </Records>
	  </data>
    </DescribeCrawlerRequests>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"Records":[
			{
				"UpdatedAt":1561392000000,
				"Data":"",
				"Cookies":{
					"JSESSIONID":"3A6FA438DDB20E860F64FB4F57F315DC"
				},
				"Index":1,
				"Method":"GET",
				"URL":"http://***. ***.com/user/login?username=admin"
			},
			{
				"UpdatedAt":1561392000000,
				"Data":"",
				"Cookies":{
					"JSESSIONID":"3A6FA438DDB20E860F64FB4F57F315DC"
				},
				"Index":2,
				"Method":"GET",
				"URL":"http://***. ***.com/user/login?username=admin"
			}
		],
		"Total":123
	},
	"code":"200",
	"success":true
}
```

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

