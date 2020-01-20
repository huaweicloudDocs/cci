# 创建Namespace<a name="cci_02_3002"></a>

## 功能介绍<a name="s892e02bfa26441fc9c5f37e55ee37eef"></a>

创建一个Namespace。

当前云容器实例提供“通用计算型“和“GPU加速型“两种类型的资源，创建命名空间时需要选择资源类型，后续创建的负载中容器就运行在此类型的集群上。调用接口时必须指定metadata.annotations中namespace.kubernetes.io/flavor字段为如下值。

-   general-computing：通用计算型，基本水平的计算、存储和网络资源，适用于通用工作负载场景。
-   gpu-accelerated：GPU加速型，突出的图形计算能力，适用于AI等高性能场景。

Namespace下**必须**要创建一个Network，用于定义kubernetes中一个namespace内的网络与华为云虚拟私有云服务的子网和vpc的映射关系，具体请参见[创建Network](创建Network.md)。

## URI<a name="scf08ff5a2d1b418baa3ed1716ca70ed1"></a>

POST /api/v1/namespaces

**表 1**  Query描述

<a name="zh-cn_topic_0079615062_table60720217"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615062_row32267243"><th class="cellrowborder" valign="top" width="28.69286928692869%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615062_p63509856"><a name="zh-cn_topic_0079615062_p63509856"></a><a name="zh-cn_topic_0079615062_p63509856"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.3023302330233%" id="mcps1.2.4.1.2"><p id="p3589811321059"><a name="p3589811321059"></a><a name="p3589811321059"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="48.004800480048004%" id="mcps1.2.4.1.3"><p id="p2206602921059"><a name="p2206602921059"></a><a name="p2206602921059"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615062_row9439626"><td class="cellrowborder" valign="top" width="28.69286928692869%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615062_p26412257"><a name="zh-cn_topic_0079615062_p26412257"></a><a name="zh-cn_topic_0079615062_p26412257"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="23.3023302330233%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615062_p59018101"><a name="zh-cn_topic_0079615062_p59018101"></a><a name="zh-cn_topic_0079615062_p59018101"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="48.004800480048004%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615062_p15736877"><a name="zh-cn_topic_0079615062_p15736877"></a><a name="zh-cn_topic_0079615062_p15736877"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0079615062_ref458675483"></a>

**请求参数：**

**表 2**  Namespace v1数据结构说明

