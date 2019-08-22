# AddAssets {#doc_api_avds_AddAssets .reference}

调用本接口添加用户资产。

该API可以添加资产列表和标签列表。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=AddAssets&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|AddAssets|系统规定参数。取值：AddAssets。

 |
|Assets.N|RepeatList|是|\['a.aliyun.com', 'b.aliyun.com'\]|指定待添加的资产列表。

 |
|SourceIp|String|否|1.2.3.4|指定访问者源IP地址。

 |
|Tags.N|RepeatList|否|\['tag1', 'tag2'\]|指定添加标签列表中各标签下的资产。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|0C992F5D-8568-41B4-9685-05C0DAEAE9D7|返回请求结果ID。

 |
|Success|Boolean|true|返回请求添加资产是否成功的结果。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]//?Action=AddAssets
&Assets.1='a.aliyun.com'
&Assets.2='b.aliyun.com'
&Tags.1='tag1'
&Tags.2='tag2'
&SourceIp=
&<公共请求参数>


```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<AddAssets>
      <code>200</code>
      <requestId>0C992F5D-8568-41B4-9685-05C0DAEAE9D7</requestId>
      <success>true</success>
</AddAssets>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"0C992F5D-8568-41B4-9685-05C0DAEAE9D7",
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

