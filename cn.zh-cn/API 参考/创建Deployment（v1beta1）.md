# 创建Deployment<a name="cci_02_0025"></a>

## 功能介绍<a name="zh-cn_topic_0083864910_section15904123713483"></a>

该API用于创建一个Deployment资源对象。

## URI<a name="zh-cn_topic_0083864910_section764545414815"></a>

POST /apis/apps/v1beta1/namespaces/\{namespace\}/deployments

[表1 参数描述 ](#zh-cn_topic_0083864910_table167042013408)描述该API的参数。

**表 1**  参数描述

<a name="zh-cn_topic_0083864910_table167042013408"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row2067022020405"><th class="cellrowborder" valign="top" width="17.82178217821782%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0083864910_p65652297517"><a name="zh-cn_topic_0083864910_p65652297517"></a><a name="zh-cn_topic_0083864910_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22.772277227722775%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0083864910_p165661629135114"><a name="zh-cn_topic_0083864910_p165661629135114"></a><a name="zh-cn_topic_0083864910_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="59.4059405940594%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0083864910_p14567629115114"><a name="zh-cn_topic_0083864910_p14567629115114"></a><a name="zh-cn_topic_0083864910_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row1670122004014"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864910_p166701820144010"><a name="zh-cn_topic_0083864910_p166701820144010"></a><a name="zh-cn_topic_0083864910_p166701820144010"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864910_p14670122004017"><a name="zh-cn_topic_0083864910_p14670122004017"></a><a name="zh-cn_topic_0083864910_p14670122004017"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row136701220114011"><td class="cellrowborder" valign="top" width="17.82178217821782%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0083864910_p19670182074012"><a name="zh-cn_topic_0083864910_p19670182074012"></a><a name="zh-cn_topic_0083864910_p19670182074012"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="22.772277227722775%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0083864910_p196702020184012"><a name="zh-cn_topic_0083864910_p196702020184012"></a><a name="zh-cn_topic_0083864910_p196702020184012"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="59.4059405940594%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0083864910_p11670162004012"><a name="zh-cn_topic_0083864910_p11670162004012"></a><a name="zh-cn_topic_0083864910_p11670162004012"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0083864910_section24905416619"></a>

**请求参数**：

请求参数如[表2](#zh-cn_topic_0083864910_table12862324102610)所示。

**表 2**  请求参数

<a name="zh-cn_topic_0083864910_table12862324102610"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row68631424102610"><th class="cellrowborder" valign="top" width="17.01829817018298%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0083864910_zh-cn_topic_0083857388_zh-cn_topic_0079615000_p19784972"><a name="zh-cn_topic_0083864910_zh-cn_topic_0083857388_zh-cn_topic_0079615000_p19784972"></a><a name="zh-cn_topic_0083864910_zh-cn_topic_0083857388_zh-cn_topic_0079615000_p19784972"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.07839216078392%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0083864910_zh-cn_topic_0083857388_p62904453205444"><a name="zh-cn_topic_0083864910_zh-cn_topic_0083857388_p62904453205444"></a><a name="zh-cn_topic_0083864910_zh-cn_topic_0083857388_p62904453205444"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18.92810718928107%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0083864910_zh-cn_topic_0083857388_p62095922205444"><a name="zh-cn_topic_0083864910_zh-cn_topic_0083857388_p62095922205444"></a><a name="zh-cn_topic_0083864910_zh-cn_topic_0083857388_p62095922205444"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.97520247975203%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0083864910_zh-cn_topic_0083857388_p63713767205444"><a name="zh-cn_topic_0083864910_zh-cn_topic_0083857388_p63713767205444"></a><a name="zh-cn_topic_0083864910_zh-cn_topic_0083857388_p63713767205444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row386313249268"><td class="cellrowborder" valign="top" width="17.01829817018298%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p1986314247267"><a name="zh-cn_topic_0083864910_p1986314247267"></a><a name="zh-cn_topic_0083864910_p1986314247267"></a>apiVersion</p>
</td>
<td class="cellrowborder" valign="top" width="16.07839216078392%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p1486362472612"><a name="zh-cn_topic_0083864910_p1486362472612"></a><a name="zh-cn_topic_0083864910_p1486362472612"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="18.92810718928107%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p148631124192613"><a name="zh-cn_topic_0083864910_p148631124192613"></a><a name="zh-cn_topic_0083864910_p148631124192613"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.97520247975203%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p38631024132612"><a name="zh-cn_topic_0083864910_p38631024132612"></a><a name="zh-cn_topic_0083864910_p38631024132612"></a>APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row8863172412267"><td class="cellrowborder" valign="top" width="17.01829817018298%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p148638244268"><a name="zh-cn_topic_0083864910_p148638244268"></a><a name="zh-cn_topic_0083864910_p148638244268"></a>kind</p>
</td>
<td class="cellrowborder" valign="top" width="16.07839216078392%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p76386914116"><a name="zh-cn_topic_0083864910_p76386914116"></a><a name="zh-cn_topic_0083864910_p76386914116"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="18.92810718928107%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p1486372472613"><a name="zh-cn_topic_0083864910_p1486372472613"></a><a name="zh-cn_topic_0083864910_p1486372472613"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.97520247975203%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p1863112415264"><a name="zh-cn_topic_0083864910_p1863112415264"></a><a name="zh-cn_topic_0083864910_p1863112415264"></a>Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row9863724112610"><td class="cellrowborder" valign="top" width="17.01829817018298%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p686372411268"><a name="zh-cn_topic_0083864910_p686372411268"></a><a name="zh-cn_topic_0083864910_p686372411268"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="16.07839216078392%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p1312651084112"><a name="zh-cn_topic_0083864910_p1312651084112"></a><a name="zh-cn_topic_0083864910_p1312651084112"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="18.92810718928107%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p8864172472616"><a name="zh-cn_topic_0083864910_p8864172472616"></a><a name="zh-cn_topic_0083864910_p8864172472616"></a><a href="请求数据结构（OLD-VERSIONS）.md#zh-cn_topic_0083857342_zh-cn_topic_0079614925_table47756489">表10</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.97520247975203%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p6864112411261"><a name="zh-cn_topic_0083864910_p6864112411261"></a><a name="zh-cn_topic_0083864910_p6864112411261"></a>Standard object metadata.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row15864524102611"><td class="cellrowborder" valign="top" width="17.01829817018298%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p9864152411266"><a name="zh-cn_topic_0083864910_p9864152411266"></a><a name="zh-cn_topic_0083864910_p9864152411266"></a>spec</p>
</td>
<td class="cellrowborder" valign="top" width="16.07839216078392%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p4986110104112"><a name="zh-cn_topic_0083864910_p4986110104112"></a><a name="zh-cn_topic_0083864910_p4986110104112"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="18.92810718928107%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p8864142422612"><a name="zh-cn_topic_0083864910_p8864142422612"></a><a name="zh-cn_topic_0083864910_p8864142422612"></a><a href="#zh-cn_topic_0083864910_table15570752102811">表3</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.97520247975203%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p086472482619"><a name="zh-cn_topic_0083864910_p086472482619"></a><a name="zh-cn_topic_0083864910_p086472482619"></a>Specification of the desired behavior of the Deployment.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row78644248266"><td class="cellrowborder" valign="top" width="17.01829817018298%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p786418243264"><a name="zh-cn_topic_0083864910_p786418243264"></a><a name="zh-cn_topic_0083864910_p786418243264"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="16.07839216078392%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p3864112482611"><a name="zh-cn_topic_0083864910_p3864112482611"></a><a name="zh-cn_topic_0083864910_p3864112482611"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.92810718928107%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p586492412263"><a name="zh-cn_topic_0083864910_p586492412263"></a><a name="zh-cn_topic_0083864910_p586492412263"></a><a href="#zh-cn_topic_0083864910_table3226535203116">表4</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.97520247975203%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p9864162417264"><a name="zh-cn_topic_0083864910_p9864162417264"></a><a name="zh-cn_topic_0083864910_p9864162417264"></a>Most recently observed status of the Deployment. Read-only.</p>
</td>
</tr>
</tbody>
</table>

**表 3**  spec字段数据结构说明

<a name="zh-cn_topic_0083864910_table15570752102811"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row457055292811"><th class="cellrowborder" valign="top" width="17.24%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0083864910_p1745604817818"><a name="zh-cn_topic_0083864910_p1745604817818"></a><a name="zh-cn_topic_0083864910_p1745604817818"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.08%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0083864910_p046512488820"><a name="zh-cn_topic_0083864910_p046512488820"></a><a name="zh-cn_topic_0083864910_p046512488820"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0083864910_p104741648481"><a name="zh-cn_topic_0083864910_p104741648481"></a><a name="zh-cn_topic_0083864910_p104741648481"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.68%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0083864910_p15491184819810"><a name="zh-cn_topic_0083864910_p15491184819810"></a><a name="zh-cn_topic_0083864910_p15491184819810"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row4570125212286"><td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p15617156102917"><a name="zh-cn_topic_0083864910_p15617156102917"></a><a name="zh-cn_topic_0083864910_p15617156102917"></a>minReadySeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.08%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p196171162291"><a name="zh-cn_topic_0083864910_p196171162291"></a><a name="zh-cn_topic_0083864910_p196171162291"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p1461720642920"><a name="zh-cn_topic_0083864910_p1461720642920"></a><a name="zh-cn_topic_0083864910_p1461720642920"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p961746112911"><a name="zh-cn_topic_0083864910_p961746112911"></a><a name="zh-cn_topic_0083864910_p961746112911"></a>Minimum number of seconds for which a newly created pod should be ready without any of its containers crashing, for it to be considered available. Defaults to 0 (pod will be considered available as soon as it is ready)</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row18570145219282"><td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p06171614294"><a name="zh-cn_topic_0083864910_p06171614294"></a><a name="zh-cn_topic_0083864910_p06171614294"></a>paused</p>
</td>
<td class="cellrowborder" valign="top" width="16.08%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p26171263291"><a name="zh-cn_topic_0083864910_p26171263291"></a><a name="zh-cn_topic_0083864910_p26171263291"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p66174617297"><a name="zh-cn_topic_0083864910_p66174617297"></a><a name="zh-cn_topic_0083864910_p66174617297"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="47.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p1261715618295"><a name="zh-cn_topic_0083864910_p1261715618295"></a><a name="zh-cn_topic_0083864910_p1261715618295"></a>Indicates that the deployment is paused.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row1257055232819"><td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p1061716652918"><a name="zh-cn_topic_0083864910_p1061716652918"></a><a name="zh-cn_topic_0083864910_p1061716652918"></a>progressDeadlineSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="16.08%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p136185612293"><a name="zh-cn_topic_0083864910_p136185612293"></a><a name="zh-cn_topic_0083864910_p136185612293"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p1161815622910"><a name="zh-cn_topic_0083864910_p1161815622910"></a><a name="zh-cn_topic_0083864910_p1161815622910"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p17618961297"><a name="zh-cn_topic_0083864910_p17618961297"></a><a name="zh-cn_topic_0083864910_p17618961297"></a>The maximum time in seconds for a deployment to make progress before it is considered to be failed. The deployment controller will continue to process failed deployments and a condition with a ProgressDeadlineExceeded reason will be surfaced in the deployment status. Once autoRollback is implemented, the deployment controller will automatically rollback failed deployments. Note that progress will not be estimated during the time a deployment is paused. Defaults to 600s.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row4570175212287"><td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p136182612299"><a name="zh-cn_topic_0083864910_p136182612299"></a><a name="zh-cn_topic_0083864910_p136182612299"></a>replicas</p>
</td>
<td class="cellrowborder" valign="top" width="16.08%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p156184692916"><a name="zh-cn_topic_0083864910_p156184692916"></a><a name="zh-cn_topic_0083864910_p156184692916"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p19618156152920"><a name="zh-cn_topic_0083864910_p19618156152920"></a><a name="zh-cn_topic_0083864910_p19618156152920"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p761818692914"><a name="zh-cn_topic_0083864910_p761818692914"></a><a name="zh-cn_topic_0083864910_p761818692914"></a>Number of desired pods. This is a pointer to distinguish between explicit zero and not specified. Defaults to 1.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row16571252142813"><td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p13618136202911"><a name="zh-cn_topic_0083864910_p13618136202911"></a><a name="zh-cn_topic_0083864910_p13618136202911"></a>revisionHistoryLimit</p>
</td>
<td class="cellrowborder" valign="top" width="16.08%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p96181069296"><a name="zh-cn_topic_0083864910_p96181069296"></a><a name="zh-cn_topic_0083864910_p96181069296"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p961836122910"><a name="zh-cn_topic_0083864910_p961836122910"></a><a name="zh-cn_topic_0083864910_p961836122910"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p8351621935"><a name="zh-cn_topic_0083864910_p8351621935"></a><a name="zh-cn_topic_0083864910_p8351621935"></a></p>
<p id="zh-cn_topic_0083864910_p1761815614291"><a name="zh-cn_topic_0083864910_p1761815614291"></a><a name="zh-cn_topic_0083864910_p1761815614291"></a>The number of old ReplicaSets to retain to allow rollback. This is a pointer to distinguish between explicit zero and not specified. Defaults to 2.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row25715521289"><td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p461866132918"><a name="zh-cn_topic_0083864910_p461866132918"></a><a name="zh-cn_topic_0083864910_p461866132918"></a>rollbackTo</p>
</td>
<td class="cellrowborder" valign="top" width="16.08%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p206181610290"><a name="zh-cn_topic_0083864910_p206181610290"></a><a name="zh-cn_topic_0083864910_p206181610290"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p78567169339"><a name="zh-cn_topic_0083864910_p78567169339"></a><a name="zh-cn_topic_0083864910_p78567169339"></a><a href="#zh-cn_topic_0083864910_table38158357321">表5</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p46191365294"><a name="zh-cn_topic_0083864910_p46191365294"></a><a name="zh-cn_topic_0083864910_p46191365294"></a>The config this deployment is rolling back to. Will be cleared after rollback is done.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row557165219282"><td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p1861914682913"><a name="zh-cn_topic_0083864910_p1861914682913"></a><a name="zh-cn_topic_0083864910_p1861914682913"></a>selector</p>
</td>
<td class="cellrowborder" valign="top" width="16.08%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p10619126192913"><a name="zh-cn_topic_0083864910_p10619126192913"></a><a name="zh-cn_topic_0083864910_p10619126192913"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p138907188364"><a name="zh-cn_topic_0083864910_p138907188364"></a><a name="zh-cn_topic_0083864910_p138907188364"></a><a href="#zh-cn_topic_0083864910_table5344134293516">表6</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p156190611293"><a name="zh-cn_topic_0083864910_p156190611293"></a><a name="zh-cn_topic_0083864910_p156190611293"></a>Label selector for pods. Existing ReplicaSets whose pods are selected by this will be the ones affected by this deployment.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row1757135214288"><td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p76191760292"><a name="zh-cn_topic_0083864910_p76191760292"></a><a name="zh-cn_topic_0083864910_p76191760292"></a>strategy</p>
</td>
<td class="cellrowborder" valign="top" width="16.08%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p361936172916"><a name="zh-cn_topic_0083864910_p361936172916"></a><a name="zh-cn_topic_0083864910_p361936172916"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p1619116122915"><a name="zh-cn_topic_0083864910_p1619116122915"></a><a name="zh-cn_topic_0083864910_p1619116122915"></a><a href="#zh-cn_topic_0083864910_table10348336183618">表7</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p361915616297"><a name="zh-cn_topic_0083864910_p361915616297"></a><a name="zh-cn_topic_0083864910_p361915616297"></a>The deployment strategy to use to replace existing pods with new ones.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row4571145219283"><td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p1861913692914"><a name="zh-cn_topic_0083864910_p1861913692914"></a><a name="zh-cn_topic_0083864910_p1861913692914"></a>template</p>
</td>
<td class="cellrowborder" valign="top" width="16.08%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p19619176142914"><a name="zh-cn_topic_0083864910_p19619176142914"></a><a name="zh-cn_topic_0083864910_p19619176142914"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p1849772214710"><a name="zh-cn_topic_0083864910_p1849772214710"></a><a name="zh-cn_topic_0083864910_p1849772214710"></a><a href="请求数据结构（OLD-VERSIONS）.md#zh-cn_topic_0083857342_zh-cn_topic_0079614925_table52089545">表20</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.68%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p361914615293"><a name="zh-cn_topic_0083864910_p361914615293"></a><a name="zh-cn_topic_0083864910_p361914615293"></a>Template describes the pods that will be created.</p>
</td>
</tr>
</tbody>
</table>

**表 4**  status字段数据结构说明

<a name="zh-cn_topic_0083864910_table3226535203116"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row162271135153117"><th class="cellrowborder" valign="top" width="17.378262173782623%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0083864910_p186516551182"><a name="zh-cn_topic_0083864910_p186516551182"></a><a name="zh-cn_topic_0083864910_p186516551182"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.828417158284172%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0083864910_p107515551089"><a name="zh-cn_topic_0083864910_p107515551089"></a><a name="zh-cn_topic_0083864910_p107515551089"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18.998100189981002%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0083864910_p15881655682"><a name="zh-cn_topic_0083864910_p15881655682"></a><a name="zh-cn_topic_0083864910_p15881655682"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.795220477952206%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0083864910_p69835516817"><a name="zh-cn_topic_0083864910_p69835516817"></a><a name="zh-cn_topic_0083864910_p69835516817"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row722703513115"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p7770135423110"><a name="zh-cn_topic_0083864910_p7770135423110"></a><a name="zh-cn_topic_0083864910_p7770135423110"></a>availableReplicas</p>
</td>
<td class="cellrowborder" valign="top" width="15.828417158284172%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p77701754123116"><a name="zh-cn_topic_0083864910_p77701754123116"></a><a name="zh-cn_topic_0083864910_p77701754123116"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.998100189981002%" headers="mcps1.2.5.1.3 "><p id="p520412371419"><a name="p520412371419"></a><a name="p520412371419"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.795220477952206%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p17706543314"><a name="zh-cn_topic_0083864910_p17706543314"></a><a name="zh-cn_topic_0083864910_p17706543314"></a>Total number of available pods (ready for at least minReadySeconds) targeted by this deployment.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row222703573119"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p1577045419318"><a name="zh-cn_topic_0083864910_p1577045419318"></a><a name="zh-cn_topic_0083864910_p1577045419318"></a>collisionCount</p>
</td>
<td class="cellrowborder" valign="top" width="15.828417158284172%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p1770105416310"><a name="zh-cn_topic_0083864910_p1770105416310"></a><a name="zh-cn_topic_0083864910_p1770105416310"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.998100189981002%" headers="mcps1.2.5.1.3 "><p id="p10225123714119"><a name="p10225123714119"></a><a name="p10225123714119"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.795220477952206%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p18234152173017"><a name="zh-cn_topic_0083864910_p18234152173017"></a><a name="zh-cn_topic_0083864910_p18234152173017"></a></p>
<p id="zh-cn_topic_0083864910_p1477014546311"><a name="zh-cn_topic_0083864910_p1477014546311"></a><a name="zh-cn_topic_0083864910_p1477014546311"></a>Count of hash collisions for the Deployment. The Deployment controller uses this field as a collision avoidance mechanism when it needs to create the name for the newest ReplicaSet.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row13227123593111"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p7770354203113"><a name="zh-cn_topic_0083864910_p7770354203113"></a><a name="zh-cn_topic_0083864910_p7770354203113"></a>conditions</p>
</td>
<td class="cellrowborder" valign="top" width="15.828417158284172%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p377012542314"><a name="zh-cn_topic_0083864910_p377012542314"></a><a name="zh-cn_topic_0083864910_p377012542314"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.998100189981002%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p5707133213438"><a name="zh-cn_topic_0083864910_p5707133213438"></a><a name="zh-cn_topic_0083864910_p5707133213438"></a><a href="#zh-cn_topic_0083864910_table2173152418384">表8</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.795220477952206%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p15770105413316"><a name="zh-cn_topic_0083864910_p15770105413316"></a><a name="zh-cn_topic_0083864910_p15770105413316"></a>Represents the latest available observations of a deployment's current state.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row922733533115"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p1977014542315"><a name="zh-cn_topic_0083864910_p1977014542315"></a><a name="zh-cn_topic_0083864910_p1977014542315"></a>observedGeneration</p>
</td>
<td class="cellrowborder" valign="top" width="15.828417158284172%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p13770105419318"><a name="zh-cn_topic_0083864910_p13770105419318"></a><a name="zh-cn_topic_0083864910_p13770105419318"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.998100189981002%" headers="mcps1.2.5.1.3 "><p id="p4483183911415"><a name="p4483183911415"></a><a name="p4483183911415"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.795220477952206%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p197709544316"><a name="zh-cn_topic_0083864910_p197709544316"></a><a name="zh-cn_topic_0083864910_p197709544316"></a>The generation observed by the deployment controller</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row2227143519311"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p10770205413314"><a name="zh-cn_topic_0083864910_p10770205413314"></a><a name="zh-cn_topic_0083864910_p10770205413314"></a>readyReplicas</p>
</td>
<td class="cellrowborder" valign="top" width="15.828417158284172%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p11770154173115"><a name="zh-cn_topic_0083864910_p11770154173115"></a><a name="zh-cn_topic_0083864910_p11770154173115"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.998100189981002%" headers="mcps1.2.5.1.3 "><p id="p949523914418"><a name="p949523914418"></a><a name="p949523914418"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.795220477952206%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p14770145414316"><a name="zh-cn_topic_0083864910_p14770145414316"></a><a name="zh-cn_topic_0083864910_p14770145414316"></a>Total number of ready pods targeted by this deployment</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row12271235143114"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p4770115412311"><a name="zh-cn_topic_0083864910_p4770115412311"></a><a name="zh-cn_topic_0083864910_p4770115412311"></a>replicas</p>
</td>
<td class="cellrowborder" valign="top" width="15.828417158284172%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p577112540319"><a name="zh-cn_topic_0083864910_p577112540319"></a><a name="zh-cn_topic_0083864910_p577112540319"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.998100189981002%" headers="mcps1.2.5.1.3 "><p id="p1651063924120"><a name="p1651063924120"></a><a name="p1651063924120"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.795220477952206%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p8771185414313"><a name="zh-cn_topic_0083864910_p8771185414313"></a><a name="zh-cn_topic_0083864910_p8771185414313"></a>Total number of non-terminated pods targeted by this deployment (their labels match the selector).</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row22281835203110"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p107718541314"><a name="zh-cn_topic_0083864910_p107718541314"></a><a name="zh-cn_topic_0083864910_p107718541314"></a>unavailableReplicas</p>
</td>
<td class="cellrowborder" valign="top" width="15.828417158284172%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p2077110546313"><a name="zh-cn_topic_0083864910_p2077110546313"></a><a name="zh-cn_topic_0083864910_p2077110546313"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.998100189981002%" headers="mcps1.2.5.1.3 "><p id="p7513164104117"><a name="p7513164104117"></a><a name="p7513164104117"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.795220477952206%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p6771115483111"><a name="zh-cn_topic_0083864910_p6771115483111"></a><a name="zh-cn_topic_0083864910_p6771115483111"></a>Total number of unavailable pods targeted by this deployment.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row102281735193120"><td class="cellrowborder" valign="top" width="17.378262173782623%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p10771175433111"><a name="zh-cn_topic_0083864910_p10771175433111"></a><a name="zh-cn_topic_0083864910_p10771175433111"></a>updatedReplicas</p>
</td>
<td class="cellrowborder" valign="top" width="15.828417158284172%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p1777155423110"><a name="zh-cn_topic_0083864910_p1777155423110"></a><a name="zh-cn_topic_0083864910_p1777155423110"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.998100189981002%" headers="mcps1.2.5.1.3 "><p id="p75291741194117"><a name="p75291741194117"></a><a name="p75291741194117"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.795220477952206%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p10771105413317"><a name="zh-cn_topic_0083864910_p10771105413317"></a><a name="zh-cn_topic_0083864910_p10771105413317"></a>Total number of non-terminated pods targeted by this deployment that have the desired template spec.</p>
</td>
</tr>
</tbody>
</table>

**表 5**  rollbackTo字段数据结构说明

<a name="zh-cn_topic_0083864910_table38158357321"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row19816735143214"><th class="cellrowborder" valign="top" width="17.078292170782923%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0083864910_p237555920814"><a name="zh-cn_topic_0083864910_p237555920814"></a><a name="zh-cn_topic_0083864910_p237555920814"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.258374162583742%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0083864910_p338415916810"><a name="zh-cn_topic_0083864910_p338415916810"></a><a name="zh-cn_topic_0083864910_p338415916810"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18.95810418958104%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0083864910_p93912591082"><a name="zh-cn_topic_0083864910_p93912591082"></a><a name="zh-cn_topic_0083864910_p93912591082"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.7052294770523%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0083864910_p1400185912814"><a name="zh-cn_topic_0083864910_p1400185912814"></a><a name="zh-cn_topic_0083864910_p1400185912814"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row1181643511323"><td class="cellrowborder" valign="top" width="17.078292170782923%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p714245073218"><a name="zh-cn_topic_0083864910_p714245073218"></a><a name="zh-cn_topic_0083864910_p714245073218"></a>revision</p>
</td>
<td class="cellrowborder" valign="top" width="16.258374162583742%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p2014218504328"><a name="zh-cn_topic_0083864910_p2014218504328"></a><a name="zh-cn_topic_0083864910_p2014218504328"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.95810418958104%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p714216500323"><a name="zh-cn_topic_0083864910_p714216500323"></a><a name="zh-cn_topic_0083864910_p714216500323"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.7052294770523%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p81425509322"><a name="zh-cn_topic_0083864910_p81425509322"></a><a name="zh-cn_topic_0083864910_p81425509322"></a>The revision to rollback to. If set to 0, rollback to the last revision.</p>
</td>
</tr>
</tbody>
</table>

**表 6**  selector字段数据结构说明

<a name="zh-cn_topic_0083864910_table5344134293516"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row534520429359"><th class="cellrowborder" valign="top" width="17.071707170717072%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0083864910_p719318520913"><a name="zh-cn_topic_0083864910_p719318520913"></a><a name="zh-cn_topic_0083864910_p719318520913"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.2016201620162%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0083864910_p172011251691"><a name="zh-cn_topic_0083864910_p172011251691"></a><a name="zh-cn_topic_0083864910_p172011251691"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="18.801880188018803%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0083864910_p4212351298"><a name="zh-cn_topic_0083864910_p4212351298"></a><a name="zh-cn_topic_0083864910_p4212351298"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.92479247924793%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0083864910_p5221851899"><a name="zh-cn_topic_0083864910_p5221851899"></a><a name="zh-cn_topic_0083864910_p5221851899"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row6345184212356"><td class="cellrowborder" valign="top" width="17.071707170717072%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p944819019361"><a name="zh-cn_topic_0083864910_p944819019361"></a><a name="zh-cn_topic_0083864910_p944819019361"></a>matchExpressions</p>
</td>
<td class="cellrowborder" valign="top" width="16.2016201620162%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p1144815011368"><a name="zh-cn_topic_0083864910_p1144815011368"></a><a name="zh-cn_topic_0083864910_p1144815011368"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.801880188018803%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p1744810113613"><a name="zh-cn_topic_0083864910_p1744810113613"></a><a name="zh-cn_topic_0083864910_p1744810113613"></a><a href="#table96731180568">表9</a></p>
</td>
<td class="cellrowborder" valign="top" width="47.92479247924793%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p744813073619"><a name="zh-cn_topic_0083864910_p744813073619"></a><a name="zh-cn_topic_0083864910_p744813073619"></a>matchExpressions is a list of label selector requirements. The requirements are ANDed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row3345164233517"><td class="cellrowborder" valign="top" width="17.071707170717072%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p194481063618"><a name="zh-cn_topic_0083864910_p194481063618"></a><a name="zh-cn_topic_0083864910_p194481063618"></a>matchLabels</p>
</td>
<td class="cellrowborder" valign="top" width="16.2016201620162%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p184481017368"><a name="zh-cn_topic_0083864910_p184481017368"></a><a name="zh-cn_topic_0083864910_p184481017368"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="18.801880188018803%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p2044820153610"><a name="zh-cn_topic_0083864910_p2044820153610"></a><a name="zh-cn_topic_0083864910_p2044820153610"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="47.92479247924793%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p154481302365"><a name="zh-cn_topic_0083864910_p154481302365"></a><a name="zh-cn_topic_0083864910_p154481302365"></a>matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.</p>
</td>
</tr>
</tbody>
</table>

**表 7**  strategy字段数据结构说明

<a name="zh-cn_topic_0083864910_table10348336183618"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row1134893616361"><th class="cellrowborder" valign="top" width="17%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0083864910_p582213142912"><a name="zh-cn_topic_0083864910_p582213142912"></a><a name="zh-cn_topic_0083864910_p582213142912"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0083864910_p583310141595"><a name="zh-cn_topic_0083864910_p583310141595"></a><a name="zh-cn_topic_0083864910_p583310141595"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0083864910_p68451414897"><a name="zh-cn_topic_0083864910_p68451414897"></a><a name="zh-cn_topic_0083864910_p68451414897"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="48%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0083864910_p14859814891"><a name="zh-cn_topic_0083864910_p14859814891"></a><a name="zh-cn_topic_0083864910_p14859814891"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row934963683617"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p878476133714"><a name="zh-cn_topic_0083864910_p878476133714"></a><a name="zh-cn_topic_0083864910_p878476133714"></a>rollingUpdate</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p97843653716"><a name="zh-cn_topic_0083864910_p97843653716"></a><a name="zh-cn_topic_0083864910_p97843653716"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p19720175165913"><a name="zh-cn_topic_0083864910_p19720175165913"></a><a name="zh-cn_topic_0083864910_p19720175165913"></a><a href="#zh-cn_topic_0083864910_table890691614586">表10</a></p>
</td>
<td class="cellrowborder" valign="top" width="48%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p17842616373"><a name="zh-cn_topic_0083864910_p17842616373"></a><a name="zh-cn_topic_0083864910_p17842616373"></a>Rolling update config params. Present only if DeploymentStrategyType = RollingUpdate.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row2034916369362"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p20784965372"><a name="zh-cn_topic_0083864910_p20784965372"></a><a name="zh-cn_topic_0083864910_p20784965372"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="16%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p127848613719"><a name="zh-cn_topic_0083864910_p127848613719"></a><a name="zh-cn_topic_0083864910_p127848613719"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p778436123715"><a name="zh-cn_topic_0083864910_p778436123715"></a><a name="zh-cn_topic_0083864910_p778436123715"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p37841653711"><a name="zh-cn_topic_0083864910_p37841653711"></a><a name="zh-cn_topic_0083864910_p37841653711"></a>Type of deployment. Can be "Recreate" or "RollingUpdate". Default is RollingUpdate.</p>
</td>
</tr>
</tbody>
</table>

**表 8**  conditions字段数据结构说明

<a name="zh-cn_topic_0083864910_table2173152418384"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row2173224153814"><th class="cellrowborder" valign="top" width="17.23%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0083864910_p132092172915"><a name="zh-cn_topic_0083864910_p132092172915"></a><a name="zh-cn_topic_0083864910_p132092172915"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.959999999999999%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0083864910_p192215171194"><a name="zh-cn_topic_0083864910_p192215171194"></a><a name="zh-cn_topic_0083864910_p192215171194"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.17%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0083864910_p923313171796"><a name="zh-cn_topic_0083864910_p923313171796"></a><a name="zh-cn_topic_0083864910_p923313171796"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.64%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0083864910_p924521711912"><a name="zh-cn_topic_0083864910_p924521711912"></a><a name="zh-cn_topic_0083864910_p924521711912"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row1317317240385"><td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p164612382388"><a name="zh-cn_topic_0083864910_p164612382388"></a><a name="zh-cn_topic_0083864910_p164612382388"></a>lastTransitionTime</p>
</td>
<td class="cellrowborder" valign="top" width="15.959999999999999%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p1464617388382"><a name="zh-cn_topic_0083864910_p1464617388382"></a><a name="zh-cn_topic_0083864910_p1464617388382"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p76461238143813"><a name="zh-cn_topic_0083864910_p76461238143813"></a><a name="zh-cn_topic_0083864910_p76461238143813"></a>Time</p>
</td>
<td class="cellrowborder" valign="top" width="47.64%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p8646838173813"><a name="zh-cn_topic_0083864910_p8646838173813"></a><a name="zh-cn_topic_0083864910_p8646838173813"></a>Last time the condition transitioned from one status to another.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row131740244384"><td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p14646123819381"><a name="zh-cn_topic_0083864910_p14646123819381"></a><a name="zh-cn_topic_0083864910_p14646123819381"></a>lastUpdateTime</p>
</td>
<td class="cellrowborder" valign="top" width="15.959999999999999%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p1564633813385"><a name="zh-cn_topic_0083864910_p1564633813385"></a><a name="zh-cn_topic_0083864910_p1564633813385"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p1864615387381"><a name="zh-cn_topic_0083864910_p1864615387381"></a><a name="zh-cn_topic_0083864910_p1864615387381"></a>Time</p>
</td>
<td class="cellrowborder" valign="top" width="47.64%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p12646173816383"><a name="zh-cn_topic_0083864910_p12646173816383"></a><a name="zh-cn_topic_0083864910_p12646173816383"></a>The last time this condition was updated.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row13174124123814"><td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p12646838133815"><a name="zh-cn_topic_0083864910_p12646838133815"></a><a name="zh-cn_topic_0083864910_p12646838133815"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="15.959999999999999%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p11646163893819"><a name="zh-cn_topic_0083864910_p11646163893819"></a><a name="zh-cn_topic_0083864910_p11646163893819"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p2647173811388"><a name="zh-cn_topic_0083864910_p2647173811388"></a><a name="zh-cn_topic_0083864910_p2647173811388"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.64%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p1064773843816"><a name="zh-cn_topic_0083864910_p1064773843816"></a><a name="zh-cn_topic_0083864910_p1064773843816"></a>A human readable message indicating details about the transition.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row817492473812"><td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p146471738113811"><a name="zh-cn_topic_0083864910_p146471738113811"></a><a name="zh-cn_topic_0083864910_p146471738113811"></a>reason</p>
</td>
<td class="cellrowborder" valign="top" width="15.959999999999999%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p156471038143813"><a name="zh-cn_topic_0083864910_p156471038143813"></a><a name="zh-cn_topic_0083864910_p156471038143813"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p5647103816385"><a name="zh-cn_topic_0083864910_p5647103816385"></a><a name="zh-cn_topic_0083864910_p5647103816385"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.64%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p6647143815384"><a name="zh-cn_topic_0083864910_p6647143815384"></a><a name="zh-cn_topic_0083864910_p6647143815384"></a>The reason for the condition's last transition.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row11747243386"><td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p1064723833816"><a name="zh-cn_topic_0083864910_p1064723833816"></a><a name="zh-cn_topic_0083864910_p1064723833816"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="15.959999999999999%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p3647113833811"><a name="zh-cn_topic_0083864910_p3647113833811"></a><a name="zh-cn_topic_0083864910_p3647113833811"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p20647638173812"><a name="zh-cn_topic_0083864910_p20647638173812"></a><a name="zh-cn_topic_0083864910_p20647638173812"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.64%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p16471338163813"><a name="zh-cn_topic_0083864910_p16471338163813"></a><a name="zh-cn_topic_0083864910_p16471338163813"></a>Status of the condition, one of True, False, Unknown.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row2174724103810"><td class="cellrowborder" valign="top" width="17.23%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p6647638183810"><a name="zh-cn_topic_0083864910_p6647638183810"></a><a name="zh-cn_topic_0083864910_p6647638183810"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="15.959999999999999%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p16647113814389"><a name="zh-cn_topic_0083864910_p16647113814389"></a><a name="zh-cn_topic_0083864910_p16647113814389"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p18647638153813"><a name="zh-cn_topic_0083864910_p18647638153813"></a><a name="zh-cn_topic_0083864910_p18647638153813"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.64%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p20647143817386"><a name="zh-cn_topic_0083864910_p20647143817386"></a><a name="zh-cn_topic_0083864910_p20647143817386"></a>Type of deployment condition.</p>
</td>
</tr>
</tbody>
</table>

**表 9**  matchExpressions字段数据结构说明

<a name="table96731180568"></a>
<table><thead align="left"><tr id="row9694118105616"><th class="cellrowborder" valign="top" width="17.43%" id="mcps1.2.5.1.1"><p id="p8700882564"><a name="p8700882564"></a><a name="p8700882564"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.93%" id="mcps1.2.5.1.2"><p id="p117042855619"><a name="p117042855619"></a><a name="p117042855619"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.12%" id="mcps1.2.5.1.3"><p id="p1670915812565"><a name="p1670915812565"></a><a name="p1670915812565"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.52%" id="mcps1.2.5.1.4"><p id="p871318135611"><a name="p871318135611"></a><a name="p871318135611"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row17184819566"><td class="cellrowborder" valign="top" width="17.43%" headers="mcps1.2.5.1.1 "><p id="p147229813565"><a name="p147229813565"></a><a name="p147229813565"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="15.93%" headers="mcps1.2.5.1.2 "><p id="p472748135613"><a name="p472748135613"></a><a name="p472748135613"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.2.5.1.3 "><p id="p157291819561"><a name="p157291819561"></a><a name="p157291819561"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.52%" headers="mcps1.2.5.1.4 "><p id="p1973498155620"><a name="p1973498155620"></a><a name="p1973498155620"></a>key is the label key that the selector applies to.</p>
</td>
</tr>
<tr id="row273508135615"><td class="cellrowborder" valign="top" width="17.43%" headers="mcps1.2.5.1.1 "><p id="p17394865619"><a name="p17394865619"></a><a name="p17394865619"></a>operator</p>
</td>
<td class="cellrowborder" valign="top" width="15.93%" headers="mcps1.2.5.1.2 "><p id="p674217855611"><a name="p674217855611"></a><a name="p674217855611"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.2.5.1.3 "><p id="p9746108105619"><a name="p9746108105619"></a><a name="p9746108105619"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="47.52%" headers="mcps1.2.5.1.4 "><p id="p187495845610"><a name="p187495845610"></a><a name="p187495845610"></a>operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.</p>
</td>
</tr>
<tr id="row10752284569"><td class="cellrowborder" valign="top" width="17.43%" headers="mcps1.2.5.1.1 "><p id="p1775513812568"><a name="p1775513812568"></a><a name="p1775513812568"></a>values</p>
</td>
<td class="cellrowborder" valign="top" width="15.93%" headers="mcps1.2.5.1.2 "><p id="p20760681569"><a name="p20760681569"></a><a name="p20760681569"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.2.5.1.3 "><p id="p1476348195612"><a name="p1476348195612"></a><a name="p1476348195612"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="47.52%" headers="mcps1.2.5.1.4 "><p id="p147661687564"><a name="p147661687564"></a><a name="p147661687564"></a>values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.</p>
</td>
</tr>
</tbody>
</table>

**表 10**  RollingUpateDeployment字段数据结构说明

<a name="zh-cn_topic_0083864910_table890691614586"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row1892421675817"><th class="cellrowborder" valign="top" width="17.43%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0083864910_p991719241897"><a name="zh-cn_topic_0083864910_p991719241897"></a><a name="zh-cn_topic_0083864910_p991719241897"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.93%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0083864910_p20924224396"><a name="zh-cn_topic_0083864910_p20924224396"></a><a name="zh-cn_topic_0083864910_p20924224396"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.12%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0083864910_p19934202412920"><a name="zh-cn_topic_0083864910_p19934202412920"></a><a name="zh-cn_topic_0083864910_p19934202412920"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="47.52%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0083864910_p4948102417917"><a name="zh-cn_topic_0083864910_p4948102417917"></a><a name="zh-cn_topic_0083864910_p4948102417917"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row694815168581"><td class="cellrowborder" valign="top" width="17.43%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p4952181618587"><a name="zh-cn_topic_0083864910_p4952181618587"></a><a name="zh-cn_topic_0083864910_p4952181618587"></a>maxSurge</p>
</td>
<td class="cellrowborder" valign="top" width="15.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p11955121645820"><a name="zh-cn_topic_0083864910_p11955121645820"></a><a name="zh-cn_topic_0083864910_p11955121645820"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p1295919168584"><a name="zh-cn_topic_0083864910_p1295919168584"></a><a name="zh-cn_topic_0083864910_p1295919168584"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.52%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p5963121610580"><a name="zh-cn_topic_0083864910_p5963121610580"></a><a name="zh-cn_topic_0083864910_p5963121610580"></a>The maximum number of pods that can be scheduled above the desired number of pods. Value can be an absolute number (ex: 5) or a percentage of desired pods (ex: 10%). This cannot be 0 if MaxUnavailable is 0. Absolute number is calculated from percentage by rounding up. Defaults to 25%. Example: when this is set to 30%, the new RC can be scaled up immediately when the rolling update starts, such that the total number of old and new pods do not exceed 130% of desired pods. Once old pods have been killed, new RC can be scaled up further, ensuring that total number of pods running at any time during the update is at most 130% of desired pods.</p>
</td>
</tr>
<tr id="zh-cn_topic_0083864910_row1496614166583"><td class="cellrowborder" valign="top" width="17.43%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0083864910_p1997013167589"><a name="zh-cn_topic_0083864910_p1997013167589"></a><a name="zh-cn_topic_0083864910_p1997013167589"></a>maxUnavailable</p>
</td>
<td class="cellrowborder" valign="top" width="15.93%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0083864910_p4975161635818"><a name="zh-cn_topic_0083864910_p4975161635818"></a><a name="zh-cn_topic_0083864910_p4975161635818"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0083864910_p497801645820"><a name="zh-cn_topic_0083864910_p497801645820"></a><a name="zh-cn_topic_0083864910_p497801645820"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="47.52%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0083864910_p66201122115917"><a name="zh-cn_topic_0083864910_p66201122115917"></a><a name="zh-cn_topic_0083864910_p66201122115917"></a>The maximum number of pods that can be unavailable during the update. Value can be an absolute number (ex: 5) or a percentage of desired pods (ex: 10%). Absolute number is calculated from percentage by rounding down. This cannot be 0 if MaxSurge is 0. Defaults to 25%. Example: when this is set to 30%, the old RC can be scaled down to 70% of desired pods immediately when the rolling update starts. Once new pods are ready, old RC can be scaled down further, followed by scaling up the new RC, ensuring that the total number of pods available at all times during the update is at least 70% of desired pods.</p>
</td>
</tr>
</tbody>
</table>

**请求示例：**

```
{
    "apiVersion": "apps/v1beta1", 
    "kind": "Deployment", 
    "metadata": {
        "annotations": {
            "description": ""
        }, 
        "labels": {
            "appgroup": ""
        }, 
        "name": "deployment-test"
    }, 
    "spec": {
        "replicas": 1, 
        "selector": {
            "matchLabels": {
                "app": "deployment-test"
            }
        }, 
        "template": {
            "metadata": {
                "annotations": {
                    "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]", 
                    "com.huawei.scheduler/container-type": "secure-container"
                }, 
                "labels": {
                    "app": "deployment-test"
                }
            }, 
            "spec": {
                "containers": [
                    {
                        "image": "nginx:latest", 
                        "name": "container-0", 
                        "resources": {
                            "limits": {
                                "cpu": "500m", 
                                "memory": "1024Mi"
                            }, 
                            "requests": {
                                "cpu": "500m", 
                                "memory": "1024Mi"
                            }
                        }, 
                        "lifecycle": {}
                    }
                ], 
                "imagePullSecrets": [
                    {
                        "name": "imagepull-secret"
                    }
                ], 
                "affinity": {}
            }
        }, 
        "minReadySeconds": 0, 
        "strategy": {
            "type": "RollingUpdate", 
            "rollingUpdate": {
                "maxSurge": 0, 
                "maxUnavailable": 1
            }
        }
    }
}
```

## 响应消息<a name="zh-cn_topic_0083864910_section1575712476123"></a>

**响应参数**：

响应参数如[表2](#zh-cn_topic_0083864910_table12862324102610)所示。

**响应示例：**

```
{
    "kind": "Deployment", 
    "apiVersion": "apps/v1beta1", 
    "metadata": {
        "name": "deployment-test", 
        "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
        "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/deployments/deployment-test", 
        "uid": "ed89a51c-2728-11e8-b891-84a9c46e8c8b", 
        "resourceVersion": "4510929", 
        "generation": 1, 
        "creationTimestamp": "2018-03-14T01:42:17Z", 
        "labels": {
            "appgroup": ""
        }, 
        "annotations": {
            "description": ""
        }, 
        "enable": true
    }, 
    "spec": {
        "replicas": 1, 
        "selector": {
            "matchLabels": {
                "app": "deployment-test"
            }
        }, 
        "template": {
            "metadata": {
                "creationTimestamp": null, 
                "labels": {
                    "app": "deployment-test"
                }, 
                "annotations": {
                    "com.huawei.scheduler/container-type": "secure-container", 
                    "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]"
                }, 
                "enable": true
            }, 
            "spec": {
                "containers": [
                    {
                        "name": "container-0", 
                        "image": "nginx:latest", 
                        "resources": {
                            "limits": {
                                "cpu": "1", 
                                "memory": "1024Mi"
                            }, 
                            "requests": {
                                "cpu": "1", 
                                "memory": "1024Mi"
                            }
                        }, 
                        "lifecycle": {}, 
                        "terminationMessagePath": "/dev/termination-log", 
                        "terminationMessagePolicy": "File", 
                        "imagePullPolicy": "Always"
                    }
                ], 
                "restartPolicy": "Always", 
                "terminationGracePeriodSeconds": 30, 
                "dnsPolicy": "ClusterFirst", 
                "securityContext": {}, 
                "imagePullSecrets": [
                    {
                        "name": "imagepull-secret"
                    }
                ], 
                "affinity": {}, 
                "schedulerName": "default-scheduler"
            }
        }, 
        "strategy": {
            "type": "RollingUpdate", 
            "rollingUpdate": {
                "maxUnavailable": 1, 
                "maxSurge": 0
            }
        }, 
        "revisionHistoryLimit": 2, 
        "progressDeadlineSeconds": 600
    }, 
    "status": {}
}
```

## 状态码<a name="zh-cn_topic_0083864910_section16509142112516"></a>

[表11 状态码](#zh-cn_topic_0083864910_table6957182913514)描述API的状态码。

**表 11**  状态码

<a name="zh-cn_topic_0083864910_table6957182913514"></a>
<table><thead align="left"><tr id="zh-cn_topic_0083864910_row12961162965119"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0083864910_p189627299518"><a name="zh-cn_topic_0083864910_p189627299518"></a><a name="zh-cn_topic_0083864910_p189627299518"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0083864910_p1596342917515"><a name="zh-cn_topic_0083864910_p1596342917515"></a><a name="zh-cn_topic_0083864910_p1596342917515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0083864910_row15964122975119"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0083864910_p09651299518"><a name="zh-cn_topic_0083864910_p09651299518"></a><a name="zh-cn_topic_0083864910_p09651299518"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0083864910_p18966142915518"><a name="zh-cn_topic_0083864910_p18966142915518"></a><a name="zh-cn_topic_0083864910_p18966142915518"></a>This operation succeeds, and a Deployment resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

