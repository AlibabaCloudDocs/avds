# DescribeAssetsByTags {#doc_api_avds_DescribeAssetsByTags .reference}

调用本接口查询标签下的资产列表。

该API可以查看多个标签下的资产列表信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeAssetsByTags&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAssetsByTags|系统规定参数。取值：DescribeAssetsByTags。

 |
|Tags.N|RepeatList|是|\['tag1', 'tag2'\]|指定待显示的标签下资产的标签列表。

 |
|CurrentPage|Integer|否|2|指定返回资产列表的当前页码。

 |
|Lang|String|否|zh|指定返回结果的语言环境。

 -   **zh**：中文
-   **en**：英文

 |
|PageSize|Integer|否|20|指定返回资产列表的每页显示数据总条数。

 |
|Search|String|否|1.2.3.5|指定待查询的目标资产信息。

 |
|SourceIp|String|否|1.2.3.4|指定访问者源IP。

 |
|Type|String|否|ip|指定目标资产类型的标签信息。可选

 -   **ip**：IP类型资产
-   **domain**：根域名类型资产

 |
|Untagged|Integer|否|0|指定是否获取无标签下的资产信息。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|14|返回结果的当前页中显示数据条数。

 |
|CurrentPage|Integer|5|返回结果的当前页码。

 |
|List| | |返回的资产列表。

 |
|Asset|String|test|返回资产列表中的资产名称。

 |
|AssetId|String|13183b57-f77c-459b-8512-\*\*\*\*\*\*|返回资产列表中的资产ID。

 |
|ExpireTime|Long|1592044480000|用户资产的到期时间。

 |
|GmtCreate|Long|1545972690000|返回资产列表中的资产的创建时间。

 |
|LastScanDate|Long|1540744470000|返回资产列表中的资产的最后漏洞扫描时间。

 |
|Source|String|UserAdd|返回资产列表中的资产来源类型。

 |
|Type|String|ip|返回资产列表中的资产类型。

 |
|PageCount|Integer|7|返回结果的总页数。

 |
|PageSize|Integer|20|返回结果每页显示的数据总条数。

 |
|RequestId|String|6A218865-5D7C-42EE-9509-33069D66F284|返回结果的请求ID。

 |
|TotalCount|Integer|60|返回结果的资产总数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeAssetsByTags
&CurrentPage=1
&PageSize=20
&Search=test
&Type=Ip
&SourceIp=1.2.3.4
&Tags.1='tag1'
&Untagged=0
&<公共请求参数>

```

正常返回示例

`XML` 格式

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
			      <Asset>***.***.io</Asset>
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

`JSON` 格式

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
				"Asset":"***.***.io",
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

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

