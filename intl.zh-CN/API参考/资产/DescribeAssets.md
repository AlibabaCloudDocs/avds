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
|Assets.N|RepeatList|否|\[\]|指定待查询的资产列表。

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
|SourceIp|String|否|127.1.1.1|指定访问者源IP地址。

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
&AssetGroupId=default
&Assets.1=[]
&CurrentPage=1
&GmtCreateFrom=1112121
&GmtCreateTo=1212121
&PageSize=20
&Search=test
&Source=UserAdd
&SourceIp=111
&Status=WaitingForVerification
&Types.1=ip
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeAssets>
	  <requestId>6D584A17-4DA1-4CFD-BB31-******</requestId>
	  <data>
		    <PageCount>2</PageCount>
		    <Count>20</Count>
		    <TotalCount>36</TotalCount>
		    <PageSize>20</PageSize>
		    <CurrentPage>1</CurrentPage>
		    <List>
			      <Source>UserAdd</Source>
			      <Status>WaitingForVerification</Status>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>domain</Type>
			      <Asset>test.cn</Asset>
			      <GmtCreate>1533543752000</GmtCreate>
			      <AssetId>eb293323-ccc9-417d-bb03-******</AssetId>
		    </List>
		    <List>
			      <Source>UserAdd</Source>
			      <Status>VerificationSuccess</Status>
			      <VerifyFailureReason>OpsSet</VerifyFailureReason>
			      <LastScanDate>2018-07-10T10:41Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>ip</Type>
			      <Asset>65.*.*.*</Asset>
			      <GmtCreate>1531126613000</GmtCreate>
			      <AssetId>6f86fcaf-72bc-41dd-9a76-******</AssetId>
		    </List>
		    <List>
			      <Source>UserAdd</Source>
			      <Status>VerificationSuccess</Status>
			      <VerifyFailureReason>OpsSet</VerifyFailureReason>
			      <LastScanDate>2018-07-25T16:30Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>demo.***.net</Asset>
			      <GmtCreate>1531126613000</GmtCreate>
			      <AssetId>fb48968d-d28d-4a96-b819-******</AssetId>
		    </List>
		    <List>
			      <Source>UserAdd</Source>
			      <Status>VerificationSuccess</Status>
			      <VerifyFailureReason>OpsSet</VerifyFailureReason>
			      <LastScanDate>2018-07-10T11:11Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>vuln.***.io</Asset>
			      <GmtCreate>1531125482000</GmtCreate>
			      <AssetId>0b77e27e-c0d9-40ef-b52d-******</AssetId>
		    </List>
		    <List>
			      <Source>UserAdd</Source>
			      <Status>VerificationSuccess</Status>
			      <VerifyFailureReason>OpsSet</VerifyFailureReason>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>bb.***01.com</Asset>
			      <GmtCreate>1529917345000</GmtCreate>
			      <AssetId>c31f3ae7-603c-49ab-9baf-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>domain</Type>
			      <Asset>***.win</Asset>
			      <GmtCreate>1527673834000</GmtCreate>
			      <AssetId>26dbe18c-a808-411d-a43f-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>www.***.com</Asset>
			      <GmtCreate>1527673834000</GmtCreate>
			      <AssetId>89211f1e-cf50-4335-a1de-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>www.***.win</Asset>
			      <GmtCreate>1527673834000</GmtCreate>
			      <AssetId>63965202-900f-4316-90dd-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>***.txooo.com</Asset>
			      <GmtCreate>1526524531000</GmtCreate>
			      <AssetId>2b32bf53-2872-43b6-853e-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>mail.b***e.it</Asset>
			      <GmtCreate>1526524531000</GmtCreate>
			      <AssetId>943a9c6d-7363-491b-aa97-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>mljt.***.com</Asset>
			      <GmtCreate>1526524531000</GmtCreate>
			      <AssetId>8c8c8e8a-24fe-41f8-a69c-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>ses-a***-1.g***.***</Asset>
			      <GmtCreate>1526524531000</GmtCreate>
			      <AssetId>e1613a49-69dd-4933-8e23-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>smtp.b***.it</Asset>
			      <GmtCreate>1526524531000</GmtCreate>
			      <AssetId>f905acfc-0e16-4b91-80f0-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>subdomain</Type>
			      <Asset>staging-01.****.at</Asset>
			      <GmtCreate>1526524531000</GmtCreate>
			      <AssetId>5a83bae2-b579-4d97-994b-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-22T09:40Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>domain</Type>
			      <Asset>upup****.com</Asset>
			      <GmtCreate>1526524531000</GmtCreate>
			      <AssetId>6e5a8bb8-1ced-48b2-b5c0-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-31T09:37Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>ip</Type>
			      <Asset>47.*.*.*</Asset>
			      <GmtCreate>1525869391000</GmtCreate>
			      <AssetId>387ccde3-e9e2-4ca2-893d-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-09T19:39Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>ip</Type>
			      <Asset>176.*.*.*</Asset>
			      <GmtCreate>1524599490000</GmtCreate>
			      <AssetId>28fa26a4-75e6-4bc8-b041-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-09T19:39Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>ip</Type>
			      <Asset>10.*.*.*</Asset>
			      <GmtCreate>1524177510000</GmtCreate>
			      <AssetId>3d45fb6f-442d-465d-b772-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-09T19:39Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>ip</Type>
			      <Asset>45.*.*.*</Asset>
			      <GmtCreate>1524177510000</GmtCreate>
			      <AssetId>b9f90eb2-0558-47af-b553-******</AssetId>
		    </List>
		    <List>
			      <Source>ScanDiscover</Source>
			      <Status>VerificationSuccess</Status>
			      <LastScanDate>2018-05-21T09:38Z</LastScanDate>
			      <AssetGroupId>default</AssetGroupId>
			      <Type>ip</Type>
			      <Asset>120.*.*.*</Asset>
			      <GmtCreate>1524177510000</GmtCreate>
			      <AssetId>b7691e9e-205d-4681-bd39-******</AssetId>
		    </List>
	  </data>
	  <code>200</code>
	  <success>true</success>
