# 创建Deployment<a name="cci_02_3018"></a>

## 功能介绍<a name="section15904123713483"></a>

创建一个Deployment。

创建Deployment时挂载OBS的使用限制请参见[挂载OBS使用限制](挂载OBS使用限制.md)。

## URI<a name="section764545414815"></a>

POST /apis/apps/v1/namespaces/\{namespace\}/deployments

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

<a name="zh-cn_topic_0079615001_table32114614"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615001_row42303331"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615001_p4017754"><a name="zh-cn_topic_0079615001_p4017754"></a><a name="zh-cn_topic_0079615001_p4017754"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.2"><p id="p27173000203043"><a name="p27173000203043"></a><a name="p27173000203043"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.3"><p id="p53529377203043"><a name="p53529377203043"></a><a name="p53529377203043"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615001_row29042598"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615001_p3640263"><a name="zh-cn_topic_0079615001_p3640263"></a><a name="zh-cn_topic_0079615001_p3640263"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615001_p26425925"><a name="zh-cn_topic_0079615001_p26425925"></a><a name="zh-cn_topic_0079615001_p26425925"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0079615001_p60125191"><a name="zh-cn_topic_0079615001_p60125191"></a><a name="zh-cn_topic_0079615001_p60125191"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section24905416619"></a>

**请求参数**：

请求参数如[表79](数据结构.md#table12862324102610)所示。

**请求示例：**

```
{
    "apiVersion": "apps/v1",
    "kind": "Deployment",
    "metadata": {
        "name": "deployment-test"
    },
    "spec": {
        "replicas": 1,
        "selector": {
            "matchLabels": {
                "app": "redis"
            }
        },
        "template": {
            "metadata": {
                "labels": {
                    "app": "redis"
                }
            },
            "spec": {
                "containers": [
                    {
                        "image": "redis",
                        "name": "container-0",
                        "resources": {
                            "limits": {
                                "cpu": "500m",
                                "memory": "1024Mi"
                            },
                            "requests": {
                                "cpu": "500m",
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
               "priority": 0
            }
        }
    }
}
```

## 响应消息<a name="section1575712476123"></a>

**响应参数**：

响应参数如[表79](数据结构.md#table12862324102610)所示。

**响应示例：**

```
{
    "kind": "Deployment",
    "apiVersion": "apps/v1",
    "metadata": {
        "name": "deployment-test",
        "namespace": "namespace-test",
        "selfLink": "/apis/apps/v1/namespaces/namespace-test/deployments/deployment-test",
        "uid": "777dce52-b186-11e8-8cb0-c81fbe371a17",
        "resourceVersion": "5630832",
        "generation": 1,
        "creationTimestamp": "2018-09-06T03:39:32Z",
        "labels": {
            "app": "redis"
        },
        "enable": true
    },
    "spec": {
        "replicas": 1,
        "priority": 0,
        "selector": {
            "matchLabels": {
                "app": "redis"
            }
        },
        "template": {
            "metadata": {
                "creationTimestamp": null,
                "labels": {
                    "app": "redis"
                },
                "annotations": {
                    "cri.cci.io/container-type": "secure-container"
                },
                "enable": true
            },
            "spec": {
                "containers": [
                    {
                        "name": "container-0",
                        "image": "redis",
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
                        "imagePullPolicy": "IfNotPresent"
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
                "schedulerName": "default-scheduler"
            }
        },
        "strategy": {
            "type": "RollingUpdate",
            "rollingUpdate": {
                "maxUnavailable": "25%",
                "maxSurge": "25%"
            }
        },
        "revisionHistoryLimit": 10,
        "progressDeadlineSeconds": 600
    },
    "status": {}
}
```

## 状态码<a name="section16509142112516"></a>

[表3 状态码](#table6957182913514)描述API的状态码。

**表 3**  状态码

<a name="table6957182913514"></a>
<table><thead align="left"><tr id="row12961162965119"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p189627299518"><a name="p189627299518"></a><a name="p189627299518"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p1596342917515"><a name="p1596342917515"></a><a name="p1596342917515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row15964122975119"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p09651299518"><a name="p09651299518"></a><a name="p09651299518"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p18966142915518"><a name="p18966142915518"></a><a name="p18966142915518"></a>This operation succeeds, and a Deployment resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

