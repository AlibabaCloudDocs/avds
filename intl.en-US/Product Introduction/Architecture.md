# Architecture {#concept_ckc_2mg_xdb .concept}

Website Threat Inspector consists of the following modules:

-   **Common data system**: stores assets information on the Internet, including worldwide IP affiliations, worldwide domains, WHOIS data, Internet Security Socket Layer \(SSL\) certificates, Internet port fingerprints, Internet Web fingerprints, registered Internet Content Providers \(ICPs\), and employee password databases.

-   **Asset analysis module**: uses the big data resources of Alibaba Cloud to parse and associate domains, and analyzes and recognizes port fingerprints and Web fingerprints of assets.

-   **Scan task module**: refers to the elastic and scalable scan worker cluster deployed in the cloud. In this module, you can configure scan tasks, schedule and dispatch tasks, detect website threats such as vulnerabilities, sensitive content, drive-by downloads, and tampering, by using the vulnerability database and rule components, and output website threats and detection results.


