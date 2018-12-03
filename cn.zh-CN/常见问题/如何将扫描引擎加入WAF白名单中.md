# 如何将扫描引擎加入WAF白名单中 {#concept_sh2_x21_lfb .concept}

如果您在主机中使用了Web应用防火墙（WAF）服务，需要将网站威胁扫描系统加入到WAF白名单中。未加入白名单，可能会影响扫描结果。

## 操作步骤 {#section_i4s_b31_lfb .section}

1.  登录云盾[Web应用防火墙（WAF）控制台](https://yundun.console.aliyun.com/?spm=5176.2020520001.aliyun_sidebar.54.70364bd3cEzWrd&p=waf#/waf/main/dashboard/app)。
2.  单击导航栏左侧**管理**按钮。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/154383079313599_zh-CN.png)

3.  在**网站配置**页面单击目标域名**操作**栏的**防护配置**按钮。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/154383079313600_zh-CN.png)

4.  在**精准访问控制**模块单击**前去配置**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/154383079313601_zh-CN.png)

5.  在精准访问控制列表中单击右侧的**新增规则**打开**新增规则**对话框。
6.  在**新增规则**对话框中设置参数。
    -   **规则名称：**自定义规则名称。
    -   **匹配字段：**在**匹配字段**下拉框中选择**IP**或**User-Agent**并在**匹配内容**输入栏中输入对应的网站漏洞扫描匹配项。

        -   匹配**IP**：IP可选范围47.110.180.150 ~ 47.110.180.249。

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/154383079333626_zh-CN.png)

        -   匹配**User-Agent**：请提交工单获取User-Agent匹配项内容。

            ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/154383079313602_zh-CN.png)

        **说明：** 新增规则匹配字段只需配置IP地址或User-Agent即可，其他匹配字段无需配置。建议配置字段优先选择IP地址。

7.  在**匹配动作**下拉框中选择**放行**。

    ![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/23608/154383079313603_zh-CN.png)

    **说明：** **匹配动作**设置为**放行**即可完成规则配置。请勿勾选**匹配动作**下方的**继续执行Web应用攻击防护**等选项，否则网站威胁扫描引擎的访问请求将仍可能会被WAF的其他防护功能拦截。

8.  单击**确定**应用配置。

