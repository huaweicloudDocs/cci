# 删除Pod<a name="cci_02_3007"></a>

## 功能介绍<a name="s741ec6c50c454471bb3292d7950b0098"></a>

删除Pod。

## URI<a name="s7d7ef3af438c482abce017b9cb2ad884"></a>

DELETE /api/v1/namespaces/\{namespace\}/pods/\{name\}

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
<tr id="row725102210428"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p1655710298422"><a name="p1655710298422"></a><a name="p1655710298422"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p17214336164213"><a name="p17214336164213"></a><a name="p17214336164213"></a>Name of the Pod.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079615056_table52824818"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615056_row59343410"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615056_p42086942"><a name="zh-cn_topic_0079615056_p42086942"></a><a name="zh-cn_topic_0079615056_p42086942"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="22%" id="mcps1.2.4.1.2"><p id="p6618481203046"><a name="p6618481203046"></a><a name="p6618481203046"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="45%" id="mcps1.2.4.1.3"><p id="p66334913203046"><a name="p66334913203046"></a><a name="p66334913203046"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615056_row13311722"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615056_p4507703"><a name="zh-cn_topic_0079615056_p4507703"></a><a name="zh-cn_topic_0079615056_p4507703"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615056_p29579681"><a name="zh-cn_topic_0079615056_p29579681"></a><a name="zh-cn_topic_0079615056_p29579681"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615056_p47143951"><a name="zh-cn_topic_0079615056_p47143951"></a><a name="zh-cn_topic_0079615056_p47143951"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="rf0174cc788d1406791ebac9b6df8acd6"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="a9c85576f378c4573b485d43745475398"><a name="a9c85576f378c4573b485d43745475398"></a><a name="a9c85576f378c4573b485d43745475398"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615056_p777074816124"><a name="zh-cn_topic_0079615056_p777074816124"></a><a name="zh-cn_topic_0079615056_p777074816124"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.4.1.3 "><p id="a1843ce09947646f88cd95ea3763333df"><a name="a1843ce09947646f88cd95ea3763333df"></a><a name="a1843ce09947646f88cd95ea3763333df"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="rb1ed5b6bf60f472cb3ebfd7cf2da6608"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="a39b66f9d415342329a82762fdbf8b74f"><a name="a39b66f9d415342329a82762fdbf8b74f"></a><a name="a39b66f9d415342329a82762fdbf8b74f"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.2 "><p id="aa77cf8a04e5241ce98460b55c28a32c4"><a name="aa77cf8a04e5241ce98460b55c28a32c4"></a><a name="aa77cf8a04e5241ce98460b55c28a32c4"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.4.1.3 "><p id="aac08fb72b4494c9fab0ef0063ef57cd4"><a name="aac08fb72b4494c9fab0ef0063ef57cd4"></a><a name="aac08fb72b4494c9fab0ef0063ef57cd4"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="read1142efb9a4dfc9b8b9a886405f90f"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615056_p549795241210"><a name="zh-cn_topic_0079615056_p549795241210"></a><a name="zh-cn_topic_0079615056_p549795241210"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="22%" headers="mcps1.2.4.1.2 "><p id="a1a32896b6e3f4d75855c467213f67b58"><a name="a1a32896b6e3f4d75855c467213f67b58"></a><a name="a1a32896b6e3f4d75855c467213f67b58"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="45%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615056_p174970527122"><a name="zh-cn_topic_0079615056_p174970527122"></a><a name="zh-cn_topic_0079615056_p174970527122"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s60dd10d6b3e449f19dba8169c1fe4661"></a>

**请求参数：**

