# GenerateVulReport {#doc_api_avds_GenerateVulReport .reference}

You can call this operation to generate a report for the task instance.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=GenerateVulReport&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|GenerateVulReport|The operation that you want to perform. Set the value to GenerateVulReport.

 |
|TaskIds.N|RepeatList|Yes|111|The IDs of task instances for which reports are generated.

 |
|Lang|String|No|zh|The language in which the responses are returned.

 -   **zh**: Chinese
-   **en**: English

 |
|SourceIp|String|No|1.2.3.4|The source IP address of the request.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|6D584A17-4DA1-4CFD-BB31-\*\*\*\*\*\*|The ID of the request.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=GenerateVulReport
&TaskIds.1=111
&TaskIds.2=112
&SourceIp=
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<GenerateVulReport>
      <code>200</code>
      <requestId>6D584A17-4DA1-4CFD-BB31-******</requestId>
      <success>true</success>
</GenerateVulReport>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"6D584A17-4DA1-4CFD-BB31-******",
	"code":"200",
	"success":true
}
```

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

