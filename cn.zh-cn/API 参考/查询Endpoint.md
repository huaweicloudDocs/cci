# 查询Endpoint<a name="cci_02_3125"></a>

## 功能介绍<a name="zh-cn_topic_0079615072_section885082"></a>

查询Endpoint。

## URI<a name="s4c063734e7b04b8aa1818085c9fdd5f3"></a>

GET /api/v1/namespaces/\{namespace\}/endpoints/\{name\}

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
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the event.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="d0e45403"></a>
<table><thead align="left"><tr id="row15382595"><th class="cellrowborder" valign="top" width="16.851685168516852%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.11101110111011%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="73.03730373037303%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row50128196"><td class="cellrowborder" valign="top" width="16.851685168516852%" headers="mcps1.2.4.1.1 "><p id="p33852041"><a name="p33852041"></a><a name="p33852041"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="10.11101110111011%" headers="mcps1.2.4.1.2 "><p id="p57660778"><a name="p57660778"></a><a name="p57660778"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="73.03730373037303%" headers="mcps1.2.4.1.3 "><p id="p40011473"><a name="p40011473"></a><a name="p40011473"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row24558937"><td class="cellrowborder" valign="top" width="16.851685168516852%" headers="mcps1.2.4.1.1 "><p id="p43116865"><a name="p43116865"></a><a name="p43116865"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="10.11101110111011%" headers="mcps1.2.4.1.2 "><p id="p2805153"><a name="p2805153"></a><a name="p2805153"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="73.03730373037303%" headers="mcps1.2.4.1.3 "><p id="p8957179144314"><a name="p8957179144314"></a><a name="p8957179144314"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="row16784107"><td class="cellrowborder" valign="top" width="16.851685168516852%" headers="mcps1.2.4.1.1 "><p id="p17335461"><a name="p17335461"></a><a name="p17335461"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="10.11101110111011%" headers="mcps1.2.4.1.2 "><p id="p61995128"><a name="p61995128"></a><a name="p61995128"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="73.03730373037303%" headers="mcps1.2.4.1.3 "><p id="p12754151974311"><a name="p12754151974311"></a><a name="p12754151974311"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="se5dc3a3d39a34f22a7353e5b56820ee1"></a>

N/A

## 响应消息<a name="sb016aaee185e4c39889395b7b34f7968"></a>

**响应参数：**

响应参数的详细描述请参见[表134](数据结构.md#table143351122168)。

**响应示例：**

```
{
    "kind": "Endpoints",
    "apiVersion": "v1",
    "metadata": {
        "name": "cluster-test",
        "namespace": "default",
        "selfLink": "/api/v1/namespaces/default/endpoints/cluster-test",
        "uid": "81b1503d-5960-11e6-b444-286ed488fafe",
        "resourceVersion": "18186",
        "creationTimestamp": "2016-08-03T09:56:10Z"
    },
    "subsets": [
        {
            "addresses": [
                {
                    "ip": "172.16.106.152"
                },
                {
                    "ip": "172.16.79.157"
                }
            ],
            "ports": [
                {
                    "port": 1,
                    "protocol": "TCP"
                }
            ]
        }
    ]
}
```

## 状态码<a name="sf826b071d47f4d51bc560ff6f2ef1fbf"></a>

**表 3**  状态码

<a name="zh-cn_topic_0079615072_table12672824"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615072_row17662689"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p39753582201644"><a name="p39753582201644"></a><a name="p39753582201644"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0079615072_p55008403"><a name="zh-cn_topic_0079615072_p55008403"></a><a name="zh-cn_topic_0079615072_p55008403"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615072_row26495667"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615072_p65774263"><a name="zh-cn_topic_0079615072_p65774263"></a><a name="zh-cn_topic_0079615072_p65774263"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615072_p26115080"><a name="zh-cn_topic_0079615072_p26115080"></a><a name="zh-cn_topic_0079615072_p26115080"></a>This operation succeeds, and an Endpoint resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