<a name="zh-cn_topic_0079615062_ref458759029"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615062_row61660876"><th class="cellrowborder" valign="top" width="21.8%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0079615062_p28475059"><a name="zh-cn_topic_0079615062_p28475059"></a><a name="zh-cn_topic_0079615062_p28475059"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.17%" id="mcps1.2.5.1.2"><p id="p4475307021059"><a name="p4475307021059"></a><a name="p4475307021059"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.74%" id="mcps1.2.5.1.3"><p id="p112003821059"><a name="p112003821059"></a><a name="p112003821059"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.290000000000006%" id="mcps1.2.5.1.4"><p id="p2361423021059"><a name="p2361423021059"></a><a name="p2361423021059"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615062_row40656116"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615062_p4811061"><a name="zh-cn_topic_0079615062_p4811061"></a><a name="zh-cn_topic_0079615062_p4811061"></a>kind</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615062_p54151655"><a name="zh-cn_topic_0079615062_p54151655"></a><a name="zh-cn_topic_0079615062_p54151655"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0079615062_p24207921"><a name="zh-cn_topic_0079615062_p24207921"></a><a name="zh-cn_topic_0079615062_p24207921"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0079615062_p14684604"><a name="zh-cn_topic_0079615062_p14684604"></a><a name="zh-cn_topic_0079615062_p14684604"></a>Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase.</p>
<p id="zh-cn_topic_0079615062_p65052577"><a name="zh-cn_topic_0079615062_p65052577"></a><a name="zh-cn_topic_0079615062_p65052577"></a>The value of this parameter is <strong id="zh-cn_topic_0079615062_b48602288"><a name="zh-cn_topic_0079615062_b48602288"></a><a name="zh-cn_topic_0079615062_b48602288"></a>Namespace</strong>.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079615062_row34767408"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615062_p64696659"><a name="zh-cn_topic_0079615062_p64696659"></a><a name="zh-cn_topic_0079615062_p64696659"></a>apiVersion</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615062_p5938035"><a name="zh-cn_topic_0079615062_p5938035"></a><a name="zh-cn_topic_0079615062_p5938035"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0079615062_p11218807"><a name="zh-cn_topic_0079615062_p11218807"></a><a name="zh-cn_topic_0079615062_p11218807"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0079615062_p36308168"><a name="zh-cn_topic_0079615062_p36308168"></a><a name="zh-cn_topic_0079615062_p36308168"></a>APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values.</p>
<p id="zh-cn_topic_0079615062_p58338056"><a name="zh-cn_topic_0079615062_p58338056"></a><a name="zh-cn_topic_0079615062_p58338056"></a>The value of this parameter is <strong id="zh-cn_topic_0079615062_b55280461"><a name="zh-cn_topic_0079615062_b55280461"></a><a name="zh-cn_topic_0079615062_b55280461"></a>v1</strong>.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079615062_row27762102"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615062_p34137829"><a name="zh-cn_topic_0079615062_p34137829"></a><a name="zh-cn_topic_0079615062_p34137829"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615062_p13700797"><a name="zh-cn_topic_0079615062_p13700797"></a><a name="zh-cn_topic_0079615062_p13700797"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="a3467669217d84b4c81c113d5e2da8569"><a name="a3467669217d84b4c81c113d5e2da8569"></a><a name="a3467669217d84b4c81c113d5e2da8569"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="p6864112411261"><a name="p6864112411261"></a><a name="p6864112411261"></a>Standard object metadata. 详情请参见<a href="数据结构.md#zh-cn_topic_0079614925_table47756489">表10</a>。</p>
<p id="p177247555127"><a name="p177247555127"></a><a name="p177247555127"></a>其中，annotations、labels字段请参见<a href="#table759162211124">表3</a>、<a href="#table139801827153620">表4</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0079615062_row21024178"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615062_p25236858"><a name="zh-cn_topic_0079615062_p25236858"></a><a name="zh-cn_topic_0079615062_p25236858"></a>spec</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615062_p30919631"><a name="zh-cn_topic_0079615062_p30919631"></a><a name="zh-cn_topic_0079615062_p30919631"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="p88239917279"><a name="p88239917279"></a><a name="p88239917279"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="p27117293810"><a name="p27117293810"></a><a name="p27117293810"></a>Spec defines the behavior of the Namespace. 详情请参见<a href="#zh-cn_topic_0079615062_table19390540">表5</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0079615062_row9555503"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615062_p35798250"><a name="zh-cn_topic_0079615062_p35798250"></a><a name="zh-cn_topic_0079615062_p35798250"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615062_p13977142"><a name="zh-cn_topic_0079615062_p13977142"></a><a name="zh-cn_topic_0079615062_p13977142"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="p1583710916274"><a name="p1583710916274"></a><a name="p1583710916274"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0079615062_p33323423"><a name="zh-cn_topic_0079615062_p33323423"></a><a name="zh-cn_topic_0079615062_p33323423"></a>Status describes the current status of a Namespace. 详情请参见<a href="#zh-cn_topic_0079615062_table40297137">表7</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  metadata.annotations字段说明

<a name="table759162211124"></a>
<table><thead align="left"><tr id="row0591622101219"><th class="cellrowborder" valign="top" width="21.8%" id="mcps1.2.5.1.1"><p id="p1975132291213"><a name="p1975132291213"></a><a name="p1975132291213"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.17%" id="mcps1.2.5.1.2"><p id="p37532219121"><a name="p37532219121"></a><a name="p37532219121"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.74%" id="mcps1.2.5.1.3"><p id="p87522211129"><a name="p87522211129"></a><a name="p87522211129"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.290000000000006%" id="mcps1.2.5.1.4"><p id="p1075142218127"><a name="p1075142218127"></a><a name="p1075142218127"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row13751122161210"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="p1190415031319"><a name="p1190415031319"></a><a name="p1190415031319"></a>namespace.kubernetes.io/flavor</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="p177562211129"><a name="p177562211129"></a><a name="p177562211129"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="p19751022111211"><a name="p19751022111211"></a><a name="p19751022111211"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="p171624431319"><a name="p171624431319"></a><a name="p171624431319"></a>用于指定namespace所属集群的flavor类型，目前支持GPU加速型(gpu-accelerated)、通用计算型(general-computing)两种类型。</p>
</td>
</tr>
<tr id="row489231161517"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="p28911444141910"><a name="p28911444141910"></a><a name="p28911444141910"></a>namespace.kubernetes.io/allowed-on-shared-node</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="p1089371113154"><a name="p1089371113154"></a><a name="p1089371113154"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="p6893171121510"><a name="p6893171121510"></a><a name="p6893171121510"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="p0893191113155"><a name="p0893191113155"></a><a name="p0893191113155"></a>用于指定是否开启弹性调度，可设置为true或false。默认取值为false，不开启时不需要指定该参数值。</p>
<p id="p2034614315202"><a name="p2034614315202"></a><a name="p2034614315202"></a>弹性调度：指当专属资源用尽时，可自动弹性创建CCI按需实例。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  metadata.labels字段说明

