# 查询Namespace<a name="cci_02_3004"></a>

## 功能介绍<a name="scf9d2368d0b84db5ada29db6edfd4bbd"></a>

查询Namespace的详细信息。

## URI<a name="sb2f55ca34eb140d59a0949c9d56ac022"></a>

GET /api/v1/namespaces/\{name\}

**表 1**  Path参数

<a name="table1696332124519"></a>
<table><thead align="left"><tr id="row11961332194516"><th class="cellrowborder" valign="top" width="24%" id="mcps1.2.3.1.1"><p id="p396032144518"><a name="p396032144518"></a><a name="p396032144518"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="76%" id="mcps1.2.3.1.2"><p id="p18962325454"><a name="p18962325454"></a><a name="p18962325454"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9960327457"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p1496113214456"><a name="p1496113214456"></a><a name="p1496113214456"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p796193274515"><a name="p796193274515"></a><a name="p796193274515"></a>Name of the Namespace.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079614931_table56165728"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614931_row20888703"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614931_p14263389"><a name="zh-cn_topic_0079614931_p14263389"></a><a name="zh-cn_topic_0079614931_p14263389"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.202020202020204%" id="mcps1.2.4.1.2"><p id="p20413034201629"><a name="p20413034201629"></a><a name="p20413034201629"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="46.464646464646464%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0079614931_p32345284"><a name="zh-cn_topic_0079614931_p32345284"></a><a name="zh-cn_topic_0079614931_p32345284"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614931_row2722332"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614931_p19182316"><a name="zh-cn_topic_0079614931_p19182316"></a><a name="zh-cn_topic_0079614931_p19182316"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="20.202020202020204%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614931_p10263773"><a name="zh-cn_topic_0079614931_p10263773"></a><a name="zh-cn_topic_0079614931_p10263773"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="46.464646464646464%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614931_p26059286"><a name="zh-cn_topic_0079614931_p26059286"></a><a name="zh-cn_topic_0079614931_p26059286"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="re57ad01ee3a34ce8a3654fb86a2fda40"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="a63bd058863724e12b9d15146171392f0"><a name="a63bd058863724e12b9d15146171392f0"></a><a name="a63bd058863724e12b9d15146171392f0"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="20.202020202020204%" headers="mcps1.2.4.1.2 "><p id="ae54f3dedf0af4ebfad7f25d07b720fa3"><a name="ae54f3dedf0af4ebfad7f25d07b720fa3"></a><a name="ae54f3dedf0af4ebfad7f25d07b720fa3"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="46.464646464646464%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614931_p398385119426"><a name="zh-cn_topic_0079614931_p398385119426"></a><a name="zh-cn_topic_0079614931_p398385119426"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="radf0b1c1f27e4c64ab4302c90a1be0e1"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="a6e0c1acd92cc45b38eb0423933ea7004"><a name="a6e0c1acd92cc45b38eb0423933ea7004"></a><a name="a6e0c1acd92cc45b38eb0423933ea7004"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="20.202020202020204%" headers="mcps1.2.4.1.2 "><p id="aa87f0f2c7d234e6292a7f45884335324"><a name="aa87f0f2c7d234e6292a7f45884335324"></a><a name="aa87f0f2c7d234e6292a7f45884335324"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="46.464646464646464%" headers="mcps1.2.4.1.3 "><p id="aae71f6e3574c4b11883d9f396d6b5924"><a name="aae71f6e3574c4b11883d9f396d6b5924"></a><a name="aae71f6e3574c4b11883d9f396d6b5924"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="sb8143102599b4bd19398ad00f0bcd799"></a>

N/A

## 响应消息<a name="sa8800f7e4a154473b712eb496a26a20a"></a>

**响应参数：**

