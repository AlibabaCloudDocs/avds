# Common parameters {#concept_yqm_l3h_ygb .concept}

This topic describes common request parameters required for each API request.

## Common request parameters {#section_zm5_rgf_cz .section}

Common request parameters must be included in all API operations.

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Format|string|No|The format to return the response values in. Valid values: JSON and XML. Default value: XML.

 |
|Version|String|Yes|The version number of the API. The format is YYYY-MM-DD. Set the value to 2017-11-29.

 |
|AccessKeyId|String|Yes|The AccessKey ID provided to you by Alibaba Cloud.|
|Signature|String|Yes|The signature string of the current request.|
|SignatureMethod|String|Yes|The encryption method of the signature string. Set the value to HMAC-SHA1.

 |
|Timestamp|String|Yes|The timestamp of the request. Specify the time in the ISO 8601 standard in the `YYYY-MM-DDThh:mm:ssZ` format. The time must be in UTC. For example, `2013-01-10T12:00:00Z` indicates January 10, 2013, 20:00:00 \(UTC+8\).

 |
|SignatureVersion|String|Yes|The version of the signature encryption algorithm. Set the value to 1.0.|
|SignatureNonce|String|Yes|A unique, random number used to prevent replay attacks. You must use different numbers for different requests.

 |
|ResourceOwnerAccount|String|No|The owner account \(the logon username\) of the resource to be accessed through this API request.|

**Examples** 

``` {#codeblock_fwm_ref_rao}
https://avds.aliyuncs.com/
? Format=xml
&Version=2017-11-29
&Signature=Pc5WB8gokVn0xfeu%2FZV%2BiNM1dgI%3D
&SignatureMethod=HMAC-SHA1
&SignatureNonce=15215528852396
&SignatureVersion=1.0
&AccessKeyId=key-test
&Timestamp=2012-06-01T12:00:00Z
```

## Common response parameters {#section_rjn_1hf_cz .section}

The API response uses a unified format. A 2XX HTTP status code is returned if the call is successful. A 4xx or 5xx HTTP status code is returned if the call has failed.

Response data can be returned in either the JSON or XML format. You can specify the response format when you are making the request. The default response format is XML.

Each time you send a request to call an API, the system returns a unique identifier RequestId, regardless of whether the request is successful.

-   XML format

    ``` {#codeblock_q1o_87l_8bc}
    <? xml version="1.0" encoding="utf-8"? > 
        <!-Result root node-->
        <Operation name+Response>
            <!-Return request tag-->
            <RequestId>4C467B38-3910-447D-87BC-AC049166F216</RequestId>
            <!-Returned result data-->
        </Operation name+Response>
    					
    ```

-   JSON format

    ``` {#codeblock_68m_qy9_uqg}
    {
        "RequestId":"4C467B38-3910-447D-87BC-AC049166F216",
        /*Returned result data*/
        }
    ```