</DescribeAssets>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"6D584A17-4DA1-4CFD-BB31-******",
	"data":{
		"PageCount":2,
		"Count":20,
		"TotalCount":36,
		"PageSize":20,
		"List":[
			{
				"Source":"UserAdd",
				"Status":"WaitingForVerification",
				"AssetGroupId":"default",
				"Type":"domain",
				"Asset":"test.cn",
				"GmtCreate":1533543752000,
				"AssetId":"eb293323-ccc9-417d-bb03-******"
			},
			{
				"Source":"UserAdd",
				"Status":"VerificationSuccess",
				"VerifyFailureReason":"OpsSet",
				"LastScanDate":"2018-07-10T10:41Z",
				"AssetGroupId":"default",
				"Type":"ip",
				"Asset":"65.*.*.*",
				"GmtCreate":1531126613000,
				"AssetId":"6f86fcaf-72bc-41dd-9a76-******"
			},
			{
				"Source":"UserAdd",
				"Status":"VerificationSuccess",
				"VerifyFailureReason":"OpsSet",
				"LastScanDate":"2018-07-25T16:30Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"demo.***.net",
				"GmtCreate":1531126613000,
				"AssetId":"fb48968d-d28d-4a96-b819-******"
			},
			{
				"Source":"UserAdd",
				"Status":"VerificationSuccess",
				"VerifyFailureReason":"OpsSet",
				"LastScanDate":"2018-07-10T11:11Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"vuln.***.io",
				"GmtCreate":1531125482000,
				"AssetId":"0b77e27e-c0d9-40ef-b52d-******"
			},
			{
				"Source":"UserAdd",
				"Status":"VerificationSuccess",
				"VerifyFailureReason":"OpsSet",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"bb.***01.com",
				"GmtCreate":1529917345000,
				"AssetId":"c31f3ae7-603c-49ab-9baf-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"domain",
				"Asset":"***.win",
				"GmtCreate":1527673834000,
				"AssetId":"26dbe18c-a808-411d-a43f-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"www.***.com",
				"GmtCreate":1527673834000,
				"AssetId":"89211f1e-cf50-4335-a1de-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"www.***.win",
				"GmtCreate":1527673834000,
				"AssetId":"63965202-900f-4316-90dd-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"***.txooo.com",
				"GmtCreate":1526524531000,
				"AssetId":"2b32bf53-2872-43b6-853e-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"mail.b***e.it",
				"GmtCreate":1526524531000,
				"AssetId":"943a9c6d-7363-491b-aa97-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"mljt.***.com",
				"GmtCreate":1526524531000,
				"AssetId":"8c8c8e8a-24fe-41f8-a69c-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"ses-a***-1.g***.***",
				"GmtCreate":1526524531000,
				"AssetId":"e1613a49-69dd-4933-8e23-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"smtp.b***.it",
				"GmtCreate":1526524531000,
				"AssetId":"f905acfc-0e16-4b91-80f0-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"subdomain",
				"Asset":"staging-01.****.at",
				"GmtCreate":1526524531000,
				"AssetId":"5a83bae2-b579-4d97-994b-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-22T09:40Z",
				"AssetGroupId":"default",
				"Type":"domain",
				"Asset":"upup****.com",
				"GmtCreate":1526524531000,
				"AssetId":"6e5a8bb8-1ced-48b2-b5c0-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-31T09:37Z",
				"AssetGroupId":"default",
				"Type":"ip",
				"Asset":"47.*.*.*",
				"GmtCreate":1525869391000,
				"AssetId":"387ccde3-e9e2-4ca2-893d-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-09T19:39Z",
				"AssetGroupId":"default",
				"Type":"ip",
				"Asset":"176.*.*.*",
				"GmtCreate":1524599490000,
				"AssetId":"28fa26a4-75e6-4bc8-b041-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-09T19:39Z",
				"AssetGroupId":"default",
				"Type":"ip",
				"Asset":"10.*.*.*",
				"GmtCreate":1524177510000,
				"AssetId":"3d45fb6f-442d-465d-b772-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-09T19:39Z",
				"AssetGroupId":"default",
				"Type":"ip",
				"Asset":"45.*.*.*",
				"GmtCreate":1524177510000,
				"AssetId":"b9f90eb2-0558-47af-b553-******"
			},
			{
				"Source":"ScanDiscover",
				"Status":"VerificationSuccess",
				"LastScanDate":"2018-05-21T09:38Z",
				"AssetGroupId":"default",
				"Type":"ip",
				"Asset":"120.*.*.*",
				"GmtCreate":1524177510000,
				"AssetId":"b7691e9e-205d-4681-bd39-******"
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

