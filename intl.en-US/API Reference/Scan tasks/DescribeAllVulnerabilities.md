# DescribeAllVulnerabilities {#doc_api_avds_DescribeAllVulnerabilities .reference}

You can call this operation to query scan results, including the number of detected vulnerabilities and distribution of severity levels.

You can specify query conditions in the API request to filter scan results.

## Debugging {#api_explorer .section}

[OpenAPI Explorer automatically calculates the signature value. For your convenience, we recommend that you call this operation in OpenAPI Explorer. OpenAPI Explorer dynamically generates the sample code of the operation for different SDKs.](https://api.aliyun.com/#product=avds&api=DescribeAllVulnerabilities&type=RPC&version=2017-11-29)

## Request parameters {#parameters .section}

|Parameter|Type|Required|Example|Description|
|---------|----|--------|-------|-----------|
|Action|String|Yes|DescribeAllVulnerabilities|The operation that you want to perform. Set the value to DescribeAllVulnerabilities.

 |
|BeginTime|Long|No|11258600000|The beginning of the time range by which to filter the scan results.

 |
|Category|String|No|core|The type of the vulnerability by which to filter the scan results.

 |
|CurrentPage|Integer|No|1|The number of the page to return.

 |
|EndTime|Long|No|11258400000|The end of the time range by which to filter the scan results.

 |
|Lang|String|No|zh|The language in which the responses are returned.

 -   **zh**: Chinese
-   **en**: English

 |
|Module|String|No|relation\_domain|The module of the vulnerability by which to filter the scan results.

 |
|Name|String|No|test|The name of the vulnerability by which to filter the scan results.

 |
|PageSize|Integer|No|20|The number of entries to return on each page.

 |
|ScanId|String|No|2018042307022680333|The ID of the scan task by which to filter the scan results.

 |
|Search|String|No|\*\*\*. \*\*\*.net|The name of the asset by which to filter the scan results.

 |
|Severity|Integer|No|0|The severity level of the vulnerability by which to filter the scan results.

 -   **3**: important. A vulnerability that can be exploited directly with minimal difficulty. Exploited vulnerabilities of this severity level can compromise of confidentiality, integrity, or availability of user data, and affect the integrity or availability of processing resources.
-   **2**: moderate. A vulnerability that once exploited can result in significant impacts. These vulnerabilities are more difficult to exploit and are unable to conduct attacks directly. However, they provide accessibility channel for potential attacks.
-   **1**: low. A vulnerability that cannot initiate direct attacks. However, these vulnerabilities can provide information to the attacker allowing easier detection of other security flaws.
-   **0**: info. A vulnerability that does not pose any impact to the website itself. The information provided from these vulnerabilities provides minimal assistance to the attackers.

 |
|SourceIp|String|No|1.2.3.4|The source IP address of the request.

 |
|Status|String|No|0|The status of the vulnerability by which to filter scan results.

 -   **0**: unhandled
-   **1**: handled
-   **2**: whitelist
-   **3**: ignore

 |
|TaskId|Long|No|1111111|The ID of a specified subtask by which to filter the scan results.

 |
|VulType|Long|No|1|The type of vulnerabilities to detect. Valid values:

 -   1: invalid identity authentication
-   2: invalid access control
-   3: command injection
-   4: cross-site request forgery
-   5: reflected cross-site scripting \(XSS\)
-   6: stored XSS
-   7: DOM-based XSS
-   8: encryption problems
-   9: denial of service \(DoS\)
-   10: violation of security design principles
-   11: CRLF injection \(HTTP response splitting\)
-   12: sensitive information leakage
-   13: buffer overflow
-   14: unauthorized
-   15: code execution
-   16: SQL injection
-   17: server-side request forgery
-   18: clickjacking
-   19: unverified redirection
-   20: XML external entity \(XXE\)
-   21: plaintext storage of passwords
-   22: phishing
-   23: malware or Trojan
-   24: backdoor
-   25: service logic error
-   26: plaintext storage of sensitive information
-   27: plaintext transmission of sensitive information
-   28: man-in-the-middle attack
-   29: path traversal
-   30: file inclusion
-   31: session fixation
-   32: race condition vulnerability
-   33: type confusion
-   34: command execution
-   35: security configuration error
-   36: insecure deserialization
-   37: using components with known vulnerabilities
-   38: LDAP injection
-   39: insufficient log records and monitoring
-   40: weak password
-   41: file upload vulnerability

 |

## Response parameters {#resultMapping .section}

|Parameter|Type|Example|Description|
|---------|----|-------|-----------|
|Count|Integer|10|The number of returned vulnerabilities.

 |
|CurrentPage|Integer|1|The current page number.

 |
|List| | |The returned list of vulnerabilities.

 |
|Hostname|String|\*\*\*. \*\*\*.net|The name of the asset corresponding to the returned vulnerability.

 |
|Id|Long|1833085|The ID of the returned vulnerability.

 |
|LastDiscoveredAt|Long|1531191806000|The time when the vulnerability was last detected.

 |
|Name|String|Microsoft IIS version leakage|The name of the returned vulnerability.

 |
|Severity|Integer|0|The severity level of the returned vulnerability.

 |
|Status|Integer|0|The processing status of the returned vulnerability.

 |
|Target|String|http://\*\*\*.testfire.net/|The affected asset corresponding to the returned vulnerability.

 |
|PageCount|Integer|2|The number of returned pages.

 |
|PageSize|Integer|20|The number of entries returned per page.

 |
|RequestId|String|DFF34FB0-12D9-4B8B-9DD4-1BD89A33950F|The ID of the request.

 |
|TotalCount|Integer|22|The number of returned vulnerabilities.

 |

## Examples {#demo .section}

Sample requests

``` {#request_demo}

/? Action=DescribeAllVulnerabilities
&BeginTime=11111111
&Category=core
&CurrentPage=1
&EndTime=11111111
&Lang=zh
&Module=relation_domain
&Name=test
&PageSize=20
&ScanId=2018042307022680333
&Search=***.testfire.net
&Severity=0
&SourceIp=1.2.3.4
&Status=0
&TaskId=1111111
&<Common request parameters>

```

Sample success responses

`XML` format

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
			      <Name>Microsoft IIS version leakage</Name>
			      <Status>3</Status>
			      <Severity>0</Severity>
			      <Target>http://***.testfire.net/</Target>
			      <Id>1833085</Id>
			      <LastDiscoveredAt>1531191806000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>Microsoft IIS version leakage</Name>
			      <Status>0</Status>
			      <Severity>0</Severity>
			      <Target>https://***.testfire.net/</Target>
			      <Id>1833086</Id>
			      <LastDiscoveredAt>1531191806000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>OPTIONS method allowed by the server</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net:80</Target>
			      <Id>1833088</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>ASP.NET DEBUG mode enabled</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net</Target>
			      <Id>1833090</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>ASP.NET DEBUG mode enabled</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>https://***.testfire.net</Target>
			      <Id>1833091</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>OPTIONS method allowed by the server</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>https://***.testfire.net:443</Target>
			      <Id>1833094</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>WEB sensitive directory detection</Name>
			      <Status>3</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net:8080/docs/</Target>
			      <Id>1833096</Id>
			      <LastDiscoveredAt>1531191612000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>OPTIONS method allowed by the server</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net:80</Target>
			      <Id>1833073</Id>
			      <LastDiscoveredAt>1531190450000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>ASP.NET DEBUG mode enabled</Name>
			      <Status>0</Status>
			      <Severity>1</Severity>
			      <Target>http://***.testfire.net</Target>
			      <Id>1833074</Id>
			      <LastDiscoveredAt>1531190450000</LastDiscoveredAt>
			      <Hostname>***.testfire.net</Hostname>
		    </List>
		    <List>
			      <Name>OPTIONS method allowed by the server</Name>
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

`JSON` format

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
				"Name":"Microsoft IIS version leakage",
				"Status":3,
				"Target":"http://***.testfire.net/",
				"Severity":0,
				"LastDiscoveredAt":1531191806000,
				"Id":1833085,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"Microsoft IIS version leakage",
				"Status":0,
				"Target":"https://***.testfire.net/",
				"Severity":0,
				"LastDiscoveredAt":1531191806000,
				"Id":1833086,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"OPTIONS method allowed by the server",
				"Status":0,
				"Target":"http://***.testfire.net:80",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833088,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"ASP.NET DEBUG mode enabled",
				"Status":0,
				"Target":"http://***.testfire.net",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833090,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"ASP.NET DEBUG mode enabled",
				"Status":0,
				"Target":"https://***.testfire.net",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833091,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"OPTIONS method allowed by the server",
				"Status":0,
				"Target":"https://***.testfire.net:443",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833094,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"WEB sensitive directory detection",
				"Status":3,
				"Target":"http://***.testfire.net:8080/docs/",
				"Severity":1,
				"LastDiscoveredAt":1531191612000,
				"Id":1833096,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"OPTIONS method allowed by the server",
				"Status":0,
				"Target":"http://***.testfire.net:80",
				"Severity":1,
				"LastDiscoveredAt":1531190450000,
				"Id":1833073,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"ASP.NET DEBUG mode enabled",
				"Status":0,
				"Target":"http://***.testfire.net",
				"Severity":1,
				"LastDiscoveredAt":1531190450000,
				"Id":1833074,
				"Hostname":"***.testfire.net"
			},
			{
				"Name":"OPTIONS method allowed by the server",
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

## Error codes { .section}

For more information about error codes, visit [API Error Center](https://error-center.alibabacloud.com/status/product/avds).

