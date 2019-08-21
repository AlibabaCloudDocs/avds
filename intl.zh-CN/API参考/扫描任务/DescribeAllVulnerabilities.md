# DescribeAllVulnerabilities {#doc_api_avds_DescribeAllVulnerabilities .reference}

调用本接口获取扫描任务结果，包含检测出的漏洞数量和漏洞严重等级分布。

该API可以通过条件查询来获取漏洞扫描结果。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=avds&api=DescribeAllVulnerabilities&type=RPC&version=2017-11-29)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeAllVulnerabilities|系统规定参数。取值：DescribeAllVulnerabilities。

 |
|BeginTime|Long|否|11258600000|指定查询特定搜索条件（任务开始时间）下的漏洞扫描结果。

 |
|Category|String|否|core|根据类别查询漏洞扫描结果。

 |
|CurrentPage|Integer|否|1|指定返回结果当前页码。

 |
|EndTime|Long|否|11258400000|指定查询特定任务结束时间下漏洞扫描结果

 |
|Lang|String|否|zh|指定返回结果的语言环境。

 -   **zh**：中文
-   **en**：英文

 |
|Module|String|否|relation\_domain|根据漏洞模块查询任务实例扫描结果。

 |
|Name|String|否|test|指定查询特定漏洞名称的检测结果。

 |
|PageSize|Integer|否|20|页大小

 |
|ScanId|String|否|2018042307022680333|指定查询特定任务ID的漏洞扫描结果。

 |
|Search|String|否|demo.testfire.net|根据特定的搜索条件（资产名）查询漏洞扫描结果。

 |
|Severity|Integer|否|0|指定查询特定威胁程度下漏洞结果。

 -   **3**：高危。表示可以直接被利用的漏洞，且利用难度较低。被攻击之后可能对网站或服务器的正常运行造成严重影响，或对用户财产及个人信息造成重大损失。
-   **2**：中危。表示被利用之后，造成的影响较大，但直接利用难度较高的漏洞。或本身无法直接攻击，但能为进一步攻击造成便利的漏洞。
-   **1**：低危。表示无法直接实现攻击，但提供的信息可能让攻击者更容易找到其他安全漏洞。
-   **0**：信息。表示本身对网站安全没有直接影响，提供的信息可能为攻击者提供少量帮助，或可用于其他手段的攻击，如社工等。

 |
|SourceIp|String|否|1.2.3.4|指定访问者源IP地址。

 |
|Status|String|否|0|指定查询特定漏洞状态的扫描结果。

 -   **0**：未处理
-   **1**：已处理
-   **2**：白名单
-   **3**：忽略

 |
|TaskId|Long|否|1111111|指定特定子任务ID的漏洞扫描结果。

 |
|VulType|Long|否|1|可检测的漏洞类型，包含以下类型：

 -   1,"失效的身份认证"
-   2,"失效的访问控制"
-   3,"命令注入"
-   4,"跨站请求伪造"
-   5,"跨站点脚本（反射型）"
-   6,"跨站点脚本（存储型）"
-   7,"跨站点脚本（DOM型）"
-   8,"加密问题"
-   9,"拒绝服务"
-   10,"违反安全设计原则"
-   11,"HTTP响应CRLF注入"
-   12,"敏感信息泄露"
-   13,"缓冲区溢出"
-   14,"越权"
-   15,"代码执行"
-   16,"SQL注入"
-   17,"服务器端请求伪造"
-   18,"点击劫持"
-   19,"未验证的重定向"
-   20,"XML外部实体（XXE）"
-   21,"明文存储密码"
-   22,"钓鱼"
-   23,"恶意软件/木马"
-   24,"存在后门"
-   25,"业务逻辑错误"
-   26,"敏感信息明文存储"
-   27,"敏感信息明文传输"
-   28,"中间人攻击"
-   29,"目录遍历"
-   30,"文件包含"
-   31,"会话固定"
-   32,"时间竞争漏洞"
-   33,"类型混淆"
-   34,"命令执行"
-   35,"安全配置错误"
-   36,"不安全的反序列化"
-   37,"使用含有已知漏洞的组件"
-   38,"LDAP注入"
-   39,"不足的日志记录和监控"
-   40,"弱口令"
-   41,"文件上传漏洞"

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Count|Integer|10|返回结果中的漏洞扫描结果数量。

 |
|CurrentPage|Integer|1|返回结果中显示的当前页码。

 |
|List| | |返回的漏洞列表。

 |
|Hostname|String|demo.testfire.net|返回结果中漏洞对应的资产名称。

 |
|Id|Long|1833085|返回结果中漏洞ID号。

 |
|LastDiscoveredAt|Long|1531191806000|返回结果中个漏洞最后被发现的时间。

 |
|Name|String|Microsoft IIS 版本泄露|返回结果中的各漏洞名称。

 |
|Severity|Integer|0|返回结果中各漏洞的威胁程度。

 |
