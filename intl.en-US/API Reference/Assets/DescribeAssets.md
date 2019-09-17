# DescribeAssets {#doc_api_avds_DescribeAssets .reference}

You can call this operation to query the asset list.

You can call this operation to query all assets by pagination and query your Alibaba Cloud assets.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeAssets&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeAssets|The operation that you want to perform. Set the value to DescribeAssets.

 |
|Assets.N|RepeatList|No|\['1.2.3.5'\]|Specifies asset N to be queried.

 |
|CurrentPage|Integer|No|1|The number of the page to return.

 |
|GmtCreateFrom|Long|No|1112121000000|The beginning of the time range where the asset is created.

 |
|GmtCreateTo|Long|No|1212121000000|The end of the time range where the asset is created.

 |
|PageSize|Integer|No|20|The number of entries to return on each page.

 |
|Search|String|No|test|The information by which to filter a specified asset.

 |
|Source|String|No|UserAdd|The source of the asset to return. Valid values:

 -   **UserAdd**
-   **AutoImport**
-   **ScanDiscover**

 |
|SourceIp|String|No|1.2.3.4|The source IP address of the request.

 |
|Status|String|No|WaitingForVerification|The verification status of the asset to return.

 -   **WaitingForVerification**
-   **VerificationSuccess**
-   **VerificationFailure**
-   **Verifying**

 |
|Types.N|RepeatList|No|ip|The type of the asset to return. Valid values:

 -   **domain**: the root domain of the asset.
-   **ip**: the IP address of the asset.
-   **subdomain**: the subdomain of the asset.

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Count|Integer|20|The number of data entries returned on the current page.

 |
|CurrentPage|Integer|1|The current page number.

 |
|List| | |The list of returned assets.

 |
|Asset|String|test.cn|The name of the returned asset.

 |
|AssetId|String|eb293323-ccc9-417d-bb03-\*\*\*\*\*\*|The ID of the returned asset.

 |
|ExpireTime|Long|1592044480000|The expiration time of the returned asset.

 |
|GmtCreate|Long|1533543752000|The time at which the asset was created.

 |
|LastScanDate|Long|1533543752000|The last scan time of the returned asset.

 |
|Source|String|UserAdd|The source type of the returned asset.

 |
|Type|String|domain|The type of the returned asset.

 |
|PageCount|Integer|2|The number of returned pages.

 |
|PageSize|Integer|20|The number of entries returned on each page.

 |
|RequestId|String|6D584A17-4DA1-4CFD-BB31-\*\*\*\*\*\*|The ID of the request.

 |
|TotalCount|Integer|36|The total number of returned assets.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

/? Action=DescribeAssets
&Assets.1='1.2.3.5'
&CurrentPage=1
&GmtCreateFrom=1112121
&GmtCreateTo=1212121
&PageSize=20
&Search=test
&Source=AutoImport
&SourceIp=1.2.3.4
&Types.1=ip
&<Common request parameters>

```

Sample success responses

`XML` format

``` {#xml_return_success_demo}
<DescribeAssets>
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
			      <AssetId>0b77e27e-c0d9-40ef-b52d-7d6588e5ea7a</AssetId>
			      <GmtCreate>1531125482000</GmtCreate>
			      <LastScanDate>2018-07-10T11:11Z</LastScanDate>
			      <Source>UserAdd</Source>
			      <Type>subdomain</Type>
		    </List>
		    <List>
			      <Asset>1.2.3.4</Asset>
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
</DescribeAssets>
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
				"Type":"subdomain",
				"Asset":"***. ***.io",
				"GmtCreate":1531125482000,
				"AssetId":"0b77e27e-c0d9-40ef-b52d-7d6588e5ea7a"
			},
			{
				"Source":"ScanDiscover",
				"LastScanDate":"2018-05-21T09:38Z",
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

