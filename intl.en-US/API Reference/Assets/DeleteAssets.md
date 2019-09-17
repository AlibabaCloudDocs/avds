# DeleteAssets {#doc_api_avds_DeleteAssets .reference}

You can call this operation to delete assets.

 **You can call this operation to delete assets that do not need vulnerability scan.** 

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DeleteAssets&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DeleteAssets|The operation that you want to perform. Set the value to DeleteAssets.

 |
|AssetIds.N|RepeatList|Yes|\['a.aliyun.com', 'b.aliyun.com'\]|Specifies asset N to be deleted.

 |
|SourceIp|String|No|1.2.3.4|The source IP address of the request.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|0C992F5D-8568-41B4-9685-05C0DAEAE9D7|The ID of the request.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DeleteAssets
&Assets.1=['a.aliyun.com']
&Assets.2=['b.aliyun.com']
&SourceIp=
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DeleteAssets>
      <code>200</code>
      <requestId>0C992F5D-8568-41B4-9685-05C0DAEAE9D7</requestId>
      <success>true</success>
</DeleteAssets>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"0C992F5D-8568-41B4-9685-05C0DAEAE9D7",
	"code":"200",
	"success":true
}
```

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