<a name="table139801827153620"></a>
<table><thead align="left"><tr id="row1980102715362"><th class="cellrowborder" valign="top" width="21.8%" id="mcps1.2.5.1.1"><p id="p398022793612"><a name="p398022793612"></a><a name="p398022793612"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.17%" id="mcps1.2.5.1.2"><p id="p698012278369"><a name="p698012278369"></a><a name="p698012278369"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.74%" id="mcps1.2.5.1.3"><p id="p1598022718367"><a name="p1598022718367"></a><a name="p1598022718367"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.290000000000006%" id="mcps1.2.5.1.4"><p id="p11980127143615"><a name="p11980127143615"></a><a name="p11980127143615"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6980112793611"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="p8426187183719"><a name="p8426187183719"></a><a name="p8426187183719"></a>sys_enterprise_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="p179801827133619"><a name="p179801827133619"></a><a name="p179801827133619"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="p798002715364"><a name="p798002715364"></a><a name="p798002715364"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="p2981427173614"><a name="p2981427173614"></a><a name="p2981427173614"></a>用于指定企业项目的ID。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  namespace spec字段数据结构说明

<a name="zh-cn_topic_0079615062_table19390540"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615062_row42478134"><th class="cellrowborder" valign="top" width="21.8%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0079615062_p18176840"><a name="zh-cn_topic_0079615062_p18176840"></a><a name="zh-cn_topic_0079615062_p18176840"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.17%" id="mcps1.2.5.1.2"><p id="p6641927621059"><a name="p6641927621059"></a><a name="p6641927621059"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.74%" id="mcps1.2.5.1.3"><p id="p1125227721059"><a name="p1125227721059"></a><a name="p1125227721059"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.290000000000006%" id="mcps1.2.5.1.4"><p id="p3901927921059"><a name="p3901927921059"></a><a name="p3901927921059"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615062_row9967070"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615062_p2026335"><a name="zh-cn_topic_0079615062_p2026335"></a><a name="zh-cn_topic_0079615062_p2026335"></a>finalizers</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615062_p29915412"><a name="zh-cn_topic_0079615062_p29915412"></a><a name="zh-cn_topic_0079615062_p29915412"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="p12908324164417"><a name="p12908324164417"></a><a name="p12908324164417"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0079615062_p48701244"><a name="zh-cn_topic_0079615062_p48701244"></a><a name="zh-cn_topic_0079615062_p48701244"></a>Finalizers is an opaque list of values that must be empty to permanently remove object from storage. 详情请参见<a href="#table1330102063316">表6</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  FinalizerName取值说明

<a name="table1330102063316"></a>
<table><thead align="left"><tr id="row193306209338"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p16330192010337"><a name="p16330192010337"></a><a name="p16330192010337"></a>名称</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p3330172053316"><a name="p3330172053316"></a><a name="p3330172053316"></a>值</p>
</th>
</tr>
</thead>
<tbody><tr id="row3330152013316"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p3678181483620"><a name="p3678181483620"></a><a name="p3678181483620"></a>FinalizerKubernetes</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p972582810361"><a name="p972582810361"></a><a name="p972582810361"></a>kubernetes</p>
</td>
</tr>
</tbody>
</table>

**表 7**  namespace status字段数据结构说明

