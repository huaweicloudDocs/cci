# 替换Deployment<a name="cci_02_3024"></a>

## 功能介绍<a name="section172959268501"></a>

替换Deployment。

其中以下字段支持更新：

-   metadata.labels
-   metadata.generateName
-   metadata.annotations
-   spec.template
-   spec.replicas
-   spec.revisionHistoryLimit
-   spec.progressDeadlineSeconds

## URI<a name="section1524832914503"></a>

PUT /apis/apps/v1/namespaces/\{namespace\}/deployments/\{name\}

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
<tr id="row127506310151"><td class="cellrowborder" valign="top" width="24%" headers="mcps1.2.3.1.1 "><p id="p19499173311150"><a name="p19499173311150"></a><a name="p19499173311150"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p1499123311158"><a name="p1499123311158"></a><a name="p1499123311158"></a>name of the Deployment</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table14970324122818"></a>
<table><thead align="left"><tr id="row0971162417289"><th class="cellrowborder" valign="top" width="33%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079616860_zh-cn_topic_0079614957_p54329699"><a name="zh-cn_topic_0079616860_zh-cn_topic_0079614957_p54329699"></a><a name="zh-cn_topic_0079616860_zh-cn_topic_0079614957_p54329699"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.4.1.2"><p id="p6151164282819"><a name="p6151164282819"></a><a name="p6151164282819"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="56.99999999999999%" id="mcps1.2.4.1.3"><p id="p21518421288"><a name="p21518421288"></a><a name="p21518421288"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row11971122412819"><td class="cellrowborder" valign="top" width="33%" headers="mcps1.2.4.1.1 "><p id="p1597142412282"><a name="p1597142412282"></a><a name="p1597142412282"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.4.1.2 "><p id="p497132410288"><a name="p497132410288"></a><a name="p497132410288"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="56.99999999999999%" headers="mcps1.2.4.1.3 "><p id="p1597132420289"><a name="p1597132420289"></a><a name="p1597132420289"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section1244125315509"></a>

**请求参数：**

请求参数的详细描述请参见[表80](数据结构.md#table12862324102610)。

**请求示例：**

将[创建Deployment](创建Deployment.md)创建的Deployment的replica替换为2。

```
{
    "apiVersion": "apps/v1",
    "kind": "Deployment",
    "metadata": {
        "name": "deployment-test"
    },
    "spec": {
        "replicas": 2,
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
                        "image": "100.125.5.235:20202/cci_z00425431/redis:V1",
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
                ]
            }
        }
    }
}
```

## 响应消息<a name="section59181834162920"></a>

**响应参数：**

响应参数的详细描述请参见[表80](数据结构.md#table12862324102610)。

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
    "resourceVersion": "5636210",
    "generation": 2,
    "creationTimestamp": "2018-09-06T03:39:32Z",
    "labels": {
      "app": "redis"
    },
    "enable": true
  },
  "spec": {
    "replicas": 2,
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
        "enable": true
      },
      "spec": {
        "containers": [
          {
            "name": "container-0",
            "image": "redis:3.0",
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
            "imagePullPolicy": "IfNotPresent"
          }
        ],
        "restartPolicy": "Always",
        "terminationGracePeriodSeconds": 30,
        "dnsPolicy": "ClusterFirst",
        "securityContext": {

        },
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
  "status": {
    "observedGeneration": 1,
    "replicas": 1,
    "updatedReplicas": 1,
    "readyReplicas": 1,
    "availableReplicas": 1,
    "conditions": [
      {
        "type": "Available",
        "status": "True",
        "lastUpdateTime": "2018-09-06T03:39:40Z",
        "lastTransitionTime": "2018-09-06T03:39:40Z",
        "reason": "MinimumReplicasAvailable",
        "message": "Deployment has minimum availability."
      },
      {
        "type": "Progressing",
        "status": "True",
        "lastUpdateTime": "2018-09-06T03:39:40Z",
        "lastTransitionTime": "2018-09-06T03:39:32Z",
        "reason": "NewReplicaSetAvailable",
        "message": "ReplicaSet \"deployment-test-865578b586\" has successfully progressed."
      }
    ]
  }
}
```

## 状态码<a name="section18404183601410"></a>

**表 3**  状态码

<a name="table9436536131414"></a>
<table><thead align="left"><tr id="row2436113641415"><th class="cellrowborder" valign="top" width="47%" id="mcps1.2.3.1.1"><p id="p18436193610144"><a name="p18436193610144"></a><a name="p18436193610144"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="53%" id="mcps1.2.3.1.2"><p id="p18436936101411"><a name="p18436936101411"></a><a name="p18436936101411"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row94361036151419"><td class="cellrowborder" valign="top" width="47%" headers="mcps1.2.3.1.1 "><p id="p44361236161419"><a name="p44361236161419"></a><a name="p44361236161419"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="53%" headers="mcps1.2.3.1.2 "><p id="p343618369141"><a name="p343618369141"></a><a name="p343618369141"></a>This operation succeeds, and a  Development resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

