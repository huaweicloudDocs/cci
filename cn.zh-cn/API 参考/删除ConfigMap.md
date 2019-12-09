# 删除ConfigMap<a name="cci_02_3068"></a>

## 功能介绍<a name="section4992645"></a>

删除ConfigMap。

## URI<a name="section44933808"></a>

DELETE /api/v1/namespaces/\{namespace\}/configmaps/\{name\}

**表 1**  Path参数

<a name="table1696332124519"></a>
<table><thead align="left"><tr id="row11961332194516"><th class="cellrowborder" valign="top" width="24%" id="mcps1.2.3.1.1"><p id="p396032144518"><a name="p396032144518"></a><a name="p396032144518"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="76%" id="mcps1.2.3.1.2"><p id="p18962325454"><a name="p18962325454"></a><a name="p18962325454"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9960327457"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p1496113214456"><a name="p1496113214456"></a><a name="p1496113214456"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p141902036155717"><a name="p141902036155717"></a><a name="p141902036155717"></a>Object name and auth scope, such as for teams and projects.</p>
</td>
</tr>
<tr id="row13794857171116"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p5984165818113"><a name="p5984165818113"></a><a name="p5984165818113"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the Configmap.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="d0e43122"></a>
<table><thead align="left"><tr id="row4620112"><th class="cellrowborder" valign="top" width="24.434343434343436%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.929292929292929%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.63636363636363%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row38131941"><td class="cellrowborder" valign="top" width="24.434343434343436%" headers="mcps1.2.4.1.1 "><p id="p1679523"><a name="p1679523"></a><a name="p1679523"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="14.929292929292929%" headers="mcps1.2.4.1.2 "><p id="p1823714"><a name="p1823714"></a><a name="p1823714"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.63636363636363%" headers="mcps1.2.4.1.3 "><p id="p13503178"><a name="p13503178"></a><a name="p13503178"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row39484685"><td class="cellrowborder" valign="top" width="24.434343434343436%" headers="mcps1.2.4.1.1 "><p id="p44142899"><a name="p44142899"></a><a name="p44142899"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="14.929292929292929%" headers="mcps1.2.4.1.2 "><p id="p18805103"><a name="p18805103"></a><a name="p18805103"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.63636363636363%" headers="mcps1.2.4.1.3 "><p id="p46818342"><a name="p46818342"></a><a name="p46818342"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="row18711900"><td class="cellrowborder" valign="top" width="24.434343434343436%" headers="mcps1.2.4.1.1 "><p id="p39268954"><a name="p39268954"></a><a name="p39268954"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="14.929292929292929%" headers="mcps1.2.4.1.2 "><p id="p26668680"><a name="p26668680"></a><a name="p26668680"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.63636363636363%" headers="mcps1.2.4.1.3 "><p id="p12679438"><a name="p12679438"></a><a name="p12679438"></a>Deprecated: Use the PropagationPolicy. This field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="row47006082"><td class="cellrowborder" valign="top" width="24.434343434343436%" headers="mcps1.2.4.1.1 "><p id="p49396288"><a name="p49396288"></a><a name="p49396288"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="14.929292929292929%" headers="mcps1.2.4.1.2 "><p id="p41676395"><a name="p41676395"></a><a name="p41676395"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.63636363636363%" headers="mcps1.2.4.1.3 "><p id="p48885565"><a name="p48885565"></a><a name="p48885565"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section1751091"></a>

**请求参数：**

请求参数如[表64](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

```
{
    "kind": "DeleteOptions",
    "apiVersion": "v1",
    "gracePeriodSeconds": 0
}
```

## 响应消息<a name="section15759823"></a>

**响应参数：**

响应参数的详细描述请参见[表72](数据结构.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "Status",
    "apiVersion": "v1",
    "metadata": {},
    "status": "Success",
    "details": {
        "name": "configmap-test",
        "kind": "configmaps",
        "uid": "379519a3-aff0-11e8-8f17-c81fbe371a17"
    },
    "code": 200
}
```

## 状态码<a name="section7620686"></a>

[表3](#d0e43397)描述API的状态码。

**表 3**  状态码

<a name="d0e43397"></a>
<table><thead align="left"><tr id="row30119043"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p23723412"><a name="p23723412"></a><a name="p23723412"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p42548185"><a name="p42548185"></a><a name="p42548185"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row23850938"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p52877857"><a name="p52877857"></a><a name="p52877857"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p55247987"><a name="p55247987"></a><a name="p55247987"></a>Delete a ConfigMap resource object successfully.</p>
</td>
</tr>
</tbody>
</table>

