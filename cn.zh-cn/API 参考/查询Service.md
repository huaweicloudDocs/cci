# 查询Service<a name="cci_02_3050"></a>

## 功能介绍<a name="s6b63abeb0a574a7a9c13de5369a91cd8"></a>

查询Service的详细信息。

## URI<a name="s2a208d531ff9407b93924d7c313193b8"></a>

GET /api/v1/namespaces/\{namespace\}/services/\{name\}

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
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the Service.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079614941_table43974095"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614941_row47185870"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614941_p63959112"><a name="zh-cn_topic_0079614941_p63959112"></a><a name="zh-cn_topic_0079614941_p63959112"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="25%" id="mcps1.2.4.1.2"><p id="p54432917195332"><a name="p54432917195332"></a><a name="p54432917195332"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="42%" id="mcps1.2.4.1.3"><p id="p46990176195332"><a name="p46990176195332"></a><a name="p46990176195332"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614941_row56542298"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614941_p16523463"><a name="zh-cn_topic_0079614941_p16523463"></a><a name="zh-cn_topic_0079614941_p16523463"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614941_p63332116"><a name="zh-cn_topic_0079614941_p63332116"></a><a name="zh-cn_topic_0079614941_p63332116"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614941_p29627753"><a name="zh-cn_topic_0079614941_p29627753"></a><a name="zh-cn_topic_0079614941_p29627753"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="r0af24e6998b447a7b420c9ba8d740997"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="a90c1431310924496a5cc65d5b4246e84"><a name="a90c1431310924496a5cc65d5b4246e84"></a><a name="a90c1431310924496a5cc65d5b4246e84"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.2 "><p id="a5209f92e2e0a4d0cbd92d02f2828855c"><a name="a5209f92e2e0a4d0cbd92d02f2828855c"></a><a name="a5209f92e2e0a4d0cbd92d02f2828855c"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.4.1.3 "><p id="a69e76f9c221f4f5aad657379aae91d95"><a name="a69e76f9c221f4f5aad657379aae91d95"></a><a name="a69e76f9c221f4f5aad657379aae91d95"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="r96bb6bf9ae1440009077fa844f28a88e"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614941_p151474572434"><a name="zh-cn_topic_0079614941_p151474572434"></a><a name="zh-cn_topic_0079614941_p151474572434"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="25%" headers="mcps1.2.4.1.2 "><p id="a0aa4cab1194c44d2b2658f322b9fd0fc"><a name="a0aa4cab1194c44d2b2658f322b9fd0fc"></a><a name="a0aa4cab1194c44d2b2658f322b9fd0fc"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="42%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614941_p114755710438"><a name="zh-cn_topic_0079614941_p114755710438"></a><a name="zh-cn_topic_0079614941_p114755710438"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s24d2fb0a92bc4481b97f1980a208a6ec"></a>

N/A

## 响应消息<a name="s058feaad90fa4e52a6d698f3cd609786"></a>

**响应参数：**

响应参数如[表101](数据结构.md#zh-cn_topic_0079615000_ref458759328)所示。

**响应示例：**

```
{
    "kind": "Service",
    "apiVersion": "v1",
    "metadata": {
        "name": "redis",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/services/redis",
        "uid": "d6a1ce79-afdb-11e8-b6ef-f898ef6c78b4",
        "resourceVersion": "5146412",
        "creationTimestamp": "2018-09-04T00:45:36Z",
        "labels": {
            "app": "redis"
        },
        "enable": true
    },
    "spec": {
        "ports": [
            {
                "name": "service0",
                "protocol": "TCP",
                "port": 8080,
                "targetPort": 80
            }
        ],
        "selector": {
            "app": "redis"
        },
        "clusterIP": "10.247.212.210",
        "type": "ClusterIP",
        "sessionAffinity": "None"
    },
    "status": {
        "loadBalancer": {}
    }
}
```

## 状态码<a name="sd2fb196246a241cea5cbced82b71a7c0"></a>

[表3](#zh-cn_topic_0079614941_table49299249)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079614941_table49299249"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614941_row51657386"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p47913009195332"><a name="p47913009195332"></a><a name="p47913009195332"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p55748497195332"><a name="p55748497195332"></a><a name="p55748497195332"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614941_row26379626"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079614941_p56374952"><a name="zh-cn_topic_0079614941_p56374952"></a><a name="zh-cn_topic_0079614941_p56374952"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614941_p2968403"><a name="zh-cn_topic_0079614941_p2968403"></a><a name="zh-cn_topic_0079614941_p2968403"></a>This operation succeeds, and a Service resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