<a name="zh-cn_topic_0079615062_table40297137"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615062_row62991470"><th class="cellrowborder" valign="top" width="21.8%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0079615062_p2035480"><a name="zh-cn_topic_0079615062_p2035480"></a><a name="zh-cn_topic_0079615062_p2035480"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.17%" id="mcps1.2.5.1.2"><p id="p935719621059"><a name="p935719621059"></a><a name="p935719621059"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.74%" id="mcps1.2.5.1.3"><p id="p1973538721059"><a name="p1973538721059"></a><a name="p1973538721059"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="39.290000000000006%" id="mcps1.2.5.1.4"><p id="p5506250321059"><a name="p5506250321059"></a><a name="p5506250321059"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615062_row20002757"><td class="cellrowborder" valign="top" width="21.8%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0079615062_p9610617"><a name="zh-cn_topic_0079615062_p9610617"></a><a name="zh-cn_topic_0079615062_p9610617"></a>phase</p>
</td>
<td class="cellrowborder" valign="top" width="19.17%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0079615062_p40262542"><a name="zh-cn_topic_0079615062_p40262542"></a><a name="zh-cn_topic_0079615062_p40262542"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="19.74%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0079615062_p40040492"><a name="zh-cn_topic_0079615062_p40040492"></a><a name="zh-cn_topic_0079615062_p40040492"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="39.290000000000006%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0079615062_p22054394"><a name="zh-cn_topic_0079615062_p22054394"></a><a name="zh-cn_topic_0079615062_p22054394"></a>Phase is the current lifecycle phase of the namespace.</p>
<p id="p1849654023918"><a name="p1849654023918"></a><a name="p1849654023918"></a>Namespace的状态有2个：</p>
<p id="p826234973911"><a name="p826234973911"></a><a name="p826234973911"></a>- Active: means the namespace is available for use in the system</p>
<p id="p0716155918399"><a name="p0716155918399"></a><a name="p0716155918399"></a>- Terminating: means the namespace is undergoing graceful termination</p>
</td>
</tr>
</tbody>
</table>

**请求示例：**

```
{
    "apiVersion": "v1",
    "kind": "Namespace",
    "metadata": {
        "name": "namespace-test",
        "annotations": {
            "namespace.kubernetes.io/flavor": "gpu-accelerated"
        },
        "labels": {
            "sys_enterprise_project_id": "0503dda897000fed2f78c00909158a4d"
    },
    "spec": {
        "finalizers": [
            "kubernetes"
        ]
    }
}
```

## 响应消息<a name="sc0e449fc74ae4c4a8a41deb65e63f4f9"></a>

**响应参数：**

