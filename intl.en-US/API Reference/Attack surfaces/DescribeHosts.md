# DescribeHosts {#doc_api_avds_DescribeHosts .reference}

You can also call this operation to query the list of hosts that are included in the corresponding attack surface of the task instance.

You can call this operation to query the list of hosts that are included in the corresponding attack surface when the asset is scanned in the task instance.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeHosts&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeHosts|The operation that you want to perform. Set the value to DescribeHosts.

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
|Hostname|String|foo-hostname|The name of the host.

 |
|IP|String|1.2.3.4|The IP address.

 |
|Index|Integer|1|The index number of the returned record.

 |
|IsUp|String|Up|Indicates whether the machine is operating.

 -   **Up**: operating
-   **Down**: shutdown

 |
|OS|String|Windows|The type of the operating system.

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

http(s)://[Endpoint]/? Action=DescribeHosts
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeHosts>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <Total>120</Total>
		    <Records>
			      <Index>1</Index>
			      <IP>1.2.3.4</IP>
			      <Hostname></Hostname>
			      <OS>AVtech Room Alert 26W environmental monitor </OS>
			      <IsUp>Up</IsUp>
			      <CreatedAt>1561392000000</CreatedAt>
		    </Records>
		    <Records>
			      <Index>2</Index>
			      <IP>1.2.3.4</IP>
			      <Hostname></Hostname>
			      <OS>AVtech Room Alert 26W environmental monitor </OS>
			      <IsUp>Up</IsUp>
			      <CreatedAt>1561392000000</CreatedAt>
		    </Records>
	  </data>
</DescribeHosts>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"Records":[
			{
				"Index":1,
				"IsUp":"Up",
				"IP":"1.2.3.4",
				"OS":"AVtech Room Alert 26W environmental monitor ",
				"CreatedAt":1561392000000,
				"Hostname":"foo-hostname"
			},
			{
				"Index":2,
				"IsUp":"Up",
				"IP":"1.2.3.4",
				"OS":"AVtech Room Alert 26W environmental monitor ",
				"CreatedAt":1561392000000,
				"Hostname":"foo-hostname"
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

