# DescribeWebPaths {#doc_api_avds_DescribeWebPaths .reference}

You can call this operation to query the Web paths that are included in the corresponding attack surface of the task instance.

You can call this operation to query the Web paths that are included in the corresponding attack surface when the asset is scanned in the task instance.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeWebPaths&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeWebPaths|The operation that you want to perform. Set the value to DescribeWebPaths.

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
|Extension|String|png|The filename extension.

 |
|Index|Integer|1|The index number of the returned record.

 |
|Path|String|/themes/dist/images/test-123\*\*\*.png|The details about the Web path.

 |
|Site|String|http://1.2.3.4:88\*\*|The URL of the site.

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

http(s)://[Endpoint]/? Action=DescribeWebPaths
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeWebPaths>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <Records>
			      <Index>1</Index>
			      <Site>http://icourse. ******.com:8899</Site>
			      <Path>  /themes/dist/images/sg1-476744******.png</Path>
			      <Extension>png</Extension>
			      <CreatedAt>1561392000000</CreatedAt>
		    </Records>
		    <Records>
			      <Index>2</Index>
			      <Site>http://icourse. ******.com:88**</Site>
			      <Path>  /themes/dist/images/sg1-4767******.png</Path>
			      <Extension>png</Extension>
			      <CreatedAt>1561392000000</CreatedAt>
		    </Records>
	  </data>
</DescribeWebPaths>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"Records":[
			{
				"Extension":"png",
				"Site":"http://icourse. ******.com:8899",
				"Index":1,
				"CreatedAt":1561392000000,
				"Path":"  /themes/dist/images/sg1-476744******.png"
			},
			{
				"Extension":"png",
				"Site":"http://icourse. ******.com:88**",
				"Index":2,
				"CreatedAt":1561392000000,
				"Path":"  /themes/dist/images/sg1-4767******.png"
			}
		]
	},
	"code":"200",
	"success":true
}
```

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

