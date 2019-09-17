# DescribeDNSMap {#doc_api_avds_DescribeDNSMap .reference}

You can call this operation to query the DNS records that are included in the corresponding attack surface of the task instance.

You can call this operation to query the DNS records that are included in the corresponding attack surface when the asset is scanned in the task instance.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeDNSMap&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeDNSMap|The operation that you want to perform. Set the value to DescribeDNSMap.

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
|Domain|String|www.foo.com|The domain name.

 |
|Index|Integer|1|The index number of the returned record.

 |
|Record|String|1.2.3.4|The details about the DNS records.

 |
|Type|String|A|The type of the returned record.

 -   **A**: IP resolution
-   **CNAME**: host alias resolution

 |
|UpdatedAt|Long|1561392000000|The timestamp of the scan.

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795|The ID of the request.

 |
|Total|Integer|1000|The number of returned entries.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DescribeDNSMap
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeDNSMap>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <Total>120</Total>
		    <Records>
			      <Index>1</Index>
			      <Domain>www.foo.com</Domain>
			      <Record>1.2.3.4</Record>
			      <Type>A</Type>
			      <CreatedAt>1561392000000</CreatedAt>
		    </Records>
		    <Records>
			      <Index>2</Index>
			      <Domain>www.foo.com</Domain>
			      <Record>1.2.3.4</Record>
			      <Type>A</Type>
			      <CreatedAt>1561392000000</CreatedAt>
		    </Records>
	  </data>
</DescribeDNSMap>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"Records":[
			{
				"Index":1,
				"Record":"1.2.3.4",
				"Domain":"www.foo.com",
				"Type":"A",
				"CreatedAt":1561392000000
			},
			{
				"Index":2,
				"Record":"1.2.3.4",
				"Domain":"www.foo.com",
				"Type":"A",
				"CreatedAt":1561392000000
			}
		],
		"Total":120
	},
	"code":"200",
	"success":true
}
```

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