|Status|Integer|0|返回结果中个漏洞的处理状态。

 |
|Target|String|http://\*\*\*.testfire.net/|返回结果中个漏洞影响发到资产信息。

 |
|PageCount|Integer|2|返回结果的总页数。

 |
|PageSize|Integer|20|返回结果中每页显示数据条数。

 |
|RequestId|String|DFF34FB0-12D9-4B8B-9DD4-1BD89A33950F|返回结果的请求ID。

 |
|TotalCount|Integer|22|返回结果中的漏洞总数量。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

/?Action=DescribeAllVulnerabilities
&BeginTime=11111111
&Category=core
&CurrentPage=1
&EndTime=11111111
&Lang=zh
&Module=relation_domain
&Name=test
&PageSize=20
&ScanId=2018042307022680333
&Search=demo.testfire.net
&Severity=0
&SourceIp=111
&Status=0
&TaskId=1111111
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeAllVulnerabilities>
	  <requestId>DFF34FB0-12D9-4B8B-9DD4-1BD89A33950F</requestId>
	  <data>
		    <PageCount>3</PageCount>
		    <Count>10</Count>
		    <TotalCount>22</TotalCount>
		    <PageSize>10</PageSize>
		    <CurrentPage>1</CurrentPage>
		    <List>
			      <Name>Microsoft IIS 版本泄露</Name>
			      <Status>3</Status>
			      <Severity>0</Severity>
			      <Target>http://***.testfire.net/</Target>
			      <Id>1833085</Id>
			      <LastDiscoveredAt>1531191806000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>Microsoft IIS 版本泄露</Name>
			      <Status>0</Status>
			      <Severity>0</Severity>
			      <Target>https://***.testfire.net/</Target>
			      <Id>1833086</Id>
			      <LastDiscoveredAt>1531191806000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>服务器允许OPTIONS方法</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net:80</Target>
			      <Id>1833088</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>ASP.NET DEBUG 模式开启</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net</Target>
			      <Id>1833090</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>ASP.NET DEBUG 模式开启</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>https://***.testfire.net</Target>
			      <Id>1833091</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>服务器允许OPTIONS方法</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>https://***.testfire.net:443</Target>
			      <Id>1833094</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>WEB 敏感目录探测</Name>
			      <Status>3</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net:8080/docs/</Target>
			      <Id>1833096</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>服务器允许OPTIONS方法</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net:80</Target>
			      <Id>1833073</Id>
			      <LastDiscoveredAt>1531190450000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>ASP.NET DEBUG 模式开启</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net</Target>
			      <Id>1833074</Id>
			      <LastDiscoveredAt>1531190450000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>服务器允许OPTIONS方法</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>https://***.testfire.net:443</Target>
			      <Id>1833078</Id>
			      <LastDiscoveredAt>1531190450000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
	  </data>
	  <code>200</code>
	  <success>true</success>
    </DescribeAllVulnerabilities>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"requestId":"DFF34FB0-12D9-4B8B-9DD4-1BD89A33950F",
	"data":{
		"PageCount":3,
		"Count":10,
		"TotalCount":22,
		"PageSize":10,
		"List":[
			{
				"Name":"Microsoft IIS 版本泄露",
				"Status":3,
				"Target":"http://***.testfire.net/",
				"Severity":0,
				"LastDiscoveredAt":1531191806000,
				"Id":1833085,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"Microsoft IIS 版本泄露",
				"Status":0,
				"Target":"https://***.testfire.net/",
				"Severity":0,
				"LastDiscoveredAt":1531191806000,
				"Id":1833086,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"服务器允许OPTIONS方法",
				"Status":0,
				"Target":"http://***.testfire.net:80",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833088,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"ASP.NET DEBUG 模式开启",
				"Status":0,
				"Target":"http://***.testfire.net",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833090,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"ASP.NET DEBUG 模式开启",
				"Status":0,
				"Target":"https://***.testfire.net",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833091,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"服务器允许OPTIONS方法",
				"Status":0,
				"Target":"https://***.testfire.net:443",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833094,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"WEB 敏感目录探测",
				"Status":3,
				"Target":"http://***.testfire.net:8080/docs/",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833096,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"服务器允许OPTIONS方法",
				"Status":0,
				"Target":"http://***.testfire.net:80",
				"Severity":1,
				"LastDiscoveredAt":1531190450000,
				"Id":1833073,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"ASP.NET DEBUG 模式开启",
				"Status":0,
				"Target":"http://***.testfire.net",
				"Severity":1,
				"LastDiscoveredAt":1531190450000,
				"Id":1833074,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"服务器允许OPTIONS方法",
				"Status":0,
				"Target":"https://***.testfire.net:443",
				"Severity":1,
				"LastDiscoveredAt":1531190450000,
				"Id":1833078,
				"Hostname":"***.testfire.net"
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

