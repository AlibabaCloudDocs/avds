# API概览 {#doc_1266834 .concept}

漏洞扫描提供以下相关API接口。

## 资产 {#section_s2j_uea_gyc .section}

|API|描述|
|---|--|
|[AddAssets](intl.zh-CN/API参考/资产/AddAssets.md)|调用本接口添加用户资产。|
|[DescribeAssets](intl.zh-CN/API参考/资产/DescribeAssets.md)|调用本接口查询资产列表。|
|[DeleteAssets](intl.zh-CN/API参考/资产/DeleteAssets.md)|调用本接口删除用户资产。|
|[DescribeUserTags](intl.zh-CN/API参考/资产/DescribeUserTags.md)|调用本接口查询用户所有标签列表。|
|[AddAssetTags](intl.zh-CN/API参考/资产/AddAssetTags.md)|调用本接口为资产添加标签。|
|[DescribeAssetsByTags](intl.zh-CN/API参考/资产/DescribeAssetsByTags.md)|调用本接口查询标签下的资产列表。|

## 扫描任务 {#section_bij_bld_dmm .section}

|API|描述|
|---|--|
|[CreateScan](intl.zh-CN/API参考/扫描任务/CreateScan.md)|调用本接口创建扫描任务。|
|[DescribeScans](intl.zh-CN/API参考/扫描任务/DescribeScans.md)|调用本接口获取扫描任务列表。|
|[DescribeScanSessions](intl.zh-CN/API参考/扫描任务/DescribeScanSessions.md)|调用本接口获取扫描任务实例列表。|
|[GenerateVulReport](intl.zh-CN/API参考/扫描任务/GenerateVulReport.md)|调用本接口生成任务实例报表。|
|[DescribeAllVulnerabilities](intl.zh-CN/API参考/扫描任务/DescribeAllVulnerabilities.md)|调用本接口获取扫描任务结果，包含检测出的漏洞数量和漏洞严重等级分布。|
|[DescribeVulnerability](intl.zh-CN/API参考/扫描任务/DescribeVulnerability.md)|调用本接口获取漏洞详情。|

## 攻击面 {#section_yii_crp_m5p .section}

|API|描述|
|---|--|
|[DescribeSubdomains](intl.zh-CN/API参考/攻击面/DescribeSubdomains.md)|调用DescribeSubdomains接口，查询任务实例对应攻击面数据项中的子域名信息。|
|[DescribeCrawlerRequests](intl.zh-CN/API参考/攻击面/DescribeCrawlerRequests.md)|调用DescribeCrawlerRequests接口，查询任务实例对应攻击面数据项中的爬虫流量信息。|
|[DescribeHostAttackSurfacesFacets](intl.zh-CN/API参考/攻击面/DescribeHostAttackSurfacesFacets.md)|调用DescribeHostAttackSurfacesFacets接口，查询任务实例对应攻击面数据项中的主机攻击面统计信息。|
|[DescribeAttackSurfacesFacets](intl.zh-CN/API参考/攻击面/DescribeAttackSurfacesFacets.md)|调用DescribeAttackSurfacesFacets查询任务实例攻击面数据统计信息。|
|[DescribeWebTechs](intl.zh-CN/API参考/攻击面/DescribeWebTechs.md)|调用DescribeWebTechs接口，查询任务实例对应攻击面数据项中的Web应用信息。|
|[DescribeDomains](intl.zh-CN/API参考/攻击面/ DescribeDomains.md)|调用DescribeDomains接口，查询任务实例对应攻击面数据项中的域名信息。|
|[DescribeHosts](intl.zh-CN/API参考/攻击面/DescribeHosts.md)|调用DescribeHosts接口，查询任务实例对应攻击面数据项中的主机列表信息。|
|[DescribePorts](intl.zh-CN/API参考/攻击面/DescribePorts.md)|调用DescribePorts接口，查询任务实例对应攻击面数据项中的端口服务信息。|
|[DescribeDomainAttackSurfacesFacets](intl.zh-CN/API参考/攻击面/DescribeDomainAttackSurfacesFacets.md)|调用DescribeDomainAttackSurfacesFacets接口，查询任务实例对应攻击面数据项中的域名攻击面统计信息。|
|[DescribeWebServers](intl.zh-CN/API参考/攻击面/DescribeWebServers.md)|调用DescribeWebServers接口，查询任务实例对应攻击面数据项中的Web服务器信息。|
|[DescribeWebPaths](intl.zh-CN/API参考/攻击面/DescribeWebPaths.md)|调用DescribeWebPaths接口，查询任务实例对应攻击面数据项中的Web路径信息。|
|[DescribeDNSMap](intl.zh-CN/API参考/攻击面/DescribeDNSMap.md)|调用DescribeDNSMap接口，查询任务实例对应攻击面数据项中的DNS解析记录信息。|

