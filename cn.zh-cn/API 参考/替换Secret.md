# 替换Secret<a name="cci_02_3077"></a>

## 功能介绍<a name="s2fa7c6b09ad0449ebce13163ee876960"></a>

替换Secret。

其中以下字段支持更新：

-   metadata.labels
-   metadata.annotations
-   data

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   当“type“的值为“Opaque“时，“data“的“key“和“value“都可以更新。  
>-   当“type“的值不为“Opaque“时，“data“的“value“可以更新。  

## URI<a name="se7a801b22ec44205a03503a15151ba92"></a>

PUT /api/v1/namespaces/\{namespace\}/secrets/\{name\}

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
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the Secret.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079615031_table22030964"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615031_row15494477"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615031_p47093149"><a name="zh-cn_topic_0079615031_p47093149"></a><a name="zh-cn_topic_0079615031_p47093149"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p3516329201621"><a name="p3516329201621"></a><a name="p3516329201621"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0079615031_p8945359"><a name="zh-cn_topic_0079615031_p8945359"></a><a name="zh-cn_topic_0079615031_p8945359"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615031_row53485440"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615031_p37353378"><a name="zh-cn_topic_0079615031_p37353378"></a><a name="zh-cn_topic_0079615031_p37353378"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615031_p5724764"><a name="zh-cn_topic_0079615031_p5724764"></a><a name="zh-cn_topic_0079615031_p5724764"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615031_p61052759"><a name="zh-cn_topic_0079615031_p61052759"></a><a name="zh-cn_topic_0079615031_p61052759"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0079615031_ref458786529"></a>

**请求参数：**

请求参数的详细描述请参见[表123](数据结构.md#zh-cn_topic_0079614900_ref458786458)。

**请求示例：**

将[创建Secret](创建Secret.md)创建的Secret中key2替换为test。

```
{
    "apiVersion": "v1",
    "kind": "Secret",
    "metadata": {
        "name": "secret-test"
    },
    "type": "Opaque",
    "data": {
        "key1": "MWYyZDFlMmU2N2Rm",
        "test": "dGVzdA=="
    }
}
```

## 响应消息<a name="s62e9d00c756e4ae99025f3a29117287f"></a>

**响应参数：**

响应参数的详细描述请参见[表123](数据结构.md#zh-cn_topic_0079614900_ref458786458)。

**响应示例：**

```
{
    "kind": "Secret",
    "apiVersion": "v1",
    "metadata": {
        "name": "secret-test",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/secrets/secret-test",
        "uid": "e6170b6d-aff6-11e8-8f17-c81fbe371a17",
        "resourceVersion": "5199399",
        "creationTimestamp": "2018-09-04T03:59:19Z",
        "enable": true
    },
    "data": {
        "key1": "MWYyZDFlMmU2N2Rm",
        "test": "dGVzdA=="
    },
    "type": "Opaque"
}
```

## 状态码<a name="s0cae25a23bb14c80b7b9465f8da69cd7"></a>

[表3](#zh-cn_topic_0079615031_table64060950)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615031_table64060950"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615031_row64282674"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.3.1.1"><p id="p57631252201621"><a name="p57631252201621"></a><a name="p57631252201621"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="80%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0079615031_p46527158"><a name="zh-cn_topic_0079615031_p46527158"></a><a name="zh-cn_topic_0079615031_p46527158"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615031_row10603493"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615031_p53576637"><a name="zh-cn_topic_0079615031_p53576637"></a><a name="zh-cn_topic_0079615031_p53576637"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="80%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615031_p44740325"><a name="zh-cn_topic_0079615031_p44740325"></a><a name="zh-cn_topic_0079615031_p44740325"></a>This operation succeeds, and a secret resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

