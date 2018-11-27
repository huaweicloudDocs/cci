# 替换ConfigMap<a name="cci_02_3067"></a>

## 功能介绍<a name="section63540285"></a>

替换ConfigMap。

The following fields can be updated:

-   metadata.labels
-   metadata.annotations
-   data

## URI<a name="section34991658"></a>

PUT /api/v1/namespaces/\{namespace\}/configmaps/\{name\}

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

<a name="d0e43866"></a>
<table><thead align="left"><tr id="row28873940"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5943917"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p11695287"><a name="p11695287"></a><a name="p11695287"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="p7794181"><a name="p7794181"></a><a name="p7794181"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="p27348928"><a name="p27348928"></a><a name="p27348928"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="d0e43915"></a>

**请求参数：**

请求参数的详细描述请参见[表122](公共参数.md#table79541510192317)。

**请求示例：**

将[创建ConfigMap](创建ConfigMap.md)创建的ConfigMap的property\_1的值改为“test2“。

```
{
    "apiVersion": "v1",
    "data": {
        "property_1": "test2"
    },
    "kind": "ConfigMap",
    "metadata": {
        "name": "configmap-test"
    }
}
```

## 响应消息<a name="section15752039"></a>

**响应参数：**

响应参数的详细描述请参见[表122](公共参数.md#table79541510192317)。

**响应示例：**

```
{
  "kind": "ConfigMap",
  "apiVersion": "v1",
  "metadata": {
    "name": "configmap-test",
    "namespace": "namespace-test",
    "selfLink": "/api/v1/namespaces/namespace-test/configmaps/configmap-test",
    "uid": "379519a3-aff0-11e8-8f17-c81fbe371a17",
    "resourceVersion": "5172849",
    "creationTimestamp": "2018-09-04T03:11:29Z",
    "enable": true
  },
  "data": {
    "property_1": "test2"
  }
}
```

## 状态码<a name="section7550625"></a>

[表3](#d0e43958)描述API的状态码。

**表 3**  状态码

<a name="d0e43958"></a>
<table><thead align="left"><tr id="row63594840"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p50908388"><a name="p50908388"></a><a name="p50908388"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p29938789"><a name="p29938789"></a><a name="p29938789"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row15878750163618"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1387816501365"><a name="p1387816501365"></a><a name="p1387816501365"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p28437418"><a name="p28437418"></a><a name="p28437418"></a>This operation succeeds.</p>
</td>
</tr>
</tbody>
</table>

