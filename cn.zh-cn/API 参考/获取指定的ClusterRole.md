# 获取指定的ClusterRole<a name="cci_02_3185"></a>

## 功能介绍<a name="section510817225448"></a>

This API is used to read the specified ClusterRole

## URL<a name="section1141816212454"></a>

GET /apis/rbac.authorization.k8s.io/v1/clusterroles/\{name\}

[参数解释](#d0e42906)描述该API的参数。

**表 1**  参数解释

<a name="d0e42906"></a>
<table><thead align="left"><tr id="row10640301"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.169999999999998%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.61%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row19095777"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p3254085"><a name="p3254085"></a><a name="p3254085"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p62254326"><a name="p62254326"></a><a name="p62254326"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p9435611"><a name="p9435611"></a><a name="p9435611"></a>name of the ClusterRole.</p>
</td>
</tr>
<tr id="row17811636"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p33456451"><a name="p33456451"></a><a name="p33456451"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p25618043"><a name="p25618043"></a><a name="p25618043"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p61795587"><a name="p61795587"></a><a name="p61795587"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section18662134312520"></a>

N/A

## 响应消息<a name="section726119112252"></a>

**响应参数：**

响应参数的详细描述请参见[表2 响应参数](#table1154814995615)。

**表 2**  响应参数

<a name="table1154814995615"></a>
<table><thead align="left"><tr id="row455284915618"><th class="cellrowborder" valign="top" width="25.88%" id="mcps1.2.4.1.1"><p id="p15553124911564"><a name="p15553124911564"></a><a name="p15553124911564"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.53%" id="mcps1.2.4.1.2"><p id="p125561849185616"><a name="p125561849185616"></a><a name="p125561849185616"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.59%" id="mcps1.2.4.1.3"><p id="p205571649135612"><a name="p205571649135612"></a><a name="p205571649135612"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1478130175710"><td class="cellrowborder" valign="top" width="25.88%" headers="mcps1.2.4.1.1 "><p id="p12478130105717"><a name="p12478130105717"></a><a name="p12478130105717"></a>apiVersion</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.2.4.1.2 "><p id="p101319428574"><a name="p101319428574"></a><a name="p101319428574"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.59%" headers="mcps1.2.4.1.3 "><p id="p547913304576"><a name="p547913304576"></a><a name="p547913304576"></a>APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values.</p>
</td>
</tr>
<tr id="row10563349125616"><td class="cellrowborder" valign="top" width="25.88%" headers="mcps1.2.4.1.1 "><p id="p85631049125619"><a name="p85631049125619"></a><a name="p85631049125619"></a>kind</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.2.4.1.2 "><p id="p115651494566"><a name="p115651494566"></a><a name="p115651494566"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.59%" headers="mcps1.2.4.1.3 "><p id="p125661749135618"><a name="p125661749135618"></a><a name="p125661749135618"></a>Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase.</p>
</td>
</tr>
<tr id="row36873674"><td class="cellrowborder" valign="top" width="25.88%" headers="mcps1.2.4.1.1 "><p id="p6785175341110"><a name="p6785175341110"></a><a name="p6785175341110"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.2.4.1.2 "><p id="p1578195321111"><a name="p1578195321111"></a><a name="p1578195321111"></a><a href="#table204271324125219">metadata</a> object</p>
</td>
<td class="cellrowborder" valign="top" width="50.59%" headers="mcps1.2.4.1.3 "><p id="p1977810533112"><a name="p1977810533112"></a><a name="p1977810533112"></a>Standard object's metadata.</p>
</td>
</tr>
<tr id="row899203"><td class="cellrowborder" valign="top" width="25.88%" headers="mcps1.2.4.1.1 "><p id="p1177617531118"><a name="p1177617531118"></a><a name="p1177617531118"></a>rules</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.2.4.1.2 "><p id="p73260102467"><a name="p73260102467"></a><a name="p73260102467"></a><a href="#table157813483553">rules</a> object</p>
</td>
<td class="cellrowborder" valign="top" width="50.59%" headers="mcps1.2.4.1.3 "><p id="p19771175311119"><a name="p19771175311119"></a><a name="p19771175311119"></a>Rules holds all the PolicyRules for this ClusterRole</p>
</td>
</tr>
</tbody>
</table>

**表 3**  metadata字段数据结构说明

<a name="table204271324125219"></a>
<table><thead align="left"><tr id="row1942919240529"><th class="cellrowborder" valign="top" width="26.080000000000002%" id="mcps1.2.4.1.1"><p id="p2042942415210"><a name="p2042942415210"></a><a name="p2042942415210"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.470000000000002%" id="mcps1.2.4.1.2"><p id="p11430122413526"><a name="p11430122413526"></a><a name="p11430122413526"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.45%" id="mcps1.2.4.1.3"><p id="p54311824115213"><a name="p54311824115213"></a><a name="p54311824115213"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6675633103315"><td class="cellrowborder" valign="top" width="26.080000000000002%" headers="mcps1.2.4.1.1 "><p id="p0306076354"><a name="p0306076354"></a><a name="p0306076354"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="23.470000000000002%" headers="mcps1.2.4.1.2 "><p id="p163091475352"><a name="p163091475352"></a><a name="p163091475352"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.45%" headers="mcps1.2.4.1.3 "><p id="p73111175354"><a name="p73111175354"></a><a name="p73111175354"></a>Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated.</p>
</td>
</tr>
<tr id="row3320133193515"><td class="cellrowborder" valign="top" width="26.080000000000002%" headers="mcps1.2.4.1.1 "><p id="p9320233143513"><a name="p9320233143513"></a><a name="p9320233143513"></a>selfLink</p>
</td>
<td class="cellrowborder" valign="top" width="23.470000000000002%" headers="mcps1.2.4.1.2 "><p id="p1832011338354"><a name="p1832011338354"></a><a name="p1832011338354"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.45%" headers="mcps1.2.4.1.3 "><p id="p23202337356"><a name="p23202337356"></a><a name="p23202337356"></a>SelfLink is a URL representing this object. Populated by the system. Read-only.</p>
</td>
</tr>
<tr id="row1949154219351"><td class="cellrowborder" valign="top" width="26.080000000000002%" headers="mcps1.2.4.1.1 "><p id="p154913425354"><a name="p154913425354"></a><a name="p154913425354"></a>uid</p>
</td>
<td class="cellrowborder" valign="top" width="23.470000000000002%" headers="mcps1.2.4.1.2 "><p id="p249164273516"><a name="p249164273516"></a><a name="p249164273516"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.45%" headers="mcps1.2.4.1.3 "><p id="p19501142193512"><a name="p19501142193512"></a><a name="p19501142193512"></a>UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations. Populated by the system. Read-only.</p>
</td>
</tr>
<tr id="row1133801411715"><td class="cellrowborder" valign="top" width="26.080000000000002%" headers="mcps1.2.4.1.1 "><p id="p18338151417174"><a name="p18338151417174"></a><a name="p18338151417174"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="23.470000000000002%" headers="mcps1.2.4.1.2 "><p id="p173382144171"><a name="p173382144171"></a><a name="p173382144171"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.45%" headers="mcps1.2.4.1.3 "><p id="p8757204541716"><a name="p8757204541716"></a><a name="p8757204541716"></a>An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources. Populated by the system. Read-only.</p>
</td>
</tr>
<tr id="row1675633111612"><td class="cellrowborder" valign="top" width="26.080000000000002%" headers="mcps1.2.4.1.1 "><p id="p176233111619"><a name="p176233111619"></a><a name="p176233111619"></a>creationTimestamp</p>
</td>
<td class="cellrowborder" valign="top" width="23.470000000000002%" headers="mcps1.2.4.1.2 "><p id="p076233111610"><a name="p076233111610"></a><a name="p076233111610"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.45%" headers="mcps1.2.4.1.3 "><p id="p311744163019"><a name="p311744163019"></a><a name="p311744163019"></a>CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is represented in RFC3339 form and is in UTC. Populated by the system. Read-only. Null for lists.</p>
</td>
</tr>
</tbody>
</table>

**表 4**  rules字段数据结构说明

<a name="table157813483553"></a>
<table><thead align="left"><tr id="row78819487558"><th class="cellrowborder" valign="top" width="25.88%" id="mcps1.2.4.1.1"><p id="p88984811556"><a name="p88984811556"></a><a name="p88984811556"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="23.53%" id="mcps1.2.4.1.2"><p id="p119414818550"><a name="p119414818550"></a><a name="p119414818550"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.59%" id="mcps1.2.4.1.3"><p id="p39616488551"><a name="p39616488551"></a><a name="p39616488551"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1998144875516"><td class="cellrowborder" valign="top" width="25.88%" headers="mcps1.2.4.1.1 "><p id="p13100148135517"><a name="p13100148135517"></a><a name="p13100148135517"></a>apiGroups</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.2.4.1.2 "><p id="p1105848175510"><a name="p1105848175510"></a><a name="p1105848175510"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50.59%" headers="mcps1.2.4.1.3 "><p id="p141087482557"><a name="p141087482557"></a><a name="p141087482557"></a>APIGroups is the name of the APIGroup that contains the resources. If multiple API groups are specified, any action requested against one of the enumerated resources in any API group will be allowed.</p>
</td>
</tr>
<tr id="row8205416599"><td class="cellrowborder" valign="top" width="25.88%" headers="mcps1.2.4.1.1 "><p id="p2020104155912"><a name="p2020104155912"></a><a name="p2020104155912"></a>resources</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.2.4.1.2 "><p id="p15206485912"><a name="p15206485912"></a><a name="p15206485912"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50.59%" headers="mcps1.2.4.1.3 "><p id="p172013415591"><a name="p172013415591"></a><a name="p172013415591"></a>Resources is a list of resources this rule applies to. ResourceAll represents all resources.</p>
</td>
</tr>
<tr id="row1258661265916"><td class="cellrowborder" valign="top" width="25.88%" headers="mcps1.2.4.1.1 "><p id="p1558619125591"><a name="p1558619125591"></a><a name="p1558619125591"></a>verbs</p>
</td>
<td class="cellrowborder" valign="top" width="23.53%" headers="mcps1.2.4.1.2 "><p id="p175861112195911"><a name="p175861112195911"></a><a name="p175861112195911"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50.59%" headers="mcps1.2.4.1.3 "><p id="p95861212125919"><a name="p95861212125919"></a><a name="p95861212125919"></a>Verbs is a list of Verbs that apply to ALL the ResourceKinds and AttributeRestrictions contained in this rule. VerbAll represents all kinds.</p>
</td>
</tr>
</tbody>
</table>

**响应示例：**

```
{
    "kind" : "ClusterRole",
    "apiVersion" : "rbac.authorization.k8s.io/v1",
    "metadata" : {
        "name" : "secret-reader",
        "selfLink" : "/apis/rbac.authorization.k8s.io/v1/clusterroles/secret-reader",
        "uid" : "f2cf199e-f1f0-11e8-b449-fa163ec24e06",
        "resourceVersion" : "13211",
        "creationTimestamp" : "2018-11-27T03:03:00Z"
    },
    "rules" : [ {
        "verbs" : [ "get", "watch", "list" ],
        "apiGroups" : [ "" ],
        "resources" : [ "secrets" ]
    } ]
}
```

## 状态码<a name="section534515230266"></a>

[状态码](#d0e43055)描述API的状态码。

**表 5**  状态码

<a name="d0e43055"></a>
<table><thead align="left"><tr id="row20813512"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p8172937"><a name="p8172937"></a><a name="p8172937"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p58028199"><a name="p58028199"></a><a name="p58028199"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row2663689"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p14432280"><a name="p14432280"></a><a name="p14432280"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p0978454104816"><a name="p0978454104816"></a><a name="p0978454104816"></a>OK</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

