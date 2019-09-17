# AddAssetTags {#doc_api_avds_AddAssetTags .reference}

You can call this operation to add tags for assets.

You can call this operation to add tags for multiple assets or add multiple tags for one asset.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=AddAssetTags&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|AddAssetTags|The operation that you want to perform. Set the value to AddAssetTags.

 |
|Assets.N|RepeatList|Yes|\['a.aliyun.com', 'b.aliyun.com'\]|Specifies asset N to add tags to.

 |
|Lang|String|No|zh|The language in which the responses are returned.

 -   **zh**: Chinese
-   **en**: English

 |
|SourceIp|String|No|1.2.3.4|The source IP address of the request.

 |
|Tags.N|RepeatList|No|\['tag1','tag2'\]|Specifies tag N to be added.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|RequestId|String|0C992F5D-8568-41B4-9685-05C0DAEAE9D7|The ID of the request.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=AddAssetTags
&Assets.1='a.aliyun.com'
&Assets.2='b.aliyun.com'
&Tags.1='tag1'
&Tags.2='tag2'
&SourceIp=
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<AddAssetTags>
      <code>200</code>
      <requestId>0C992F5D-8568-41B4-9685-05C0DAEAE9D7</requestId>
      <success>true</success>
</AddAssetTags>
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

