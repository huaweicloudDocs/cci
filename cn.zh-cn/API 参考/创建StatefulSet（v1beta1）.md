# 创建StatefulSet<a name="cci_02_0035"></a>

## 功能介绍<a name="zh-cn_topic_0091433687_section40975543"></a>

This API is used to create a StatefulSet resource object.

## URI<a name="zh-cn_topic_0091433687_section33235568"></a>

POST /apis/apps/v1beta1/namespaces/\{namespace\}/statefulsets

[表1](#zh-cn_topic_0091433687_d0e37523)描述该API的参数。

**表 1**  参数解释

<a name="zh-cn_topic_0091433687_d0e37523"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433687_row5993206"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0091433687_p65652297517"><a name="zh-cn_topic_0091433687_p65652297517"></a><a name="zh-cn_topic_0091433687_p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.169999999999998%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0091433687_p165661629135114"><a name="zh-cn_topic_0091433687_p165661629135114"></a><a name="zh-cn_topic_0091433687_p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.61%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0091433687_p14567629115114"><a name="zh-cn_topic_0091433687_p14567629115114"></a><a name="zh-cn_topic_0091433687_p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433687_row12622186"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433687_p15764126"><a name="zh-cn_topic_0091433687_p15764126"></a><a name="zh-cn_topic_0091433687_p15764126"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433687_p1825823"><a name="zh-cn_topic_0091433687_p1825823"></a><a name="zh-cn_topic_0091433687_p1825823"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615000_p8332925"><a name="zh-cn_topic_0079615000_p8332925"></a><a name="zh-cn_topic_0079615000_p8332925"></a>命名空间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row55956597"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0091433687_p36190548"><a name="zh-cn_topic_0091433687_p36190548"></a><a name="zh-cn_topic_0091433687_p36190548"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0091433687_p45753308"><a name="zh-cn_topic_0091433687_p45753308"></a><a name="zh-cn_topic_0091433687_p45753308"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0091433687_p15030452"><a name="zh-cn_topic_0091433687_p15030452"></a><a name="zh-cn_topic_0091433687_p15030452"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0091433687_section30684661"></a>

**请求参数：**

**表 2**  请求参数

<a name="zh-cn_topic_0091433687_d0e37568"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433687_row22231582"><th class="cellrowborder" valign="top" width="22.447755224477554%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0091433687_p55927689"><a name="zh-cn_topic_0091433687_p55927689"></a><a name="zh-cn_topic_0091433687_p55927689"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.288571142885711%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0091433687_p33848965"><a name="zh-cn_topic_0091433687_p33848965"></a><a name="zh-cn_topic_0091433687_p33848965"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0091433687_p57411641"><a name="zh-cn_topic_0091433687_p57411641"></a><a name="zh-cn_topic_0091433687_p57411641"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42.85571442855714%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0091433687_p19831374"><a name="zh-cn_topic_0091433687_p19831374"></a><a name="zh-cn_topic_0091433687_p19831374"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433687_row62837484"><td class="cellrowborder" valign="top" width="22.447755224477554%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p56671418"><a name="zh-cn_topic_0091433687_p56671418"></a><a name="zh-cn_topic_0091433687_p56671418"></a>apiVersion</p>
</td>
<td class="cellrowborder" valign="top" width="14.288571142885711%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p26982112"><a name="zh-cn_topic_0091433687_p26982112"></a><a name="zh-cn_topic_0091433687_p26982112"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p38067463"><a name="zh-cn_topic_0091433687_p38067463"></a><a name="zh-cn_topic_0091433687_p38067463"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="42.85571442855714%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p63565654"><a name="zh-cn_topic_0091433687_p63565654"></a><a name="zh-cn_topic_0091433687_p63565654"></a>APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row35219981"><td class="cellrowborder" valign="top" width="22.447755224477554%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p34246188"><a name="zh-cn_topic_0091433687_p34246188"></a><a name="zh-cn_topic_0091433687_p34246188"></a>kind</p>
</td>
<td class="cellrowborder" valign="top" width="14.288571142885711%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p22477832"><a name="zh-cn_topic_0091433687_p22477832"></a><a name="zh-cn_topic_0091433687_p22477832"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p8765064"><a name="zh-cn_topic_0091433687_p8765064"></a><a name="zh-cn_topic_0091433687_p8765064"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="42.85571442855714%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p38881556"><a name="zh-cn_topic_0091433687_p38881556"></a><a name="zh-cn_topic_0091433687_p38881556"></a>Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row14389691"><td class="cellrowborder" valign="top" width="22.447755224477554%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p24714309"><a name="zh-cn_topic_0091433687_p24714309"></a><a name="zh-cn_topic_0091433687_p24714309"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="14.288571142885711%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p55702032"><a name="zh-cn_topic_0091433687_p55702032"></a><a name="zh-cn_topic_0091433687_p55702032"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p15570756"><a name="zh-cn_topic_0091433687_p15570756"></a><a name="zh-cn_topic_0091433687_p15570756"></a><a href="请求数据结构（OLD-VERSIONS）.md#zh-cn_topic_0083857342_zh-cn_topic_0079614925_table47756489">表10</a></p>
</td>
<td class="cellrowborder" valign="top" width="42.85571442855714%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p9683143"><a name="zh-cn_topic_0091433687_p9683143"></a><a name="zh-cn_topic_0091433687_p9683143"></a>Standard list metadata.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row20039428"><td class="cellrowborder" valign="top" width="22.447755224477554%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p12580961"><a name="zh-cn_topic_0091433687_p12580961"></a><a name="zh-cn_topic_0091433687_p12580961"></a>spec</p>
</td>
<td class="cellrowborder" valign="top" width="14.288571142885711%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p12424902"><a name="zh-cn_topic_0091433687_p12424902"></a><a name="zh-cn_topic_0091433687_p12424902"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p66893020"><a name="zh-cn_topic_0091433687_p66893020"></a><a name="zh-cn_topic_0091433687_p66893020"></a><a href="#table3236827151115">表3</a></p>
</td>
<td class="cellrowborder" valign="top" width="42.85571442855714%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p43976738"><a name="zh-cn_topic_0091433687_p43976738"></a><a name="zh-cn_topic_0091433687_p43976738"></a>Spec defines the desired identities of pods in this set.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row60246329"><td class="cellrowborder" valign="top" width="22.447755224477554%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p48114513"><a name="zh-cn_topic_0091433687_p48114513"></a><a name="zh-cn_topic_0091433687_p48114513"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="14.288571142885711%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p4961465"><a name="zh-cn_topic_0091433687_p4961465"></a><a name="zh-cn_topic_0091433687_p4961465"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p66334361"><a name="zh-cn_topic_0091433687_p66334361"></a><a name="zh-cn_topic_0091433687_p66334361"></a><a href="#zh-cn_topic_0091433687_d0e37659">表4</a></p>
</td>
<td class="cellrowborder" valign="top" width="42.85571442855714%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p39367534"><a name="zh-cn_topic_0091433687_p39367534"></a><a name="zh-cn_topic_0091433687_p39367534"></a>Status is the current status of Pods in this StatefulSet. This data may be out of date by some window of time.</p>
</td>
</tr>
</tbody>
</table>

**表 3**  spec字段数据结构说明

<a name="table3236827151115"></a>
<table><thead align="left"><tr id="row82561727171110"><th class="cellrowborder" valign="top" width="22%" id="mcps1.2.5.1.1"><p id="p15262112712113"><a name="p15262112712113"></a><a name="p15262112712113"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15%" id="mcps1.2.5.1.2"><p id="p526516275115"><a name="p526516275115"></a><a name="p526516275115"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="21%" id="mcps1.2.5.1.3"><p id="p12270182717118"><a name="p12270182717118"></a><a name="p12270182717118"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42%" id="mcps1.2.5.1.4"><p id="p527582761114"><a name="p527582761114"></a><a name="p527582761114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1928132718115"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p8286127181120"><a name="p8286127181120"></a><a name="p8286127181120"></a>replicas</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.2 "><p id="p1292192791116"><a name="p1292192791116"></a><a name="p1292192791116"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.3 "><p id="p5298162715111"><a name="p5298162715111"></a><a name="p5298162715111"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.5.1.4 "><p id="p6304427121111"><a name="p6304427121111"></a><a name="p6304427121111"></a>Replicas is the desired number of replicas of the given Template. These are replicas in the sense that they are instantiations of the same Template, but individual replicas also have a consistent identity. If unspecified, defaults to 1.</p>
</td>
</tr>
<tr id="row1230662716118"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p4312127121112"><a name="p4312127121112"></a><a name="p4312127121112"></a>podManagementPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.2 "><p id="p1131712781119"><a name="p1131712781119"></a><a name="p1131712781119"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.3 "><p id="p03221827151115"><a name="p03221827151115"></a><a name="p03221827151115"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.5.1.4 "><p id="p83283273114"><a name="p83283273114"></a><a name="p83283273114"></a></p>
<p id="p19331102719119"><a name="p19331102719119"></a><a name="p19331102719119"></a>podManagementPolicy controls how pods are created during initial scale up, when replacing pods on nodes, or when scaling down. The default policy is OrderedReady, where pods are created in increasing order (pod-0, then pod-1, etc) and the controller will wait until each pod is ready before continuing. When scaling down, the pods are removed in the opposite order. The alternative policy is Parallel which will create pods in parallel to match the desired scale without waiting, and on scale down will delete all pods at once.</p>
</td>
</tr>
<tr id="row5333182713117"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p633792741111"><a name="p633792741111"></a><a name="p633792741111"></a>revisionHistoryLimit</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.2 "><p id="p163445275118"><a name="p163445275118"></a><a name="p163445275118"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.3 "><p id="p143481427111116"><a name="p143481427111116"></a><a name="p143481427111116"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.5.1.4 "><p id="p16353162710114"><a name="p16353162710114"></a><a name="p16353162710114"></a></p>
<p id="p135662711114"><a name="p135662711114"></a><a name="p135662711114"></a>revisionHistoryLimit is the maximum number of revisions that will be maintained in the StatefulSet's revision history. The revision history consists of all revisions not represented by a currently applied StatefulSetSpec version. The default value is 10.</p>
</td>
</tr>
<tr id="row835912751115"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p20363122711112"><a name="p20363122711112"></a><a name="p20363122711112"></a>updateStrategy</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.2 "><p id="p2369527101114"><a name="p2369527101114"></a><a name="p2369527101114"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.3 "><p id="p13374112717112"><a name="p13374112717112"></a><a name="p13374112717112"></a><a href="#zh-cn_topic_0091433687_d0e38083">表7</a></p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.5.1.4 "><p id="p15381927161112"><a name="p15381927161112"></a><a name="p15381927161112"></a></p>
<p id="p1938532751120"><a name="p1938532751120"></a><a name="p1938532751120"></a>updateStrategy indicates the StatefulSetUpdateStrategy that will be employed to update Pods in the StatefulSet when a revision is made to Template.</p>
</td>
</tr>
<tr id="row1138792721112"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p15392102711116"><a name="p15392102711116"></a><a name="p15392102711116"></a>serviceName</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.2 "><p id="p33976276117"><a name="p33976276117"></a><a name="p33976276117"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.3 "><p id="p1840252714113"><a name="p1840252714113"></a><a name="p1840252714113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.5.1.4 "><p id="p540662713113"><a name="p540662713113"></a><a name="p540662713113"></a>ServiceName is the name of the service that governs this StatefulSet. This service must exist before the StatefulSet, and is responsible for the network identity of the set. Pods get DNS/hostnames that follow the pattern: pod-specific-string.serviceName.default.svc.cluster.local where "pod-specific-string" is managed by the StatefulSet controller.</p>
</td>
</tr>
<tr id="row3433122716113"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p74388279113"><a name="p74388279113"></a><a name="p74388279113"></a>selector</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.2 "><p id="p544362713115"><a name="p544362713115"></a><a name="p544362713115"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.3 "><p id="p144919276113"><a name="p144919276113"></a><a name="p144919276113"></a><a href="#zh-cn_topic_0091433687_d0e37920">表5</a></p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.5.1.4 "><p id="p10456182715116"><a name="p10456182715116"></a><a name="p10456182715116"></a>Selector is a label query over pods that should match the replica count. If empty, defaulted to labels on the pod template.</p>
</td>
</tr>
<tr id="row1458132721118"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.5.1.1 "><p id="p346632771113"><a name="p346632771113"></a><a name="p346632771113"></a>template</p>
</td>
<td class="cellrowborder" valign="top" width="15%" headers="mcps1.2.5.1.2 "><p id="p144714273119"><a name="p144714273119"></a><a name="p144714273119"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="21%" headers="mcps1.2.5.1.3 "><p id="p144759277110"><a name="p144759277110"></a><a name="p144759277110"></a><a href="数据结构.md#zh-cn_topic_0079614925_table58905579">表1</a></p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.5.1.4 "><p id="p18483122715119"><a name="p18483122715119"></a><a name="p18483122715119"></a>Template is the object that describes the pod that will be created if insufficient replicas are detected. Each pod stamped out by the StatefulSet will fulfill this Template, but have a unique identity from the rest of the StatefulSet.</p>
</td>
</tr>
</tbody>
</table>

**表 4**  status字段数据结构说明

<a name="zh-cn_topic_0091433687_d0e37659"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433687_row16874366"><th class="cellrowborder" valign="top" width="22.68%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0091433687_p24646410"><a name="zh-cn_topic_0091433687_p24646410"></a><a name="zh-cn_topic_0091433687_p24646410"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.430000000000001%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0091433687_p50202190"><a name="zh-cn_topic_0091433687_p50202190"></a><a name="zh-cn_topic_0091433687_p50202190"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.59%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0091433687_p39845619"><a name="zh-cn_topic_0091433687_p39845619"></a><a name="zh-cn_topic_0091433687_p39845619"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.3%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0091433687_p6269729"><a name="zh-cn_topic_0091433687_p6269729"></a><a name="zh-cn_topic_0091433687_p6269729"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433687_row38086015"><td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p65068341"><a name="zh-cn_topic_0091433687_p65068341"></a><a name="zh-cn_topic_0091433687_p65068341"></a>observedGeneration</p>
</td>
<td class="cellrowborder" valign="top" width="14.430000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p36044268"><a name="zh-cn_topic_0091433687_p36044268"></a><a name="zh-cn_topic_0091433687_p36044268"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.59%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p33904587"><a name="zh-cn_topic_0091433687_p33904587"></a><a name="zh-cn_topic_0091433687_p33904587"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="43.3%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p61917051"><a name="zh-cn_topic_0091433687_p61917051"></a><a name="zh-cn_topic_0091433687_p61917051"></a>Most recent generation observed by this autoscaler.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row20382553"><td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p40374085"><a name="zh-cn_topic_0091433687_p40374085"></a><a name="zh-cn_topic_0091433687_p40374085"></a>replicas</p>
</td>
<td class="cellrowborder" valign="top" width="14.430000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p49075413"><a name="zh-cn_topic_0091433687_p49075413"></a><a name="zh-cn_topic_0091433687_p49075413"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.59%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p15685489"><a name="zh-cn_topic_0091433687_p15685489"></a><a name="zh-cn_topic_0091433687_p15685489"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="43.3%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p62565122"><a name="zh-cn_topic_0091433687_p62565122"></a><a name="zh-cn_topic_0091433687_p62565122"></a>Replicas is the number of actual replicas.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row26215194"><td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p43055989"><a name="zh-cn_topic_0091433687_p43055989"></a><a name="zh-cn_topic_0091433687_p43055989"></a>currentReplicas</p>
</td>
<td class="cellrowborder" valign="top" width="14.430000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p64983097"><a name="zh-cn_topic_0091433687_p64983097"></a><a name="zh-cn_topic_0091433687_p64983097"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.59%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p29139468"><a name="zh-cn_topic_0091433687_p29139468"></a><a name="zh-cn_topic_0091433687_p29139468"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="43.3%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p11486745"><a name="zh-cn_topic_0091433687_p11486745"></a><a name="zh-cn_topic_0091433687_p11486745"></a></p>
<p id="zh-cn_topic_0091433687_p36271844"><a name="zh-cn_topic_0091433687_p36271844"></a><a name="zh-cn_topic_0091433687_p36271844"></a>currentReplicas is the number of Pods created by the StatefulSet controller from the StatefulSet version indicated by currentRevision.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row58011142"><td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p1282043"><a name="zh-cn_topic_0091433687_p1282043"></a><a name="zh-cn_topic_0091433687_p1282043"></a>currentRevision</p>
</td>
<td class="cellrowborder" valign="top" width="14.430000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p36736673"><a name="zh-cn_topic_0091433687_p36736673"></a><a name="zh-cn_topic_0091433687_p36736673"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.59%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p22880543"><a name="zh-cn_topic_0091433687_p22880543"></a><a name="zh-cn_topic_0091433687_p22880543"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.3%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p41384734"><a name="zh-cn_topic_0091433687_p41384734"></a><a name="zh-cn_topic_0091433687_p41384734"></a></p>
<p id="zh-cn_topic_0091433687_p36918294"><a name="zh-cn_topic_0091433687_p36918294"></a><a name="zh-cn_topic_0091433687_p36918294"></a>currentRevision, if not empty, indicates the version of the StatefulSet used to generate Pods in the sequence [0,currentReplicas).</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row63829190"><td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p2781886"><a name="zh-cn_topic_0091433687_p2781886"></a><a name="zh-cn_topic_0091433687_p2781886"></a>readyReplicas</p>
</td>
<td class="cellrowborder" valign="top" width="14.430000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p24006190"><a name="zh-cn_topic_0091433687_p24006190"></a><a name="zh-cn_topic_0091433687_p24006190"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.59%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p65453247"><a name="zh-cn_topic_0091433687_p65453247"></a><a name="zh-cn_topic_0091433687_p65453247"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="43.3%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p112792"><a name="zh-cn_topic_0091433687_p112792"></a><a name="zh-cn_topic_0091433687_p112792"></a></p>
<p id="zh-cn_topic_0091433687_p1015136"><a name="zh-cn_topic_0091433687_p1015136"></a><a name="zh-cn_topic_0091433687_p1015136"></a>readyReplicas is the number of Pods created by the StatefulSet controller that have a Ready Condition.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row9136226"><td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p1836869"><a name="zh-cn_topic_0091433687_p1836869"></a><a name="zh-cn_topic_0091433687_p1836869"></a>updateRevision</p>
</td>
<td class="cellrowborder" valign="top" width="14.430000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p14568680"><a name="zh-cn_topic_0091433687_p14568680"></a><a name="zh-cn_topic_0091433687_p14568680"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.59%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p39212403"><a name="zh-cn_topic_0091433687_p39212403"></a><a name="zh-cn_topic_0091433687_p39212403"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.3%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p22088079"><a name="zh-cn_topic_0091433687_p22088079"></a><a name="zh-cn_topic_0091433687_p22088079"></a></p>
<p id="zh-cn_topic_0091433687_p64574987"><a name="zh-cn_topic_0091433687_p64574987"></a><a name="zh-cn_topic_0091433687_p64574987"></a>updateRevision, if not empty, indicates the version of the StatefulSet used to generate Pods in the sequence [replicas-updatedReplicas,replicas)</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row44303971"><td class="cellrowborder" valign="top" width="22.68%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p31851928"><a name="zh-cn_topic_0091433687_p31851928"></a><a name="zh-cn_topic_0091433687_p31851928"></a>updatedReplicas</p>
</td>
<td class="cellrowborder" valign="top" width="14.430000000000001%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p29869398"><a name="zh-cn_topic_0091433687_p29869398"></a><a name="zh-cn_topic_0091433687_p29869398"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.59%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p3502148"><a name="zh-cn_topic_0091433687_p3502148"></a><a name="zh-cn_topic_0091433687_p3502148"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="43.3%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p15238538"><a name="zh-cn_topic_0091433687_p15238538"></a><a name="zh-cn_topic_0091433687_p15238538"></a></p>
<p id="zh-cn_topic_0091433687_p2929118"><a name="zh-cn_topic_0091433687_p2929118"></a><a name="zh-cn_topic_0091433687_p2929118"></a>updatedReplicas is the number of Pods created by the StatefulSet controller from the StatefulSet version indicated by updateRevision.</p>
</td>
</tr>
</tbody>
</table>

**表 5**  selector字段数据结构说明

<a name="zh-cn_topic_0091433687_d0e37920"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433687_row42112853"><th class="cellrowborder" valign="top" width="22.447755224477554%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0091433687_p55697946"><a name="zh-cn_topic_0091433687_p55697946"></a><a name="zh-cn_topic_0091433687_p55697946"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.308469153084694%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0091433687_p15239763"><a name="zh-cn_topic_0091433687_p15239763"></a><a name="zh-cn_topic_0091433687_p15239763"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.388061193880613%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0091433687_p26461289"><a name="zh-cn_topic_0091433687_p26461289"></a><a name="zh-cn_topic_0091433687_p26461289"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="42.85571442855714%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0091433687_p62989635"><a name="zh-cn_topic_0091433687_p62989635"></a><a name="zh-cn_topic_0091433687_p62989635"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433687_row1886793"><td class="cellrowborder" valign="top" width="22.447755224477554%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p18612581"><a name="zh-cn_topic_0091433687_p18612581"></a><a name="zh-cn_topic_0091433687_p18612581"></a>matchExpressions</p>
</td>
<td class="cellrowborder" valign="top" width="15.308469153084694%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p31224060"><a name="zh-cn_topic_0091433687_p31224060"></a><a name="zh-cn_topic_0091433687_p31224060"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.388061193880613%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p46120952"><a name="zh-cn_topic_0091433687_p46120952"></a><a name="zh-cn_topic_0091433687_p46120952"></a><a href="#zh-cn_topic_0091433687_d0e37970">表6</a> array</p>
</td>
<td class="cellrowborder" valign="top" width="42.85571442855714%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p633806"><a name="zh-cn_topic_0091433687_p633806"></a><a name="zh-cn_topic_0091433687_p633806"></a>matchExpressions is a list of label selector requirements. The requirements are ANDed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row5704254"><td class="cellrowborder" valign="top" width="22.447755224477554%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p59391448"><a name="zh-cn_topic_0091433687_p59391448"></a><a name="zh-cn_topic_0091433687_p59391448"></a>matchLabels</p>
</td>
<td class="cellrowborder" valign="top" width="15.308469153084694%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p45977974"><a name="zh-cn_topic_0091433687_p45977974"></a><a name="zh-cn_topic_0091433687_p45977974"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.388061193880613%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p33228417"><a name="zh-cn_topic_0091433687_p33228417"></a><a name="zh-cn_topic_0091433687_p33228417"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="42.85571442855714%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p7147232"><a name="zh-cn_topic_0091433687_p7147232"></a><a name="zh-cn_topic_0091433687_p7147232"></a>MatchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.</p>
</td>
</tr>
</tbody>
</table>

**表 6**  matchExpressions字段数据结构说明

<a name="zh-cn_topic_0091433687_d0e37970"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433687_row44155801"><th class="cellrowborder" valign="top" width="22.447755224477547%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0091433687_p19850148"><a name="zh-cn_topic_0091433687_p19850148"></a><a name="zh-cn_topic_0091433687_p19850148"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="15.308469153084689%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0091433687_p64358168"><a name="zh-cn_topic_0091433687_p64358168"></a><a name="zh-cn_topic_0091433687_p64358168"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.40795920407959%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0091433687_p45629083"><a name="zh-cn_topic_0091433687_p45629083"></a><a name="zh-cn_topic_0091433687_p45629083"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="41.83581641835816%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0091433687_p4968280"><a name="zh-cn_topic_0091433687_p4968280"></a><a name="zh-cn_topic_0091433687_p4968280"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433687_row66886389"><td class="cellrowborder" valign="top" width="22.447755224477547%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p49088410"><a name="zh-cn_topic_0091433687_p49088410"></a><a name="zh-cn_topic_0091433687_p49088410"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="15.308469153084689%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p16738288"><a name="zh-cn_topic_0091433687_p16738288"></a><a name="zh-cn_topic_0091433687_p16738288"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="20.40795920407959%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p13624094"><a name="zh-cn_topic_0091433687_p13624094"></a><a name="zh-cn_topic_0091433687_p13624094"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="41.83581641835816%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p29809869"><a name="zh-cn_topic_0091433687_p29809869"></a><a name="zh-cn_topic_0091433687_p29809869"></a>key is the label key that the selector applies to.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row66962237"><td class="cellrowborder" valign="top" width="22.447755224477547%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p55232079"><a name="zh-cn_topic_0091433687_p55232079"></a><a name="zh-cn_topic_0091433687_p55232079"></a>operator</p>
</td>
<td class="cellrowborder" valign="top" width="15.308469153084689%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p44613430"><a name="zh-cn_topic_0091433687_p44613430"></a><a name="zh-cn_topic_0091433687_p44613430"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="20.40795920407959%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p56918106"><a name="zh-cn_topic_0091433687_p56918106"></a><a name="zh-cn_topic_0091433687_p56918106"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="41.83581641835816%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p46963874"><a name="zh-cn_topic_0091433687_p46963874"></a><a name="zh-cn_topic_0091433687_p46963874"></a>operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row20021687"><td class="cellrowborder" valign="top" width="22.447755224477547%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p11143985"><a name="zh-cn_topic_0091433687_p11143985"></a><a name="zh-cn_topic_0091433687_p11143985"></a>values</p>
</td>
<td class="cellrowborder" valign="top" width="15.308469153084689%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p30247620"><a name="zh-cn_topic_0091433687_p30247620"></a><a name="zh-cn_topic_0091433687_p30247620"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="20.40795920407959%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p34138135"><a name="zh-cn_topic_0091433687_p34138135"></a><a name="zh-cn_topic_0091433687_p34138135"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="41.83581641835816%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p13725522"><a name="zh-cn_topic_0091433687_p13725522"></a><a name="zh-cn_topic_0091433687_p13725522"></a>values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.</p>
</td>
</tr>
</tbody>
</table>

**表 7**  updateStrategy字段数据结构说明

<a name="zh-cn_topic_0091433687_d0e38083"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433687_row1068106"><th class="cellrowborder" valign="top" width="20.40795920407959%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0091433687_p19407724"><a name="zh-cn_topic_0091433687_p19407724"></a><a name="zh-cn_topic_0091433687_p19407724"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.34836516348365%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0091433687_p28521827"><a name="zh-cn_topic_0091433687_p28521827"></a><a name="zh-cn_topic_0091433687_p28521827"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="23.447655234476546%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0091433687_p28566679"><a name="zh-cn_topic_0091433687_p28566679"></a><a name="zh-cn_topic_0091433687_p28566679"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.7960203979602%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0091433687_p32199663"><a name="zh-cn_topic_0091433687_p32199663"></a><a name="zh-cn_topic_0091433687_p32199663"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433687_row58035924"><td class="cellrowborder" valign="top" width="20.40795920407959%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p3289389"><a name="zh-cn_topic_0091433687_p3289389"></a><a name="zh-cn_topic_0091433687_p3289389"></a>rollingUpdate</p>
</td>
<td class="cellrowborder" valign="top" width="16.34836516348365%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p65113955"><a name="zh-cn_topic_0091433687_p65113955"></a><a name="zh-cn_topic_0091433687_p65113955"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="23.447655234476546%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p39738973"><a name="zh-cn_topic_0091433687_p39738973"></a><a name="zh-cn_topic_0091433687_p39738973"></a><a href="#zh-cn_topic_0091433687_table102371729161619">表8</a></p>
</td>
<td class="cellrowborder" valign="top" width="39.7960203979602%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p45791139"><a name="zh-cn_topic_0091433687_p45791139"></a><a name="zh-cn_topic_0091433687_p45791139"></a></p>
<p id="zh-cn_topic_0091433687_p9467071"><a name="zh-cn_topic_0091433687_p9467071"></a><a name="zh-cn_topic_0091433687_p9467071"></a>RollingUpdate is used to communicate parameters when Type is RollingUpdateStatefulSetStrategyType.</p>
</td>
</tr>
<tr id="zh-cn_topic_0091433687_row18094775"><td class="cellrowborder" valign="top" width="20.40795920407959%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p56390700"><a name="zh-cn_topic_0091433687_p56390700"></a><a name="zh-cn_topic_0091433687_p56390700"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="16.34836516348365%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p4244010"><a name="zh-cn_topic_0091433687_p4244010"></a><a name="zh-cn_topic_0091433687_p4244010"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="23.447655234476546%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p8220504"><a name="zh-cn_topic_0091433687_p8220504"></a><a name="zh-cn_topic_0091433687_p8220504"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.7960203979602%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p61881054"><a name="zh-cn_topic_0091433687_p61881054"></a><a name="zh-cn_topic_0091433687_p61881054"></a></p>
<p id="zh-cn_topic_0091433687_p20058578"><a name="zh-cn_topic_0091433687_p20058578"></a><a name="zh-cn_topic_0091433687_p20058578"></a>Type indicates the type of the StatefulSetUpdateStrategy.</p>
</td>
</tr>
</tbody>
</table>

**表 8**  rollingUpdate字段数据结构说明

<a name="zh-cn_topic_0091433687_table102371729161619"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433687_row66152742"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0091433687_p56771847"><a name="zh-cn_topic_0091433687_p56771847"></a><a name="zh-cn_topic_0091433687_p56771847"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.328367163283673%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0091433687_p35116889"><a name="zh-cn_topic_0091433687_p35116889"></a><a name="zh-cn_topic_0091433687_p35116889"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="23.46765323467653%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0091433687_p25895747"><a name="zh-cn_topic_0091433687_p25895747"></a><a name="zh-cn_topic_0091433687_p25895747"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.796020397960206%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0091433687_p17180782"><a name="zh-cn_topic_0091433687_p17180782"></a><a name="zh-cn_topic_0091433687_p17180782"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433687_row49466114"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0091433687_p47332261"><a name="zh-cn_topic_0091433687_p47332261"></a><a name="zh-cn_topic_0091433687_p47332261"></a>partition</p>
</td>
<td class="cellrowborder" valign="top" width="16.328367163283673%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0091433687_p8707970"><a name="zh-cn_topic_0091433687_p8707970"></a><a name="zh-cn_topic_0091433687_p8707970"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="23.46765323467653%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0091433687_p34256959"><a name="zh-cn_topic_0091433687_p34256959"></a><a name="zh-cn_topic_0091433687_p34256959"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="39.796020397960206%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0091433687_p23350276"><a name="zh-cn_topic_0091433687_p23350276"></a><a name="zh-cn_topic_0091433687_p23350276"></a></p>
<p id="zh-cn_topic_0091433687_p8825898"><a name="zh-cn_topic_0091433687_p8825898"></a><a name="zh-cn_topic_0091433687_p8825898"></a>Partition indicates the ordinal at which the StatefulSet should be partitioned.</p>
</td>
</tr>
</tbody>
</table>

**请求示例：**

```
{
    "apiVersion": "apps/v1beta1", 
    "kind": "StatefulSet", 
    "metadata": {
        "annotations": {
            "description": ""
        }, 
        "labels": {
            "appgroup": ""
        }, 
        "name": "statefulset-test"
    }, 
    "spec": {
        "replicas": 2, 
        "selector": {
            "matchLabels": {
                "app": "statefulset-test"
            }
        }, 
        "template": {
            "metadata": {
                "annotations": {
                    "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]", 
                    "com.huawei.scheduler/container-type": "secure-container", 
                    "pod.alpha.kubernetes.io/initialized": "true"
                }, 
                "labels": {
                    "app": "statefulset-test"
                }
            }, 
            "spec": {
                "containers": [
                    {
                        "image": "undefined:undefined", 
                        "name": "container-0", 
                        "resources": {
                            "limits": {
                                "cpu": "1000m", 
                                "memory": "2048Mi"
                            }, 
                            "requests": {
                                "cpu": "1000m", 
                                "memory": "2048Mi"
                            }
                        }, 
                        "lifecycle": {}
                    }, 
                    {
                        "image": "nginx:latest", 
                        "name": "container-1", 
                        "resources": {
                            "limits": {
                                "cpu": "1000m", 
                                "memory": "2048Mi"
                            }, 
                            "requests": {
                                "cpu": "1000m", 
                                "memory": "2048Mi"
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
                "volumes": [], 
                "affinity": {}
            }
        }, 
        "serviceName": "test", 
        "updateStrategy": {
            "type": "RollingUpdate"
        }
    }
}
```

## 响应消息<a name="zh-cn_topic_0091433687_section7726493"></a>

**响应参数：**

响应参数的详细描述请参见[表2](#zh-cn_topic_0091433687_d0e37568)

**响应示例：**

```
{
    "kind": "StatefulSet", 
    "apiVersion": "apps/v1beta1", 
    "metadata": {
        "name": "statefulset-test", 
        "namespace": "8f6c39e7c269440c881bba2fc49586d6", 
        "selfLink": "/apis/apps/v1beta1/namespaces/8f6c39e7c269440c881bba2fc49586d6/statefulsets/statefulset-test", 
        "uid": "ee0ef0d0-2728-11e8-8930-84a9c46e8ca3", 
        "resourceVersion": "4510951", 
        "generation": 1, 
        "creationTimestamp": "2018-03-14T01:42:18Z", 
        "labels": {
            "appgroup": ""
        }, 
        "annotations": {
            "description": ""
        }, 
        "enable": true
    }, 
    "spec": {
        "replicas": 2, 
        "selector": {
            "matchLabels": {
                "app": "statefulset-test"
            }
        }, 
        "template": {
            "metadata": {
                "creationTimestamp": null, 
                "labels": {
                    "app": "statefulset-test"
                }, 
                "annotations": {
                    "com.huawei.scheduler/container-type": "secure-container", 
                    "metrics.alpha.kubernetes.io/custom-endpoints": "[{api:'',path:'',port:'',names:''}]", 
                    "pod.alpha.kubernetes.io/initialized": "true"
                }, 
                "enable": true
            }, 
            "spec": {
                "containers": [
                    {
                        "name": "container-0", 
                        "image": "undefined:undefined", 
                        "resources": {
                            "limits": {
                                "cpu": "1", 
                                "memory": "2Gi"
                            }, 
                            "requests": {
                                "cpu": "1", 
                                "memory": "2Gi"
                            }
                        }, 
                        "lifecycle": {}, 
                        "terminationMessagePath": "/dev/termination-log", 
                        "terminationMessagePolicy": "File", 
                        "imagePullPolicy": "IfNotPresent"
                    }, 
                    {
                        "name": "container-1", 
                        "image": "nginx:latest", 
                        "resources": {
                            "limits": {
                                "cpu": "1", 
                                "memory": "2Gi"
                            }, 
                            "requests": {
                                "cpu": "1", 
                                "memory": "2Gi"
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
        "serviceName": "test", 
        "podManagementPolicy": "OrderedReady", 
        "updateStrategy": {
            "type": "RollingUpdate"
        }, 
        "revisionHistoryLimit": 10
    }, 
    "status": {
        "replicas": 0
    }
}
```

## 状态码<a name="zh-cn_topic_0091433687_section2429579"></a>

[表9](#zh-cn_topic_0091433687_d0e38203)描述API的状态码。

**表 9**  状态码

<a name="zh-cn_topic_0091433687_d0e38203"></a>
<table><thead align="left"><tr id="zh-cn_topic_0091433687_row26900678"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="zh-cn_topic_0091433687_p31471277"><a name="zh-cn_topic_0091433687_p31471277"></a><a name="zh-cn_topic_0091433687_p31471277"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0091433687_p66145529"><a name="zh-cn_topic_0091433687_p66145529"></a><a name="zh-cn_topic_0091433687_p66145529"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0091433687_row56187666"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0091433687_p54907103"><a name="zh-cn_topic_0091433687_p54907103"></a><a name="zh-cn_topic_0091433687_p54907103"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0091433687_p18290377"><a name="zh-cn_topic_0091433687_p18290377"></a><a name="zh-cn_topic_0091433687_p18290377"></a>The request has been fulfilled, resulting in the creation of a new resource.</p>
</td>
</tr>
</tbody>
</table>

