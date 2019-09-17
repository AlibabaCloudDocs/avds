# DescribeAssetsByTags {#doc_api_avds_DescribeAssetsByTags .reference}

You can call this operation to query the asset list under a specified tag.

You can call this operation to query assets under multiple tags.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeAssetsByTags&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeAssetsByTags|The operation that you want to perform. Set the value to DescribeAssetsByTags.

 |
|Tags.N|RepeatList|Yes|\['tag1', 'tag2'\]|Specifies tag N by which to return assets.

 |
|CurrentPage|Integer|No|2|The number of the page to return.

 |
|Lang|String|No|zh|The language in which the responses are returned.

 -   **zh**: Chinese
-   **en**: English

 |
|PageSize|Integer|No|20|The number of entries to return on each page.

 |
|Search|String|No|1.2.3.5|The information by which to query a specified asset.

 |
|SourceIp|String|No|1.2.3.4|The source IP address of the request.

 |
|Type|String|No|ip|The type of the asset to be queried. Valid values:

 -   **ip**: assets of the IP address type
-   **domain**: assets of the root domain type

 |
|Untagged|Integer|No|0|Specifies whether to return assets without tags. Valid values: 0 and 1.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Count|Integer|14|The number of entries returned on the current page.

 |
|CurrentPage|Integer|5|The current page number.

 |
|List| | |The list of returned assets.

 |
|Asset|String|test|The name of the returned asset.

 |
|AssetId|String|13183b57-f77c-459b-8512-\*\*\*\*\*\*|The ID of the returned asset.

 |
|ExpireTime|Long|1592044480000|The expiration time of the returned asset.

 |
|GmtCreate|Long|1545972690000|The time at which the asset was created.

 |
|LastScanDate|Long|1540744470000|The last time when the asset was scanned.

 |
|Source|String|UserAdd|The source of the returned asset.

 |
|Type|String|ip|The type of the returned asset.

 |
|PageCount|Integer|7|The number of returned pages.

 |
|PageSize|Integer|20|The number of entries returned on each page.

 |
|RequestId|String|6A218865-5D7C-42EE-9509-33069D66F284|The ID of the request.

 |
|TotalCount|Integer|60|The total number of returned assets.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

http(s)://[Endpoint]/? Action=DescribeAssetsByTags
&CurrentPage=1
&PageSize=20
&Search=test
&Type=Ip
&SourceIp=1.2.3.4
&Tags.1='tag1'
&Untagged=0
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeAssetsByTags>
	  <code>200</code>
	  <data>
		    <Count>20</Count>
		    <CurrentPage>1</CurrentPage>
		    <List>
			      <Asset>test.cn</Asset>
			      <AssetId>eb293323-ccc9-417d-bb03-93f7227ea128</AssetId>
			      <GmtCreate>1533543752000</GmtCreate>
			      <Source>UserAdd</Source>
			      <Type>domain</Type>
		    </List>
		    <List>
			      <Asset>***. ***.io</Asset>
			      <AssetGroupId>default</AssetGroupId>
			      <AssetId>0b77e27e-c0d9-40ef-b52d-7d6588e5ea7a</AssetId>
			      <GmtCreate>1531125482000</GmtCreate>
			      <LastScanDate>2018-07-10T11:11Z</LastScanDate>
			      <Source>UserAdd</Source>
			      <Type>subdomain</Type>
		    </List>
		    <List>
			      <Asset>1.2.3.4</Asset>
			      <AssetGroupId>default</AssetGroupId>
			      <AssetId>b7691e9e-205d-4681-bd39-1b9a7c0d810a</AssetId>
			      <GmtCreate>1524177510000</GmtCreate>
			      <LastScanDate>2018-05-21T09:38Z</LastScanDate>
			      <Source>ScanDiscover</Source>
			      <Type>ip</Type>
		    </List>
		    <PageCount>2</PageCount>
		    <PageSize>20</PageSize>
		    <TotalCount>36</TotalCount>
	  </data>
	  <requestId>6D584A17-4DA1-4CFD-BB31-BDABDF60F906</requestId>
	  <success>true</success>
</DescribeAssetsByTags>
```

`JSON` format

``` {#json_return_success_demo}
{
	"requestId":"6D584A17-4DA1-4CFD-BB31-BDABDF60F906",
	"data":{
		"PageCount":2,
		"Count":20,
		"TotalCount":36,
		"PageSize":20,
		"List":[
			{
				"Source":"UserAdd",
				"Type":"domain",
				"Asset":"test.cn",
				"GmtCreate":1533543752000,
				"AssetId":"eb293323-ccc9-417d-bb03-93f7227ea128"
			},
			{
				"Source":"UserAdd",
				"LastScanDate":"2018-07-10T11:11Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"***. ***.io",
				"GmtCreate":1531125482000,
				"AssetId":"0b77e27e-c0d9-40ef-b52d-7d6588e5ea7a"
			},
			{
				"Source":"ScanDiscover",
				"LastScanDate":"2018-05-21T09:38Z",
				"AssetGroupId":"default",
				"Type":"ip",
				"Asset":"1.2.3.4",
				"GmtCreate":1524177510000,
				"AssetId":"b7691e9e-205d-4681-bd39-1b9a7c0d810a"
			}
		],
		"CurrentPage":1
	},
	"code":200,
	"success":true
}
```

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

