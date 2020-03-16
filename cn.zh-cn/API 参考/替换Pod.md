# 替换Pod<a name="cci_02_3010"></a>

## 功能介绍<a name="seb80de7886d64c79adcdf04cb6b8d3c6"></a>

替换指定Pod。

其中以下字段支持更新：

-   metadata.labels
-   metadata.annotations
-   spec.initContainers\[\*\].image
-   spec.containers\[\*\].image
-   spec.activeDeadlineSeconds
-   spec.tolerations.tolerationSeconds

其余部分不支持更新。

## URI<a name="scc13338839174f99b35830d9cbad55b0"></a>

PUT /api/v1/namespaces/\{namespace\}/pods/\{name\}

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
<tr id="row115455519446"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p15341161164510"><a name="p15341161164510"></a><a name="p15341161164510"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p1234131114458"><a name="p1234131114458"></a><a name="p1234131114458"></a>Name of the Pod.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="zh-cn_topic_0079614904_table61950116"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614904_row42466880"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079614904_p17265247"><a name="zh-cn_topic_0079614904_p17265247"></a><a name="zh-cn_topic_0079614904_p17265247"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.303030303030305%" id="mcps1.2.4.1.2"><p id="p25470926205834"><a name="p25470926205834"></a><a name="p25470926205834"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.2.4.1.3"><p id="p49879135205834"><a name="p49879135205834"></a><a name="p49879135205834"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614904_row1125057"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079614904_p24020754"><a name="zh-cn_topic_0079614904_p24020754"></a><a name="zh-cn_topic_0079614904_p24020754"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079614904_p66632916"><a name="zh-cn_topic_0079614904_p66632916"></a><a name="zh-cn_topic_0079614904_p66632916"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079614904_p28557102"><a name="zh-cn_topic_0079614904_p28557102"></a><a name="zh-cn_topic_0079614904_p28557102"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0079614899_ref458607622"></a>

**请求参数：**

请求参数的详细描述请参见[表2](数据结构.md#zh-cn_topic_0079614925_table60388168)。

**请求示例：**

将[创建Pod](创建Pod.md)创建的Pod镜像替换为“redis:latest"。

```
{
    "apiVersion": "v1",
    "kind": "Pod",
    "metadata": {
        "labels": {
            "name": "pod-test"
        },
        "name": "pod-test"
    },
    "spec": {
        "containers": [
            {
                "image": "redis:latest",
                "imagePullPolicy": "Always",
                "name": "test",
                "resources": {
                    "requests": {
                        "cpu": "0.5",
                        "memory": "1024Mi"
                    },
                    "limits": {
                        "cpu": "0.5",
                        "memory": "1024Mi"
                    }
                }
            }
        ],
        "imagePullSecrets": [
            {
                "name": "imagepull-secret"
            }
        ],
        "restartPolicy": "Always"
    }
}
```

## 响应消息<a name="sf7ea4cdd65584034bfd0c2083e4191b7"></a>

**响应参数：**

响应参数的详细描述请参见[表2](数据结构.md#zh-cn_topic_0079614925_table60388168)。

**响应示例：**

```
{
    "kind": "Pod",
    "apiVersion": "v1",
    "metadata": {
        "name": "pod-test",
        "namespace": "namespace-test",
        "selfLink": "/api/v1/namespaces/namespace-test/pods/pod-test",
        "uid": "3b99abe8-b032-11e8-9d5d-c88d83be759f",
        "resourceVersion": "5253248",
        "creationTimestamp": "2018-09-04T11:04:02Z",
        "labels": {
            "name": "pod-test"
        },
        "enable": true
    },
    "spec": {
        "containers": [
            {
                "name": "test",
                "image": "redis:latest",
                "resources": {
                    "limits": {
                        "cpu": "500m",
                        "memory": "1Gi"
                    },
                    "requests": {
                        "memory": "1Gi",
                        "cpu": "500m"
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
                "lastTransitionTime": "2018-09-04T11:04:03Z"
            },
            {
                "type": "Ready",
                "status": "True",
                "lastProbeTime": null,
                "lastTransitionTime": "2018-09-04T11:04:36Z"
            },
            {
                "type": "PodScheduled",
                "status": "True",
                "lastProbeTime": null,
                "lastTransitionTime": "2018-09-04T11:04:02Z"
            }
        ],
        "hostIP": "192.149.117.100",
        "podIP": "192.168.244.170",
        "startTime": "2018-09-04T11:04:03Z",
        "containerStatuses": [
            {
                "name": "test",
                "state": {
                    "running": {
                        "startedAt": "2018-09-04T11:04:23Z"
                    }
                },
                "lastState": {},
                "ready": true,
                "restartCount": 0,
                "image": "redis",
                "imageID": "docker-pullable://redis@sha256:3ab7046bd035a47aa06963d8240651d00b57e82dab07ba374ad01f84dfa1230c",
                "containerID": "docker://f867ab7d5c68a86fc695e4d3e5f1912fdb8f98f5029ca96032b4d5d407d9a75c"
            }
        ],
        "qosClass": "Guaranteed",
        "managementIP": "172.28.0.17"
    }
}
```

## 状态码<a name="scbd2111a9d7b41b58b8af7b555c8bb78"></a>

[表3](#zh-cn_topic_0079614899_table16427006)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079614899_table16427006"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079614899_row51117746"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p49567918201516"><a name="p49567918201516"></a><a name="p49567918201516"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p55578412201516"><a name="p55578412201516"></a><a name="p55578412201516"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079614899_row62776692"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079614899_p51747272"><a name="zh-cn_topic_0079614899_p51747272"></a><a name="zh-cn_topic_0079614899_p51747272"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079614899_p30779497"><a name="zh-cn_topic_0079614899_p30779497"></a><a name="zh-cn_topic_0079614899_p30779497"></a>This operation succeeds, and the JSON of a Pod object is returned.</p>
</td>
</tr>
</tbody>
</table>

