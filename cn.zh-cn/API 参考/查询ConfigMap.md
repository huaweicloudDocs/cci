# 查询ConfigMap<a name="cci_02_3070"></a>

## 功能介绍<a name="section55356496"></a>

查询ConfigMap详细信息。

## URI<a name="section28446419"></a>

GET /api/v1/namespaces/\{namespace\}/configmaps/\{name\}

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

<a name="d0e43679"></a>
<table><thead align="left"><tr id="row18163667"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.303030303030305%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row32810792"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p40428502"><a name="p40428502"></a><a name="p40428502"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.4.1.2 "><p id="p53483269"><a name="p53483269"></a><a name="p53483269"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.2.4.1.3 "><p id="p37177565"><a name="p37177565"></a><a name="p37177565"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row8339656"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p4423518"><a name="p4423518"></a><a name="p4423518"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.4.1.2 "><p id="p22760714"><a name="p22760714"></a><a name="p22760714"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.2.4.1.3 "><p id="p31678513"><a name="p31678513"></a><a name="p31678513"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="row16671167"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p8187309"><a name="p8187309"></a><a name="p8187309"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.4.1.2 "><p id="p59192267"><a name="p59192267"></a><a name="p59192267"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.2.4.1.3 "><p id="p29844289"><a name="p29844289"></a><a name="p29844289"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section54691182"></a>

N/A

## 响应消息<a name="section22458594"></a>

**响应参数：**

响应参数的详细描述请参见[表122](数据结构.md#table79541510192317)。

**响应示例：**

```
{
    "kind": "ConfigMap",
    "apiVersion": "v1",
    "metadata": {
        "name": "test-12130306",
        "namespace": "ns-12130306-s",
        "selfLink": "/api/v1/namespaces/ns-12130306-s/configmaps/test-12130306",
        "uid": "efd6d9e0-dfb3-11e7-9c19-fa163e2d897b",
        "resourceVersion": "419141",
        "creationTimestamp": "2017-12-13T03:15:57Z",
        "enable": true
    },
    "data": {
        "property_1": "new"
    }
}
```

## 状态码<a name="section800761"></a>

[表3](#d0e43778)描述API的状态码。

**表 3**  状态码

<a name="d0e43778"></a>
<table><thead align="left"><tr id="row4687938"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p44178660"><a name="p44178660"></a><a name="p44178660"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p21701723"><a name="p21701723"></a><a name="p21701723"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row13009167"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p47109607"><a name="p47109607"></a><a name="p47109607"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p57781836"><a name="p57781836"></a><a name="p57781836"></a>This operation succeeds, and a ConfigMap resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

