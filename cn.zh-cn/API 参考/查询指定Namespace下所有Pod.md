# 查询指定Namespace下所有Pod<a name="cci_02_3012"></a>

## 功能介绍<a name="sa15e1880c5594fc48219b954fe0ba73f"></a>

查询所有Pod的详细信息。

## URI<a name="s2816ee648d7a424dadd23e140e22ab10"></a>

GET /api/v1/namespaces/\{namespace\}/pods

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
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079615024_table39288210"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615024_row57365620"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615024_p16103609"><a name="zh-cn_topic_0079615024_p16103609"></a><a name="zh-cn_topic_0079615024_p16103609"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.34%" id="mcps1.2.4.1.2"><p id="p2877885220168"><a name="p2877885220168"></a><a name="p2877885220168"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="48.66%" id="mcps1.2.4.1.3"><p id="p4938564320168"><a name="p4938564320168"></a><a name="p4938564320168"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615024_row60306259"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615024_p52968826"><a name="zh-cn_topic_0079615024_p52968826"></a><a name="zh-cn_topic_0079615024_p52968826"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="18.34%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615024_p62616542"><a name="zh-cn_topic_0079615024_p62616542"></a><a name="zh-cn_topic_0079615024_p62616542"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="48.66%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615024_p38775142"><a name="zh-cn_topic_0079615024_p38775142"></a><a name="zh-cn_topic_0079615024_p38775142"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079615024_row13431963"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615024_p14247253"><a name="zh-cn_topic_0079615024_p14247253"></a><a name="zh-cn_topic_0079615024_p14247253"></a>labelSelector</p>
</td>
<td class="cellrowborder" valign="top" width="18.34%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615024_p13176872"><a name="zh-cn_topic_0079615024_p13176872"></a><a name="zh-cn_topic_0079615024_p13176872"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="48.66%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615024_p60693691"><a name="zh-cn_topic_0079615024_p60693691"></a><a name="zh-cn_topic_0079615024_p60693691"></a>A selector to restrict the list of returned objects by their labels. Defaults to everything.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079615024_row9372308"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615024_p20959466"><a name="zh-cn_topic_0079615024_p20959466"></a><a name="zh-cn_topic_0079615024_p20959466"></a>fieldSelector</p>
</td>
<td class="cellrowborder" valign="top" width="18.34%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615024_p19995222"><a name="zh-cn_topic_0079615024_p19995222"></a><a name="zh-cn_topic_0079615024_p19995222"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="48.66%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615024_p9000253"><a name="zh-cn_topic_0079615024_p9000253"></a><a name="zh-cn_topic_0079615024_p9000253"></a>A selector to restrict the list of returned objects by their fields. Defaults to everything.</p>
</td>
</tr>
<tr id="r48a23247a4514d3895552219d0bf1d7f"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615024_p268425212266"><a name="zh-cn_topic_0079615024_p268425212266"></a><a name="zh-cn_topic_0079615024_p268425212266"></a>includeUninitialized</p>
</td>
<td class="cellrowborder" valign="top" width="18.34%" headers="mcps1.2.4.1.2 "><p id="ab0682c66f2294f69bb2a7d10b9e29068"><a name="ab0682c66f2294f69bb2a7d10b9e29068"></a><a name="ab0682c66f2294f69bb2a7d10b9e29068"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="48.66%" headers="mcps1.2.4.1.3 "><p id="a101aec385acb47ff8569f2105ffa4e76"><a name="a101aec385acb47ff8569f2105ffa4e76"></a><a name="a101aec385acb47ff8569f2105ffa4e76"></a>If true, partially initialized resources are included in the response.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079615024_row13893419"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615024_p51625177"><a name="zh-cn_topic_0079615024_p51625177"></a><a name="zh-cn_topic_0079615024_p51625177"></a>watch</p>
</td>
<td class="cellrowborder" valign="top" width="18.34%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615024_p20889783"><a name="zh-cn_topic_0079615024_p20889783"></a><a name="zh-cn_topic_0079615024_p20889783"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="48.66%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615024_p14350829"><a name="zh-cn_topic_0079615024_p14350829"></a><a name="zh-cn_topic_0079615024_p14350829"></a>Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079615024_row62048601"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615024_p59880775"><a name="zh-cn_topic_0079615024_p59880775"></a><a name="zh-cn_topic_0079615024_p59880775"></a>resourceVersion</p>
</td>
<td class="cellrowborder" valign="top" width="18.34%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615024_p18504610"><a name="zh-cn_topic_0079615024_p18504610"></a><a name="zh-cn_topic_0079615024_p18504610"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="48.66%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615024_p22478417"><a name="zh-cn_topic_0079615024_p22478417"></a><a name="zh-cn_topic_0079615024_p22478417"></a>When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history.</p>
</td>
</tr>
<tr id="zh-cn_topic_0079615024_row979164"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615024_p12203429"><a name="zh-cn_topic_0079615024_p12203429"></a><a name="zh-cn_topic_0079615024_p12203429"></a>timeoutSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="18.34%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615024_p48953654"><a name="zh-cn_topic_0079615024_p48953654"></a><a name="zh-cn_topic_0079615024_p48953654"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="48.66%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615024_p5823032"><a name="zh-cn_topic_0079615024_p5823032"></a><a name="zh-cn_topic_0079615024_p5823032"></a>Timeout for the list/watch call.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="s417ddc31a4054521aee75e523ec75dc7"></a>

N/A

## 响应消息<a name="sf3b21eb28dd042b6860622b69c5fcf92"></a>

**响应参数：**

响应参数的详细描述请参见[表67](数据结构.md#zh-cn_topic_0079614930_table6622802)。

**响应示例：**

```
{
    "kind": "PodList",
    "apiVersion": "v1",
    "metadata": {
        "selfLink": "/api/v1/namespaces/namespace-test/pods",
        "resourceVersion": "5032373"
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
                    "cri.cci.io/container-type": "secure-container",
                    "kubernetes.io/availablezone": "dc1",
                    "network.alpha.kubernetes.io/network": "[{\"name\":\"namespace-test-dc1-default-network\",\"interface\":\"eth0\",\"network_plane\":\"default\"}]"
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
                                "memory": "1Gi",
                                "cpu": "500m"
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

## 状态码<a name="sbc30358c7d094cf7b28929f12a616f3c"></a>

[表3](#zh-cn_topic_0079615024_table18049573)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615024_table18049573"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615024_row33487713"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p3844484120168"><a name="p3844484120168"></a><a name="p3844484120168"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p2702441120168"><a name="p2702441120168"></a><a name="p2702441120168"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615024_row10105911"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615024_p13272423"><a name="zh-cn_topic_0079615024_p13272423"></a><a name="zh-cn_topic_0079615024_p13272423"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615024_p1324451"><a name="zh-cn_topic_0079615024_p1324451"></a><a name="zh-cn_topic_0079615024_p1324451"></a>This operation succeeds, and a group of Pod resource objects is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

