# DescribeUserTags {#doc_api_avds_DescribeUserTags .reference}

You can call this operation to query all tags of your assets.

You can call this operation to query all tags of your assets.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeUserTags&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeUserTags|The operation that you want to perform. Set the value to DescribeUserTags.

 |
|CurrentPage|Integer|No|20|The number of the page to return.

 |
|Lang|String|No|zh|The language in which the responses are returned.

 -   **zh**: Chinese
-   **en**: English

 |
|PageSize|Integer|No|2|The number of entries to return on each page.

 |
|Search|String|No|test. \*\*.com|The search information by which to filter tags of assets.

 |
|SourceIp|String|No|1.2.3.4|The source IP address of the request.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Count|Integer|25|The number of entries returned on the current page.

 |
|CurrentPage|Integer|3|The current page number.

 |
|List| | |The list of returned tags.

 |
|AssetCount|Integer|200|The number of returned assets under the tag.

 |
|TagKey|String|tag1|The name of the returned tag.

 |
|PageCount|Integer|5|The total number of returned pages.

 |
|PageSize|Integer|30|The number of entries returned on each page.

 |
|RequestId|String|0C992F5D-8568-41B4-9685-05C0DAEAE9D7|The ID of the request.

 |
|TotalCount|Integer|60|The total number of returned tags.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DescribeUserTags
&SourceIp=
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeUserTags>
      <code>200</code>
      <requestId>0C992F5D-8568-41B4-9685-05C0DAEAE9D7</requestId>
      <success>true</success>
      <data>
            <List>
                  <TagKey>mytag</TagKey>
                  <AssetCount>1</AssetCount>
            </List>
      </data>
</DescribeUserTags>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"0C992F5D-8568-41B4-9685-05C0DAEAE9D7",
	"data":{
		"List":[
			{
				"TagKey":"mytag",
				"AssetCount":1
			}
		]
	},
	"code":"200",
	"success":true
}
```

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

