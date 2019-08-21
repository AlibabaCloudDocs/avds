# DescribeHosts {#doc_api_avds_DescribeHosts .reference}

调用DescribeHosts接口，查询任务实例对应攻击面数据项中的主机列表信息。

调用DescribeHosts接口，可查询任务实例对资产进行扫描时，获取的攻击面数据项中的主机列表信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeHosts&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeHosts|系统规定参数。取值：DescribeHosts。

 |
|TaskId|Integer|是|12345|任务ID。获取指定任务ID数据。

 |
|Asset|String|否|foo.com|资产名称。查询指定资产下的检测数据。

 |
|CurrentPage|Integer|否|1|指定返回结果的当前页码。默认值为1。

 |
|PageSize|Integer|否|10|指定列表每页显示数据条数。默认值为10，且可设置值最大为10。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Records| | |返回结果的记录列表。

 |
|Hostname|String|foo-hostname|主机名称。

 |
|IP|String|1.2.3.4|IP地址。

 |
|Index|Integer|1|记录索引号。

 |
|IsUp|String|Up|机器是否存活。

 -   **Up**：存活
-   **Down** ：关机

 |
|OS|String|Windows|操作系统类型。

 |
|UpdatedAt|Long|1561392000000|扫描时间戳。

 |
|RequestId|String|DD73CB0A-6E99-49AB-9569-5A00C9732795|返回结果的请求ID。

 |
|Total|Integer|1000|返回数据的总数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeHosts
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeHosts>
	  <code>200</code>
	  <requestId>DD73CB0A-6E99-49AB-9569-5A00C9732795</requestId>
	  <success>true</success>
	  <data>
		    <Total>120</Total>
		    <Records>
			      <Index>1</Index>
			      <IP>1.2.3.4</IP>
			      <Hostname></Hostname>
			      <OS>AVtech Room Alert 26W environmental monitor </OS>
			      <IsUp>Up</IsUp>
			      <CreatedAt>1561392000000</CreatedAt>
		    </Records>
		    <Records>
			      <Index>2</Index>
			      <IP>1.2.3.4</IP>
			      <Hostname></Hostname>
			      <OS>AVtech Room Alert 26W environmental monitor </OS>
			      <IsUp>Up</IsUp>
			      <CreatedAt>1561392000000</CreatedAt>
		    </Records>
	  </data>
</DescribeHosts>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"DD73CB0A-6E99-49AB-9569-5A00C9732795",
	"data":{
		"Records":[
			{
				"Index":1,
				"IsUp":"Up",
				"IP":"1.2.3.4",
				"OS":"AVtech Room Alert 26W environmental monitor ",
				"CreatedAt":1561392000000,
				"Hostname":"foo-hostname"
			},
			{
				"Index":2,
				"IsUp":"Up",
				"IP":"1.2.3.4",
				"OS":"AVtech Room Alert 26W environmental monitor ",
				"CreatedAt":1561392000000,
				"Hostname":"foo-hostname"
			}
		],
		"Total":120
	},
	"code":"200",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

