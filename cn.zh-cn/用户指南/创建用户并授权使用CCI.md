# 创建用户并授权使用CCI<a name="cci_01_0072"></a>

本章节通过简单的用户组授权方法，将云容器实例的策略授予用户组，并将用户添加至用户组中，从而使用户拥有对应的云容器实例权限，操作流程如[图1](#fig673713328586)所示。

**图 1**  给用户授权CCI权限流程<a name="fig673713328586"></a>  
![](figures/给用户授权CCI权限流程.png "给用户授权CCI权限流程")

1.  <a name="li8135822590"></a>[创建用户组并授权](#section11705979215)

    在IAM控制台创建用户组，并授予云容器实例管理员权限“CCI Admin”。

2.  [创建IAM用户](#section5914125313212)

    在IAM控制台创建用户，并将其加入[1](#li8135822590)中创建的用户组。

3.  [用户登录并验证权限](#section12483530738)

    新创建的用户登录控制台，验证云容器实例的管理员权限。


## 前提条件<a name="section1612122929"></a>

-   “CCI Admin权限”为细粒度策略，请先在IAM控制台中开通细粒度策略，开通方法请参见：[申请细粒度访问控制公测](https://support.huaweicloud.com/usermanual-iam/iam_01_019.html)。
-   给用户组授权之前，请您了解用户组可以添加的CCI系统策略，并结合实际需求进行选择，CCI系统策略如[表1](#table6123192793918)所示。若您需要对除CCI之外的其它服务授权，IAM支持服务的所有策略请参见[权限策略](https://support.huaweicloud.com/usermanual-permissions/zh-cn_topic_0063498930.html)。

**表 1**  CCI系统策略

<a name="table6123192793918"></a>
<table><thead align="left"><tr id="zh-cn_topic_0167171797_row1346222921318"><th class="cellrowborder" valign="top" width="16.48%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0167171797_p246217292138"><a name="zh-cn_topic_0167171797_p246217292138"></a><a name="zh-cn_topic_0167171797_p246217292138"></a>策略名称</p>
</th>
<th class="cellrowborder" valign="top" width="46.03%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0167171797_p146292918139"><a name="zh-cn_topic_0167171797_p146292918139"></a><a name="zh-cn_topic_0167171797_p146292918139"></a>描述</p>
</th>
<th class="cellrowborder" valign="top" width="20.580000000000002%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0167171797_p191421447112216"><a name="zh-cn_topic_0167171797_p191421447112216"></a><a name="zh-cn_topic_0167171797_p191421447112216"></a>策略类别</p>
</th>
<th class="cellrowborder" valign="top" width="16.91%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0167171797_p1822191252217"><a name="zh-cn_topic_0167171797_p1822191252217"></a><a name="zh-cn_topic_0167171797_p1822191252217"></a>依赖关系</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0167171797_row1462142915137"><td class="cellrowborder" valign="top" width="16.48%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0167171797_p1196518294159"><a name="zh-cn_topic_0167171797_p1196518294159"></a><a name="zh-cn_topic_0167171797_p1196518294159"></a>CCI Admin</p>
</td>
<td class="cellrowborder" valign="top" width="46.03%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0167171797_p0462172991319"><a name="zh-cn_topic_0167171797_p0462172991319"></a><a name="zh-cn_topic_0167171797_p0462172991319"></a>云容器实例管理员权限，拥有该权限的用户可以执行云容器实例所有资源的创建、删除、查询、更新操作。</p>
</td>
<td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0167171797_p1414344782214"><a name="zh-cn_topic_0167171797_p1414344782214"></a><a name="zh-cn_topic_0167171797_p1414344782214"></a>细粒度策略</p>
</td>
<td class="cellrowborder" valign="top" width="16.91%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0167171797_p0823131242211"><a name="zh-cn_topic_0167171797_p0823131242211"></a><a name="zh-cn_topic_0167171797_p0823131242211"></a>无</p>
</td>
</tr>
<tr id="zh-cn_topic_0167171797_row151441212192316"><td class="cellrowborder" valign="top" width="16.48%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0167171797_p8145181210233"><a name="zh-cn_topic_0167171797_p8145181210233"></a><a name="zh-cn_topic_0167171797_p8145181210233"></a>CCI Viewer</p>
</td>
<td class="cellrowborder" valign="top" width="46.03%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0167171797_p1614591219235"><a name="zh-cn_topic_0167171797_p1614591219235"></a><a name="zh-cn_topic_0167171797_p1614591219235"></a>云容器实例只读权限，拥有该权限的用户仅能查看云容器实例资源。</p>
</td>
<td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0167171797_p914319473223"><a name="zh-cn_topic_0167171797_p914319473223"></a><a name="zh-cn_topic_0167171797_p914319473223"></a>细粒度策略</p>
</td>
<td class="cellrowborder" valign="top" width="16.91%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0167171797_p582314123221"><a name="zh-cn_topic_0167171797_p582314123221"></a><a name="zh-cn_topic_0167171797_p582314123221"></a>无</p>
</td>
</tr>
<tr id="zh-cn_topic_0167171797_row264417239235"><td class="cellrowborder" valign="top" width="16.48%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0167171797_p41073819195"><a name="zh-cn_topic_0167171797_p41073819195"></a><a name="zh-cn_topic_0167171797_p41073819195"></a>CCI Administrator</p>
</td>
<td class="cellrowborder" valign="top" width="46.03%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0167171797_p8104389194"><a name="zh-cn_topic_0167171797_p8104389194"></a><a name="zh-cn_topic_0167171797_p8104389194"></a>云容器实例管理员权限，拥有该权限的用户可以执行云容器实例所有资源的创建、删除、查询、更新操作。</p>
</td>
<td class="cellrowborder" valign="top" width="20.580000000000002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0167171797_p18143194716229"><a name="zh-cn_topic_0167171797_p18143194716229"></a><a name="zh-cn_topic_0167171797_p18143194716229"></a>RBAC策略</p>
</td>
<td class="cellrowborder" valign="top" width="16.91%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0167171797_p16431131115438"><a name="zh-cn_topic_0167171797_p16431131115438"></a><a name="zh-cn_topic_0167171797_p16431131115438"></a>无</p>
</td>
</tr>
</tbody>
</table>

## 步骤1：创建用户组并授权<a name="section11705979215"></a>

用户组是用户的集合，IAM通过用户组功能实现用户的授权。您在IAM中创建的用户，需要加入特定用户组后，用户才具备用户组所拥有的权限。关于创建用户组并给用户组授权的方法，可以参考如下操作。

1.  使用注册的华为云账号登录华为云，登录时请选择“账号登录”。

    **图 2**  登录<a name="fig1165220612567"></a>  
    ![](figures/登录.png "登录")

2.  进入华为云控制台， 控制台页面中单击右上角的用户名，选择“统一身份认证”。

    **图 3**  统一身份认证<a name="fig18391932175719"></a>  
    ![](figures/统一身份认证.png "统一身份认证")

3.  在统一身份认证服务的左侧导航空格中，单击“用户组”\>“创建用户组”。

    **图 4**  创建用户组<a name="fig1247792614360"></a>  
    ![](figures/创建用户组.png "创建用户组")

4.  在“创建用户组”界面，输入“用户组名称”，以“开发人员组”为例，单击“确定”。

    用户组创建完成，界面自动返回用户组列表，列表中显示新建的用户组。

5.  单击新建用户组右侧的“权限配置”。

    **图 5**  权限配置<a name="fig580512344366"></a>  
    ![](figures/权限配置.png "权限配置")

6.  在需要授权区域的所在行，单击“设置策略”。

    CCI为项目级服务，请确认用户需要使用CCI资源的项目，然后在对应项目中设置权限，则用户仅能访问授权项目中的CCI资源，无法访问其他项目中的CCI资源。

    **图 6**  设置策略-0<a name="fig6251481382"></a>  
    ![](figures/设置策略-0.png "设置策略-0")

7.  在“设置策略”中搜索“CCI”，选择“CCI Admin”。CCI的系统策略说明，请参见：[CCI系统策略](https://support.huaweicloud.com/productdesc-cci/cci_03_0008.html)。

    **图 7**  设置策略-1<a name="fig4101104613508"></a>  
    ![](figures/设置策略-1.png "设置策略-1")

8.  单击“确定”，完成用户组授权。

## 步骤2：创建IAM用户<a name="section5914125313212"></a>

IAM用户与企业中的实际员工或是应用程序相对应，有唯一的安全凭证，可以通过加入一个或多个用户组来获得用户组的权限。关于IAM用户的创建方式请参见如下步骤。

1.  在统一身份认证服务，左侧导航窗格中，单击“用户 \> 创建用户”。
2.  在“创建用户”页面填写“用户信息”。如需一次创建多个用户，可以单击“添加用户”进行批量创建，每次最多可创建10个用户。

    ![](figures/添加用户.png)

    -   用户名：用户登录华为云的用户名，以“James”为例。
    -   邮箱：IAM用户绑定的邮箱，仅“访问方式”选择“首次登录时设置”时必填，选择其他访问方式时选填。
    -   手机号（选填）：IAM用户绑定的手机号。
    -   描述（选填）：对用户的描述信息。

3.  在“创建用户”页面选择“访问方式”，完成后单击“下一步”。

    ![](figures/qwwwwwww.png)

    -   编程访问：创建用户完成后即可下载本次创建的所有用户的[访问密钥](https://support.huaweicloud.com/usermanual-ca/zh-cn_topic_0046606340.html)。
    -   华为云管理控制台访问：用户可以使用账号密码登录到华为云管理控制台。
        -   控制台登录密码设置方式：当一次创建多个用户时，密码设置方式可选择“首次登录时设置”和“自定义”，不支持“自动生成”密码；当仅创建一个用户时，以上方式均可选择。
        -   登录保护：为了您的账号安全，建议选择“开启登录保护”。后续如需开启或关闭登录保护，请参见：[登录保护](https://support.huaweicloud.com/usermanual-iam/zh-cn_topic_0079477316.html)。

4.  （可选）将用户加入到用户组，完成后单击“下一步”。
    -   选择新创建的用户组“开发人员组”。将用户加入用户组，用户将具备用户组的权限，这一过程即给该用户授权。其中“admin”为系统缺省提供的用户组，具有管理人员以及所有云服务资源的操作权限。
    -   如需创建新的用户组，可单击“创建用户组”，填写用户组名称和描述（可选），创建成功后即可将用户加入到新创建的用户组中。

5.  IAM用户创建成功，用户列表中显示新创建的IAM用户。如果在访问方式中勾选了“编程访问”，可在此页面下载访问密钥，后续也可以在“我的凭证”中[管理访问密钥](https://support.huaweicloud.com/usermanual-ca/zh-cn_topic_0046606340.html)。

    ![](figures/teser.png)


## 步骤3：用户登录并验证权限<a name="section12483530738"></a>

用户创建完成后，可以使用新用户的用户名及身份凭证登录华为云验证权限，即“CCI Admin”权限。更多用户登录方法请参见[用户登录华为云方法](https://support.huaweicloud.com/qs-iam/iam_01_0031.html#section2)。

1.  在华为云登录页面，单击右下角的“IAM用户登录”。

    ![](figures/1234456.png)

2.  在“IAM用户登录”页面，输入账号名、用户名及用户密码，使用新创建的用户登录。

    -   账号名为该IAM用户所属华为云账号的名称。
    -   用户名和密码为账号在IAM创建用户时输入的用户名和密码。

    如果登录失败，您可以联系您的账号主体，确认用户名及密码是否正确，或是重置用户名及密码，重置方法请参见：[忘记IAM用户密码](https://support.huaweicloud.com/iam_faq/iam_01_0314.html#section1)。

3.  登录成功后，进入华为云控制台，登录后默认区域为“华为-北京一”，请先切换至授权区域。

    ![](figures/授权区域.png)

4.  在“服务列表”中选择云容器实例，进入CCI主界面，左侧导航栏中选择“工作负载 \> 无状态（Deployment）“，在右侧页面单击“创建无状态负载“，如果能创建负载，说明权限设置成功。