响应参数的详细描述请参见[表2](#zh-cn_topic_0079615062_ref458759029)。

**表 8**  metadata.annotations字段说明

<a name="table0172161890"></a>
<table><thead align="left"><tr id="row12321416199"><th class="cellrowborder" valign="top" width="33.87%" id="mcps1.2.4.1.1"><p id="p54711617918"><a name="p54711617918"></a><a name="p54711617918"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.52%" id="mcps1.2.4.1.2"><p id="p154710161699"><a name="p154710161699"></a><a name="p154710161699"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.61%" id="mcps1.2.4.1.3"><p id="p747181616918"><a name="p747181616918"></a><a name="p747181616918"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row247116099"><td class="cellrowborder" valign="top" width="33.87%" headers="mcps1.2.4.1.1 "><p id="p689191014121"><a name="p689191014121"></a><a name="p689191014121"></a>pv.kubernetes.io/enable-dynamic-provisioning</p>
</td>
<td class="cellrowborder" valign="top" width="17.52%" headers="mcps1.2.4.1.2 "><p id="p18643166911"><a name="p18643166911"></a><a name="p18643166911"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.61%" headers="mcps1.2.4.1.3 "><p id="p115541816129"><a name="p115541816129"></a><a name="p115541816129"></a>是否支持动态创建存储。</p>
</td>
</tr>
<tr id="row1499785020124"><td class="cellrowborder" valign="top" width="33.87%" headers="mcps1.2.4.1.1 "><p id="p11997175031212"><a name="p11997175031212"></a><a name="p11997175031212"></a>tenant.kubernetes.io/domain-id</p>
</td>
<td class="cellrowborder" valign="top" width="17.52%" headers="mcps1.2.4.1.2 "><p id="p114411249141413"><a name="p114411249141413"></a><a name="p114411249141413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.61%" headers="mcps1.2.4.1.3 "><p id="p6997195015128"><a name="p6997195015128"></a><a name="p6997195015128"></a>用户的账号ID。</p>
</td>
</tr>
<tr id="row191704511126"><td class="cellrowborder" valign="top" width="33.87%" headers="mcps1.2.4.1.1 "><p id="p181706518124"><a name="p181706518124"></a><a name="p181706518124"></a>tenant.kubernetes.io/domain-name</p>
</td>
<td class="cellrowborder" valign="top" width="17.52%" headers="mcps1.2.4.1.2 "><p id="p645744931416"><a name="p645744931416"></a><a name="p645744931416"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.61%" headers="mcps1.2.4.1.3 "><p id="p15170165112125"><a name="p15170165112125"></a><a name="p15170165112125"></a>用户的账号名。</p>
</td>
</tr>
<tr id="row93581510128"><td class="cellrowborder" valign="top" width="33.87%" headers="mcps1.2.4.1.1 "><p id="p14358165171218"><a name="p14358165171218"></a><a name="p14358165171218"></a>tenant.kubernetes.io/project-id</p>
</td>
<td class="cellrowborder" valign="top" width="17.52%" headers="mcps1.2.4.1.2 "><p id="p3457349201411"><a name="p3457349201411"></a><a name="p3457349201411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.61%" headers="mcps1.2.4.1.3 "><p id="p5358115114122"><a name="p5358115114122"></a><a name="p5358115114122"></a>用户的项目ID。</p>
</td>
</tr>
<tr id="row3285164119146"><td class="cellrowborder" valign="top" width="33.87%" headers="mcps1.2.4.1.1 "><p id="p5285124118146"><a name="p5285124118146"></a><a name="p5285124118146"></a>tenant.kubernetes.io/project-name</p>
</td>
<td class="cellrowborder" valign="top" width="17.52%" headers="mcps1.2.4.1.2 "><p id="p3472649171413"><a name="p3472649171413"></a><a name="p3472649171413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.61%" headers="mcps1.2.4.1.3 "><p id="p1028517416144"><a name="p1028517416144"></a><a name="p1028517416144"></a>用户的项目名称。</p>
</td>
</tr>
</tbody>
</table>

**响应示例：**

```
{
    "metadata": {
        "name": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test",
        "uid": "68a68c5a-af6b-11e8-8f17-c81fbe371a17",
        "resourceVersion": "5016746",
        "creationTimestamp": "2018-09-03T11:20:48Z",
        "annotations": {
            "namespace.kubernetes.io/flavor": "gpu-accelerated",
            "pv.kubernetes.io/enable-dynamic-provisioning": "true",
            "tenant.kubernetes.io/domain-id": "aadb43c0b14c4cafbccfff483d075987",
            "tenant.kubernetes.io/domain-name": "cci",
            "tenant.kubernetes.io/project-id": "51bf52609f2a49c68bfda3398817b376",
            "tenant.kubernetes.io/project-name": "southchina"
        },
        "enable": true,
        "labels": {
            "sys_enterprise_project_id": "0503dda897000fed2f78c00909158a4d"
        }
    },
    "spec": {
        "finalizers": [
            "kubernetes"
        ]
    },
    "status": {
        "phase": "Active"
    }
}
```

## 状态码<a name="sbb5000c5c0ba41d9aee6b95e8e02c0ce"></a>

[表9](#zh-cn_topic_0079615062_table27129916)描述API的状态码。

**表 9**  状态码

<a name="zh-cn_topic_0079615062_table27129916"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615062_row7162954"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p3042097021059"><a name="p3042097021059"></a><a name="p3042097021059"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p4817954021059"><a name="p4817954021059"></a><a name="p4817954021059"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615062_row4477025"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615062_p27094719"><a name="zh-cn_topic_0079615062_p27094719"></a><a name="zh-cn_topic_0079615062_p27094719"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615062_p47188597"><a name="zh-cn_topic_0079615062_p47188597"></a><a name="zh-cn_topic_0079615062_p47188597"></a>This operation succeeds, and a Namespace resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

