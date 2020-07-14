# 删除PersistentVolumeClaim<a name="cci_02_3086"></a>

## 功能介绍<a name="sdc08610ef8314ab09a5b279ba59294bc"></a>

删除PersistentVolumeClaim。

## URI<a name="sc869e0507a5d4e9faa97547f45765876"></a>

DELETE  /api/v1/namespaces/\{namespace\}/persistentvolumeclaims/\{name\}

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
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the PersistentVolumeClaim.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="t101edc7f76364f35a20a711cac4e7e02"></a>
<table><thead align="left"><tr id="r187debc2c7c34469b9f2583f2eeb9928"><th class="cellrowborder" valign="top" width="20.369999999999997%" id="mcps1.2.4.1.1"><p id="a730c657a0f4643748672df8aae5ac8f9"><a name="a730c657a0f4643748672df8aae5ac8f9"></a><a name="a730c657a0f4643748672df8aae5ac8f9"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.54%" id="mcps1.2.4.1.2"><p id="p16157644131910"><a name="p16157644131910"></a><a name="p16157644131910"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="62.09%" id="mcps1.2.4.1.3"><p id="p171571944111913"><a name="p171571944111913"></a><a name="p171571944111913"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r9dde66d7099e4471b134e6a91a4b9ac3"><td class="cellrowborder" valign="top" width="20.369999999999997%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615049_p620075391118"><a name="zh-cn_topic_0079615049_p620075391118"></a><a name="zh-cn_topic_0079615049_p620075391118"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615049_p565547941118"><a name="zh-cn_topic_0079615049_p565547941118"></a><a name="zh-cn_topic_0079615049_p565547941118"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.09%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615049_p175355641118"><a name="zh-cn_topic_0079615049_p175355641118"></a><a name="zh-cn_topic_0079615049_p175355641118"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="r11b3dd0b982e4e78a1cb87a12b30f0e3"><td class="cellrowborder" valign="top" width="20.369999999999997%" headers="mcps1.2.4.1.1 "><p id="abc9c23c101404c82b8d9b4ae89d795a5"><a name="abc9c23c101404c82b8d9b4ae89d795a5"></a><a name="abc9c23c101404c82b8d9b4ae89d795a5"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="17.54%" headers="mcps1.2.4.1.2 "><p id="ab07b1d5d925a4b749b6650227f896f79"><a name="ab07b1d5d925a4b749b6650227f896f79"></a><a name="ab07b1d5d925a4b749b6650227f896f79"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.09%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615049_p166287132138"><a name="zh-cn_topic_0079615049_p166287132138"></a><a name="zh-cn_topic_0079615049_p166287132138"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="r5b7add32b2624ea89cad862fc2f557f7"><td class="cellrowborder" valign="top" width="20.369999999999997%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615049_p915302817133"><a name="zh-cn_topic_0079615049_p915302817133"></a><a name="zh-cn_topic_0079615049_p915302817133"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="17.54%" headers="mcps1.2.4.1.2 "><p id="af990c0414a0f4cffa8a93df2ed505b39"><a name="af990c0414a0f4cffa8a93df2ed505b39"></a><a name="af990c0414a0f4cffa8a93df2ed505b39"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.09%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615049_p115382812137"><a name="zh-cn_topic_0079615049_p115382812137"></a><a name="zh-cn_topic_0079615049_p115382812137"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="ra374123fff5543b784cfc69a57c520c7"><td class="cellrowborder" valign="top" width="20.369999999999997%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615049_p878183016139"><a name="zh-cn_topic_0079615049_p878183016139"></a><a name="zh-cn_topic_0079615049_p878183016139"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="17.54%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615049_p27823091319"><a name="zh-cn_topic_0079615049_p27823091319"></a><a name="zh-cn_topic_0079615049_p27823091319"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="62.09%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615049_p197853091318"><a name="zh-cn_topic_0079615049_p197853091318"></a><a name="zh-cn_topic_0079615049_p197853091318"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.</p>
<p id="p121661258102610"><a name="p121661258102610"></a><a name="p121661258102610"></a>Orphan - orphan the dependents</p>
<p id="p101265112712"><a name="p101265112712"></a><a name="p101265112712"></a>Background - allow the garbage collector to delete the dependents in the background</p>
<p id="p12237384273"><a name="p12237384273"></a><a name="p12237384273"></a>Foreground - a cascading policy that deletes all dependents in the foreground</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="sb038a48d22e547e3a9a0545b572cf8b6"></a>

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

## 响应消息<a name="se3a9951114354928a0998dcc1d2e25fe"></a>

**响应参数：**

响应参数的详细描述请参见[表72](数据结构.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "PersistentVolumeClaim",
    "apiVersion": "v1",
    "metadata": {
        "name": "pvc-test",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/persistentvolumeclaims/pvc-test",
        "uid": "5a9ab4c1-b1a6-11e8-8b84-c88d83be759f",
        "resourceVersion": "5669396",
        "creationTimestamp": "2018-09-06T07:27:47Z",
        "deletionTimestamp": "2018-09-06T07:51:51Z",
        "deletionGracePeriodSeconds": 0,
        "annotations": {
            "volume.beta.kubernetes.io/storage-class": "sata",
            "volume.beta.kubernetes.io/storage-provisioner": "flexvolume-huawei.com/fuxivol"
        },
        "finalizers": [
            "kubernetes.io/pvc-protection"
        ],
        "enable": true
    },
    "spec": {
        "accessModes": [
            "ReadWriteMany"
        ],
        "resources": {
            "requests": {
                "storage": "10Gi"
            }
        }
    },
    "status": {
        "phase": "Pending"
    }
}
```

## 状态码<a name="sa8b72c0600224440a2fe1daf83f5b73a"></a>

[表3](#t10fde947e6644cfa87987be473137d2b)描述API的状态码。

**表 3**  状态码

<a name="t10fde947e6644cfa87987be473137d2b"></a>
<table><thead align="left"><tr id="ra98a80c0400848a18557491c3f9e4f64"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p151761544131914"><a name="p151761544131914"></a><a name="p151761544131914"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p817714411920"><a name="p817714411920"></a><a name="p817714411920"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r3e3f40d0ede848c4bbbb7b4863b6af4c"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="a9e2f86eb816746e280d1ec69bef19894"><a name="a9e2f86eb816746e280d1ec69bef19894"></a><a name="a9e2f86eb816746e280d1ec69bef19894"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="a97163082ddd5447b884268416909cc62"><a name="a97163082ddd5447b884268416909cc62"></a><a name="a97163082ddd5447b884268416909cc62"></a>Delete a PersistentVolumeClaim resource object successfully.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

