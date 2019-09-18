# DescribePorts {#doc_api_avds_DescribePorts .reference}

You can call this operation to query the service information of the ports that are included in the corresponding attack surface of the task instance.

You can call this operation to query the service information of the ports that are included in the corresponding attack surface when the asset is scanned in the task instance.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribePorts&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribePorts| The operation that you want to perform. Set the value to DescribePorts.

 |
|TaskId|Integer|Yes|12345| The ID of the task. You can specify this parameter to obtain the data of the specific task.

 |
|Asset|String|No|foo.com| The name of the asset. You can specify this parameter to query detection data of the specific asset.

 |
|CurrentPage|Integer|No|1| The number of the page to return. Default value: 1.

 |
|PageSize|Integer|No|10| The number of entries to return on each page. Default value: 10. This is the maximum value.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Records| | | The list of returned records.

 |
|Fingerprint|String|HTTP Apache| The port fingerprint.

 |
|IP|String|1.2.3.4| The IP address.

 |
|Index|Integer|1| The index number of the returned record.

 |
|Port|String|843| The port number.

 |
|Product|String|Apache Tomcat/\*\*\*\*\*\* 1.1| The name of the service.

 |
|Protocol|String|tcp| The network protocol.

 |
|Service|String|http| The type of the service.

 |
|UpdatedAt|Long|1561392000000| The timestamp of the scan.

 |
|Version|String|1.1| The version information.

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795| The ID of the request.

 |
|Total|Integer|120| The number of returned entries.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DescribePorts
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribePorts>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <Total>120</Total>
		    <Records>
			      <Index>1</Index>
			      <IP>1.2.3.4</IP>
			      <Protocol>tcp</Protocol>
			      <Port>843</Port>
			      <Service>http</Service>
			      <Product>Apache Tomcat/Coyote JSP engine 1.1</Product>
			      <Version>1.1</Version>
			      <Fingerprint></Fingerprint>
			      <UpdatedAt>1561392000000</UpdatedAt>
		    </Records>
		    <Records>
			      <Index>2</Index>
			      <IP>1.2.3.5</IP>
			      <Protocol>tcp</Protocol>
			      <Port>843</Port>
			      <Service>http</Service>
			      <Product>Apache Tomcat/Coyote JSP engine 1.1</Product>
			      <Version>1.1</Version>
			      <Fingerprint></Fingerprint>
			      <UpdatedAt>1561392000000</UpdatedAt>
		    </Records>
	  </data>
</DescribePorts>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"Records":[
			{
				"UpdatedAt":1561392000000,
				"Service":"http",
				"Port":"843",
				"Index":1,
				"Product":"Apache Tomcat/Coyote JSP engine 1.1",
				"IP":"1.2.3.4",
				"Version":"1.1",
				"Protocol":"tcp",
				"Fingerprint":""
			},
			{
				"UpdatedAt":1561392000000,
				"Service":"http",
				"Port":"843",
				"Index":2,
				"Product":"Apache Tomcat/Coyote JSP engine 1.1",
				"IP":"1.2.3.5",
				"Version":"1.1",
				"Protocol":"tcp",
				"Fingerprint":""
			}
		],
		"Total":120
	},
	"code":"200",
	"success":true
}
```

## Error codes {#section_xom_22k_rwk .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

