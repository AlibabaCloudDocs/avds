# DeleteAssets {#doc_api_avds_DeleteAssets .reference}

调用本接口删除用户资产。

该API可以删除用户不需要漏洞扫描的资产。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DeleteAssets&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DeleteAssets|系统规定参数。取值：DeleteAssets。

 |
|AssetIds.N|RepeatList|是|\['www.aliyun.com', 'www.taobao.com'\]|指定待删除的资产构成的列表。

 |
|SourceIp|String|否|1.2.3.4|指定访问源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|0C992F5D-8568-41B4-9685-05C0DAEAE9D7|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DeleteAssets
&Assets.1=['www.aliyun.com']
&Assets.2=['www.taobao.com']
&SourceIp=
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DeleteAssets>
      <code>200</code>
      <requestId>0C992F5D-8568-41B4-9685-05C0DAEAE9D7</requestId>
      <success>true</success>
</DeleteAssets>
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

