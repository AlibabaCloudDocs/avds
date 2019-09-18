# Make API requests {#concept_zlz_t2j_ygb .concept}

You can send HTTP GET requests to call the Cloud Security Scanner \(CSS\) API. Before you send a request, specify the request parameters for the specific operation. A response is returned for each request. Requests and responses are encoded using UTF-8.

## Request structure {#section_mqj_q3f_mdb .section}

The CSS API operations use the RPC protocol. You can call CSS API operations by sending HTTP GET requests.

The request syntax is as follows:

``` {#codeblock_nj4_ueo_qkb}
https://Endpoint/?Action=xx&Parameters
```

Where:

-   Endpoint: the endpoint of the CSS API is avds.aliyuncs.com.
-   Action: the name of the operation being performed. For example, to query the asset of users, the Action parameter must be set to DescribeAssets.
-   Version: the version of the API to be used. The API version of CSS is 2017-11-29.
-   Parameters: the request parameters for the operation being called. Separate multiple parameters with ampersands \(&\).

    The request parameters include common request parameters and API-specific parameters. Common parameters include the API version and authentication information. For more information, see [Common parameters](intl.en-US/API Reference/Common parameters.md#).


The following example demonstrates how to call the DescribeAssets operation in CSS:

**Note:** To improve readability, the API request is displayed in the following format:

``` {#codeblock_88g_hrf_cya}
http(s)://avds.aliyuncs.com/? Action=DescribeAssets
&Format=xml
&Version=2017-11-29
&Signature=xxxx%xxxx%3D
&SignatureMethod=HMAC-SHA1
&SignatureNonce=15215528852396
&SignatureVersion=1.0
&AccessKeyId=key-test
&TimeStamp=2012-06-01T12:00:00Z
...
```

## API authorization {#section_mlp_qmf_mdb .section}

To ensure the security of your account, we recommend that you call the CSS API as a RAM user. Before calling CSS API as a RAM user, you must create a RAM user and assign corresponding permissions to it.

## Request signatures {#section_jtc_ymf_mdb .section}

You must sign all API requests to ensure security. Cloud Security Scanner uses the request signature to verify the identity of the API caller.

For more information about the signature calculation process, see [Sign PRC APIs](https://www.alibabacloud.com/help/doc-detail/66384.htm).

CSS implements symmetric encryption with an AccessKey ID and an AccessKey secret to verify the identity of the request sender. An AccessKey pair consists of an AccessKey ID and an AccessKey secret. An AccessKey pair is an identity credential issued to Alibaba Cloud accounts and RAM users that is similar to a logon username and password. The AccessKey ID is used to verify the identity of the user, while the AccessKey secret is used to encrypt and verify the signature string. You must keep your AccessKey secret strictly confidential.

For RPC APIs, you must add the signature to the API request in the following format:

``` {#codeblock_c56_uqq_jip}
https://endpoint/?SignatureVersion=1.0&SignatureMethod=HMAC-SHA1&Signature=CT9X0VtwR86fNWSnsc6v8YGOjuE%3D&SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0ad82fd6cf
```

Take DescribeAssets as an example. If the AccessKey ID is `testid`, the AccessKey secret is `testsecret`, the original request URL is as follows:

``` {#public1}
https://avds.aliyuncs.com/?Action=DescribeAssets
&TimeStamp=2016-02-23T12:46:24Z
&Format=XML
&AccessKeyId=testid
&SignatureMethod=HMAC-SHA1
&SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0ad82fd6cf
&Version=2017-11-29
&SignatureVersion=1.0
```

Perform the following steps to calculate the signature:

1.  Use the request parameters to create the string-to-sign.

    ``` {#codeblock_2if_ek9_qum}
    GET&%2F&AccessKeyId%3Dtestid&Action%3DDescribeAssets&Format%3DXML&SignatureMethod%3DHMAC-SHA1&SignatureNonce%3D3ee8c1b8-83d3-44af-a94f-4e0ad82fd6cf&SignatureVersion%3D1.0&TimeStamp%3D2016-02-23T12%253A46%253A24Z&Version%3D2018-12-03
    ```

2.  Calculate the HMAC value of the string-to-sign.

    Append an ampersand \(&\) to the AccessKey secret and use the new string as the key to calculate the HMAC value. In this example, the key is `testsecret&`.

    ``` {#codeblock_mpd_wee_r1o}
    CT9X0VtwR86fNWSnsc6v8YGOjuE=
    ```

3.  Add the signature string to the request parameters.

    ``` {#public3}
    https://advs.aliyuncs.com/?Action=DescribeAssets
    &TimeStamp=2016-02-23T12:46:24Z
    &Format=XML
    &AccessKeyId=testid
    &SignatureMethod=HMAC-SHA1
    &SignatureNonce=3ee8c1b8-83d3-44af-a94f-4e0ad82fd6cf
    &Version=2017-11-29
    &SignatureVersion=1.0
    &Signature=CT9X0VtwR86fNWSnsc6v8YGOjuE%3D
    ```


**Note:** Alibaba Cloud offers SDKs and third-party SDKs in multiple languages, which helps you to calculate the signature. For more information about Alibaba Cloud SDKs, see [Alibaba Cloud Development Kit \(SDK\)](https://www.alibabacloud.com/zh/support/developer-resources?spm=a2c5t.10695662.1996646101.searchclickresult.7e6c5b4fbkB1Id).

