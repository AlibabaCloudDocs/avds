# DescribeWebTechs {#doc_api_avds_DescribeWebTechs .reference}

You can also call this operation to query the Web applications that are included in the corresponding attack surface of the task instance.

You can call this operation to query the Web applications that are included in the corresponding attack surface when the asset is scanned in the task instance.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeWebTechs&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeWebTechs|The operation that you want to perform. Set the value to DescribeWebTechs.

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
|Index|Integer|1|The index number of the returned record.

 |
|Name|String|Apache|The IP address.

 |
|PoweredBy|String|Java|The programming language.

 |
|Server|String|Apache|The Web server.

 |
|Title|String|Open Platform-Homepage|The title of the Web service.

 |
|URL|String|http://\*\*\*.com|The URL of the application.

 |
|UpdatedAt|Long|1561392000000|The timestamp of the scan.

 |
|Version|String|1.7|The version information.

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795|The ID of the request.

 |
|Total|Integer|120|The number of returned entries.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DescribeWebTechs
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeWebTechs>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <Records>
			      <Index>1</Index>
			      <Name>Apache</Name>
			      <URL>https://1.2.3.4:443/</URL>
			      <Version>1.7.2</Version>
			      <Server>Apache</Server>
			      <PoweredBy></PoweredBy>
			      <Title>CPOSOpenPlatform-Homepage</Title>
			      <UpdatedAt>1561392000000</UpdatedAt>
		    </Records>
		    <Records>
			      <Index>2</Index>
			      <Name>Apache</Name>
			      <URL>https://1.2.3.4:443/</URL>
			      <Version>1.7.2</Version>
			      <Server>Apache</Server>
			      <PoweredBy></PoweredBy>
			      <Title>CPOSOpenPlatform-Homepage</Title>
			      <UpdatedAt>1561392000000</UpdatedAt>
		    </Records>
	  </data>
</DescribeWebTechs>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"Records":[
			{
				"UpdatedAt":1561392000000,
				"Name":"Apache",
				"Index":1,
				"Version":"1.7.2",
				"URL":"https://1.2.3.4:443/",
				"Title":"CPOSOpenPlatform-Homepage",
				"Server":"Apache",
				"PoweredBy":""
			},
			{
				"UpdatedAt":1561392000000,
				"Name":"Apache",
				"Index":2,
				"Version":"1.7.2",
				"URL":"https://1.2.3.4:443/",
				"Title":"CPOSOpenPlatform-Homepage",
				"Server":"Apache",
				"PoweredBy":""
			}
		]
	},
	"code":"200",
	"success":true
}
```

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

