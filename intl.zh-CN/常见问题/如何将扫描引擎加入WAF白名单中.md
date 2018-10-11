# 如何将扫描引擎加入WAF白名单中 {#concept_sh2_x21_lfb .concept}

如果您在主机中使用了Web应用防火墙（WAF）服务，需要将WAF添加到网站威胁扫描系统的白名单中。未加入白名单，可能会影响扫描结果。

## 操作步骤 {#section_i4s_b31_lfb .section}

1.  登录云盾[Web应用防火墙（WAF）控制台](https://yundun.console.aliyun.com/?spm=5176.2020520001.aliyun_sidebar.54.70364bd3cEzWrd&p=waf#/waf/main/dashboard/app)。
2.  单击导航栏左侧**管理**按钮。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/153928093513599_zh-CN.png)

3.  在**网站配置**页面单击目标域名**操作**栏的**防护配置**按钮。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/153928093613600_zh-CN.png)

4.  在**精准访问控制**模块单击**前去配置**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/153928093613601_zh-CN.png)

5.  在精准访问控制列表中单击右侧的**新建规则**。
6.  在新建规则列表中设置**规则名称**。
7.  单击**新增条件**。
8.  在**匹配字段**下拉框中选择**User-Agent**并在**匹配内容**输入栏中输入网站漏洞扫描的匹配项。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/153928093613602_zh-CN.png)

    **说明：** 请提交工单获取匹配项内容。

9.  在**匹配动作**下拉框中选择**放行**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/153928093613602_zh-CN.png)

10. 单击**确定**。

