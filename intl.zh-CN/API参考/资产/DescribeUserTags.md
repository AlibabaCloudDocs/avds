# DescribeUserTags {#doc_api_avds_DescribeUserTags .reference}

调用本接口查询用户所有标签列表。

该API可以查看用户资产的所有标签列表信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeUserTags&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeUserTags|系统规定参数。取值：DescribeUserTags。

 |
|CurrentPage|Integer|否|20|指定待查询列表的当前页码。

 |
|Lang|String|否|zh|指定返回结果语言环境。

 -   **zh**：中文
-   **en**：英文

 |
|PageSize|Integer|否|2|指定待查询结果每页显示数据总数量。

 |
|Search|String|否|test.\*\*.com|根据搜索信息查询特定资产标签列表。

 |
|SourceIp|String|否|1.2.3.4|指定访问者源IP地址。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|25|返回结果当前页数据总条数。

 |
|CurrentPage|Integer|3|返回结果的当前页码。

 |
|List| | |返回的标签列表信息。

 |
|AssetCount|Integer|200|返回标签下的资产数量。

 |
|TagKey|String|tag1|返回的标签名称。

 |
|PageCount|Integer|5|返回结果总页数。

 |
|PageSize|Integer|30|返回结果每页显示数据条数。

 |
|RequestId|String|0C992F5D-8568-41B4-9685-05C0DAEAE9D7|返回结果的请求ID。

 |
|TotalCount|Integer|60|返回的标签总数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeUserTags
&SourceIp=
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeUserTags>
      <code></code>
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

`JSON` 格式

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
	"code":"",
	"success":true
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.alibabacloud.com/status/product/avds)查看更多错误码。

