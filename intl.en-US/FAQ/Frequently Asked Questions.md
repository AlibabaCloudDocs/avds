# Frequently Asked Questions {#concept_jl2_5sn_xdb .concept}

## How to calculate the number of scan licenses required? {#section_ekw_vsn_xdb .section}

Website Threat Inspector requires scan licenses depending on the number of subdomain names. You can select a proper service package according to the number of subdomain names. For example, mail.google.com and 250.mail.google.com are regarded as two subdomains. However, if a domain name includes a directory, for example, mail.google.com and mail.google.com/123, they are regarded as the same subdomain.

## How to verify target domain names? {#section_szd_xsn_xdb .section}

-   If you add a primary domain name, such as example.com, you need to add a CNAME record under the primary domain name to point 29ea855c6ab1be883632d3fa1580d489.example.com to 29ea855c6ab1be883632d3fa1580d489.verify.aliyunscan.com to verify the added domain name.
-   If you add a subdomain name, such as www.example.com, you need to choose Website Threat Inspector \> Assets, click Add Asset in the upper-right corner, and click Download Verification File in the pop-up dialog box to download a verification file. Then, add the verification file to your website directory \(http://www.example.com/29ea855c6ab1be883632d3fa1580d489\) to verify the added domain name.

## Can I run unlimited scans? {#section_n1c_1tn_xdb .section}

Yes, you can. No matter what service package you have selected, you can always scan unlimited times to persistently detect risks in your assets.

## How to view scan status? {#section_rcl_btn_xdb .section}

Go to the **Scans** \> **Scan List**page, to view the status of your scans. You can also view scan details, and export the reports.

## What scan engine IP addresses are included in Website Threat Inspector? {#section_tjv_2tn_xdb .section}

Website Threat Inspector simulates intrusions from the Internet, and implements security scanning. If your server has been configured with security protection or monitoring, such as the Web Application Firewall \(WAF\) or Security Operations Center \(SOC\), we recommend that you assign scan access permissions to scan engine IP segments in Website Threat Inspector. You can add these IP segments to the whitelist to ensure normal scan services.

Website Threat Inspector includes the following fixed IP segments:

-   116.62.104.31

-   47.95.148.80

-   118.31.114.10

-   101.132.222.93

-   47.52.33.43

-   101.132.26.136

-   47.97.8.25

-   47.97.7.181

-   47.97.19.138

-   47.95.193.144

-   101.132.46.229

-   116.62.190.26

-   47.97.19.113

-   47.100.76.81

-   106.14.104.235

-   47.92.2.196

-   47.96.176.17

-   47.96.175.153

-   47.96.175.94

-   47.96.176.40

-   47.96.176.229

-   47.100.100.87

-   47.100.101.203

-   47.100.97.128

-   47.100.100.210

-   47.100.31.118

-   39.106.126.11

-   39.106.124.61

-   47.93.23.236

-   39.106.126.57

-   39.106.120.156


