# DescribeAssets {#doc_api_avds_DescribeAssets .reference}

调用本接口查询资产列表。

该API可以分页查询所有资产；可以查询用户阿里云资产。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeAssets&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAssets|系统规定参数。取值：DescribeAssets。

 |
|Assets.N|RepeatList|否|\['1.2.3.5'\]|指定待查询的资产列表。

 |
|CurrentPage|Integer|否|1|指定返回列表的当前页码。

 |
|GmtCreateFrom|Long|否|1112121000000|资产创建时间的开始区间。

 |
|GmtCreateTo|Long|否|1212121000000|资产创建时间的结束区间。

 |
|PageSize|Integer|否|20|指定返回的列表每页的数据条数。

 |
|Search|String|否|test|指定查询特定资产信息。

 |
|Source|String|否|UserAdd|指定返回特定资产来源下的资产信息。可选

 -   **UserAdd**：用户添加
-   **AutoImport**：自动导入
-   **ScanDiscover**：资产发现

 |
|SourceIp|String|否|1.2.3.4|指定访问者源IP地址。

 |
|Status|String|否|WaitingForVerification|指定查询特定资产认证状态的资产信息。

 -   **WaitingForVerification**：等待验证
-   **VerificationSuccess**：验证成功
-   **VerificationFailure**：验证失败
-   **Verifying**：验证中

 |
|Types.N|RepeatList|否|ip|指定返回特定资产类型下的资产信息。可选：

 -   **domain**：资产根域名
-   **ip**：资产IP
-   **subdomain**：资产子域名

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|20|返回结果的当前页显示数据条数。

 |
|CurrentPage|Integer|1|返回结果的当前页码。

 |
|List| | |资产列表。

 |
|Asset|String|test.cn|返回资产的名称。

 |
|AssetId|String|eb293323-ccc9-417d-bb03-\*\*\*\*\*\*|返回资产的ID。

 |
|ExpireTime|Long|1592044480000|用户资产的到期时间。

 |
|GmtCreate|Long|1533543752000|返回资产的创建时间。

 |
|LastScanDate|Long|1533543752000|返回资产的最后漏洞扫描时间。

 |
|Source|String|UserAdd|返回资产的来源类型。

 |
|Type|String|domain|返回资产的所属资产类型。

 |
|PageCount|Integer|2|回结果页数。

 |
|PageSize|Integer|20|返回结果每页显示的总数据条数。

 |
|RequestId|String|6D584A17-4DA1-4CFD-BB31-\*\*\*\*\*\*|请求结果ID。

 |
|TotalCount|Integer|36|返回的资产总数。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

/?Action=DescribeAssets
&Assets.1='1.2.3.5'
&CurrentPage=1
&GmtCreateFrom=1112121
&GmtCreateTo=1212121
&PageSize=20
&Search=test
&Source=AutoImport
&SourceIp=1.2.3.4
&Types.1=ip
&<公共请求参数>

```

正常返回示例

`XML` 格式

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
			      <Asset>***.***.io</Asset>
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
				"Type":"subdomain",
				"Asset":"***.***.io",
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

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