响应参数的详细描述请参见[表2](创建Namespace.md#zh-cn_topic_0079615062_ref458759029)。其中metadata.annotations说明如下[表3](#table759162211124)所示。

**表 3**  metadata.annotations必选字段说明

<a name="table759162211124"></a>
<table><thead align="left"><tr id="row0591622101219"><th class="cellrowborder" valign="top" width="35.06%" id="mcps1.2.4.1.1"><p id="p1975132291213"><a name="p1975132291213"></a><a name="p1975132291213"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.33%" id="mcps1.2.4.1.2"><p id="p87522211129"><a name="p87522211129"></a><a name="p87522211129"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="48.61%" id="mcps1.2.4.1.3"><p id="p1075142218127"><a name="p1075142218127"></a><a name="p1075142218127"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row13751122161210"><td class="cellrowborder" valign="top" width="35.06%" headers="mcps1.2.4.1.1 "><p id="p689191014121"><a name="p689191014121"></a><a name="p689191014121"></a>pv.kubernetes.io/enable-dynamic-provisioning</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p19751022111211"><a name="p19751022111211"></a><a name="p19751022111211"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.61%" headers="mcps1.2.4.1.3 "><p id="p115541816129"><a name="p115541816129"></a><a name="p115541816129"></a>是否支持动态创建存储。</p>
</td>
</tr>
<tr id="row1499785020124"><td class="cellrowborder" valign="top" width="35.06%" headers="mcps1.2.4.1.1 "><p id="p11997175031212"><a name="p11997175031212"></a><a name="p11997175031212"></a>tenant.kubernetes.io/domain-id</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p114411249141413"><a name="p114411249141413"></a><a name="p114411249141413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.61%" headers="mcps1.2.4.1.3 "><p id="p6997195015128"><a name="p6997195015128"></a><a name="p6997195015128"></a>用户的账号ID。</p>
</td>
</tr>
<tr id="row191704511126"><td class="cellrowborder" valign="top" width="35.06%" headers="mcps1.2.4.1.1 "><p id="p181706518124"><a name="p181706518124"></a><a name="p181706518124"></a>tenant.kubernetes.io/domain-name</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p645744931416"><a name="p645744931416"></a><a name="p645744931416"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.61%" headers="mcps1.2.4.1.3 "><p id="p15170165112125"><a name="p15170165112125"></a><a name="p15170165112125"></a>用户的账号名。</p>
</td>
</tr>
<tr id="row93581510128"><td class="cellrowborder" valign="top" width="35.06%" headers="mcps1.2.4.1.1 "><p id="p14358165171218"><a name="p14358165171218"></a><a name="p14358165171218"></a>tenant.kubernetes.io/project-id</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p3457349201411"><a name="p3457349201411"></a><a name="p3457349201411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="48.61%" headers="mcps1.2.4.1.3 "><p id="p5358115114122"><a name="p5358115114122"></a><a name="p5358115114122"></a>用户的项目ID。</p>
</td>
</tr>
<tr id="row3285164119146"><td class="cellrowborder" valign="top" width="35.06%" headers="mcps1.2.4.1.1 "><p id="p5285124118146"><a name="p5285124118146"></a><a name="p5285124118146"></a>tenant.kubernetes.io/project-name</p>
</td>
<td class="cellrowborder" valign="top" width="16.33%" headers="mcps1.2.4.1.2 "><p id="p3472649171413"><a name="p3472649171413"></a><a name="p3472649171413"></a>String</p>
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
        "enable": true
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

## 状态码<a name="s7e98581a81a84cc9b0ed724e05454b12"></a>

[表4](#zh-cn_topic_0079614931_table8575450)描述API的状态码。

**表 4**  状态码

<a name="zh-cn_topic_0079614931_table8575450"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614931_row63149496"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p49872066201629"><a name="p49872066201629"></a><a name="p49872066201629"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="zh-cn_topic_0079614931_p60827539"><a name="zh-cn_topic_0079614931_p60827539"></a><a name="zh-cn_topic_0079614931_p60827539"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614931_row28083633"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079614931_p60181840"><a name="zh-cn_topic_0079614931_p60181840"></a><a name="zh-cn_topic_0079614931_p60181840"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614931_p42890904"><a name="zh-cn_topic_0079614931_p42890904"></a><a name="zh-cn_topic_0079614931_p42890904"></a>This operation succeeds, and a Namespace resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