请求参数如[表64](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

```
{
    "kind": "DeleteOptions",
    "apiVersion": "v1",
    "gracePeriodSeconds": 10
}
```

## 响应消息<a name="s3687f13ac2bf4e5494185bac214448ff"></a>

**响应参数：**

响应参数的详细描述请参见[表72](数据结构.md#table37251757105918)。

**响应示例：**

```
{
    "kind": "PodList",
    "apiVersion": "v1",
    "metadata": {
        "selfLink": "/api/v1/namespaces/namespace-test/pods",
        "resourceVersion": "5035636"
    },
    "items": [
        {
            "metadata": {
                "name": "pod-test",
                "namespace": "namespace-test",
                "selfLink": "/api/v1/namespaces/namespace-test/pods/pod-test",
                "uid": "8b985a27-af74-11e8-9d5d-c88d83be759f",
                "resourceVersion": "5030610",
                "creationTimestamp": "2018-09-03T12:26:12Z",
                "labels": {
                    "name": "pod-test"
                },
                "annotations": {
                    "network.alpha.kubernetes.io/network": "[{\"name\":\"namespace-test-dc1-default-network\",\"interface\":\"eth0\",\"network_plane\":\"default\"}]",
                    "cri.cci.io/container-type": "secure-container",
                    "kubernetes.io/availablezone": "dc1"
                },
                "enable": true
            },
            "spec": {
                "containers": [
                    {
                        "name": "test",
                        "image": "redis",
                        "resources": {
                            "limits": {
                                "cpu": "500m",
                                "memory": "1Gi"
                            },
                            "requests": {
                                "cpu": "500m",
                                "memory": "1Gi"
                            }
                        },
                        "terminationMessagePath": "/dev/termination-log",
                        "terminationMessagePolicy": "File",
                        "imagePullPolicy": "Always"
                    }
                ],
                "restartPolicy": "Always",
                "terminationGracePeriodSeconds": 30,
                "dnsPolicy": "ClusterFirst",
                "nodeName": "c0dd6256-195a-e811-90a2-10c17294fcbc",
                "securityContext": {},
                "imagePullSecrets": [
                    {
                        "name": "imagepull-secret"
                    }
                ],
                "schedulerName": "default-scheduler",
                "tolerations": [
                    {
                        "key": "node.kubernetes.io/not-ready",
                        "operator": "Exists",
                        "effect": "NoExecute",
                        "tolerationSeconds": 300
                    },
                    {
                        "key": "node.kubernetes.io/unreachable",
                        "operator": "Exists",
                        "effect": "NoExecute",
                        "tolerationSeconds": 300
                    }
                ]
            },
            "status": {
                "phase": "Running",
                "conditions": [
                    {
                        "type": "Initialized",
                        "status": "True",
                        "lastProbeTime": null,
                        "lastTransitionTime": "2018-09-03T12:26:12Z"
                    },
                    {
                        "type": "Ready",
                        "status": "True",
                        "lastProbeTime": null,
                        "lastTransitionTime": "2018-09-03T12:26:16Z"
                    },
                    {
                        "type": "PodScheduled",
                        "status": "True",
                        "lastProbeTime": null,
                        "lastTransitionTime": "2018-09-03T12:26:12Z"
                    }
                ],
                "podIP": "192.168.245.185",
                "startTime": "2018-09-03T12:26:12Z",
                "containerStatuses": [
                    {
                        "name": "test",
                        "state": {
                            "running": {
                                "startedAt": "2018-09-03T12:26:16Z"
                            }
                        },
                        "lastState": {},
                        "ready": true,
                        "restartCount": 0,
                        "image": "redis",
                        "imageID": "docker-pullable://redis@sha256:3ab7046bd035a47aa06963d8240651d00b57e82dab07ba374ad01f84dfa1230c",
                        "containerID": "docker://aee55d8dedb8371f96aa5d5116f69a53bf1cb23afe1802567c24081514d3b048"
                    }
                ],
                "qosClass": "Guaranteed",
                "managementIP": "172.28.0.17"
            }
        }
    ]
}
```

## 状态码<a name="sb708a925922c4906ac99d1ac2c6751e5"></a>

[表3](#zh-cn_topic_0079615056_table50951864)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615056_table50951864"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615056_row65026214"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p41872640203046"><a name="p41872640203046"></a><a name="p41872640203046"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p36240679203046"><a name="p36240679203046"></a><a name="p36240679203046"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615056_row21145452"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615056_p35060088"><a name="zh-cn_topic_0079615056_p35060088"></a><a name="zh-cn_topic_0079615056_p35060088"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615056_p179841688599"><a name="zh-cn_topic_0079615056_p179841688599"></a><a name="zh-cn_topic_0079615056_p179841688599"></a>Delete a Pod resource objectre successfully.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

