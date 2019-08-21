# GenerateVulReport {#doc_api_avds_GenerateVulReport .reference}

调用本接口生成任务实例报表。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=GenerateVulReport&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|GenerateVulReport|系统规定参数。取值：GenerateVulReport。

 |
|TaskIds.N|RepeatList|是|\[\]|指定待返回报表的任务实例列表。

 |
|Lang|String|否|zh|指定返回结果的语言环境。

 -   **zh**：中文
-   **en**：英文

 |
|SourceIp|String|否|127.1.1.1|指定访问源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|6D584A17-4DA1-4CFD-BB31-\*\*\*\*\*\*|返回结果的请求ID。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=GenerateVulReport
&TaskIds.1=111
&TaskIds.2=112
&SourceIp=
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<GenerateVulReport>
      <code>200</code>
      <message></message>
      <success>true</success>
</GenerateVulReport>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"message":"",
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

