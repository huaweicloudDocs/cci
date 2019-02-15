# 创建Pod<a name="cci_02_3006"></a>

## 功能介绍<a name="scc86678262934086bfbe32385da35788"></a>

创建一个Pod。

>![](public_sys-resources/icon-note.gif) **说明：**   
>Pod的生命周期是短暂的，Pod是用后即焚的实体。在实际使用中，请谨慎单独创建Pod，请使用Deployment、StatefulSet和Job这些控制器创建应用，从而保障应用高可用。  

您可以选择使用GPU（只能在GPU型命名空间下）或不使用GPU。

当前提供Nvidia Telsla V100 16G显卡（显卡驱动版本: 396.26 | CUDA驱动版本: 9.2），使用GPU时容器规格有如下几种：

-   Nvidia Telsla V100 16G x 1，CPU 4核，内存32GB
-   Nvidia Telsla V100 16G x 2，CPU 8核，内存64GB
-   Nvidia Telsla V100 16G x 4，CPU 16核，内存128GB
-   Nvidia Telsla V100 16G x 8，CPU 32核，内存256GB

不使用GPU时容器规格有如下几种：

-   Pod的CPU取值范围为0.25核-32核，且单个容器的CPU必须为0.25核的整数倍
-   Pod的内存取值范围为1GB-128GB，且内存必须为1GB的整数倍
-   Pod的CPU/内存配比值必须在1:2到1:4之间
-   一个Pod内最多支持5个容器，单个容器最小配置是0.25核、0.2GB，最大同容器实例的最大配置

## URI<a name="s83bc1fb06185462cb2e2665b169bc85c"></a>

POST /api/v1/namespaces/\{namespace\}/pods

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

**表 2**  参数描述

<a name="zh-cn_topic_0079615001_table32114614"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615001_row42303331"><th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0079615001_p4017754"><a name="zh-cn_topic_0079615001_p4017754"></a><a name="zh-cn_topic_0079615001_p4017754"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="11%" id="mcps1.2.4.1.2"><p id="p27173000203043"><a name="p27173000203043"></a><a name="p27173000203043"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="75%" id="mcps1.2.4.1.3"><p id="p53529377203043"><a name="p53529377203043"></a><a name="p53529377203043"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615001_row29042598"><td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0079615001_p3640263"><a name="zh-cn_topic_0079615001_p3640263"></a><a name="zh-cn_topic_0079615001_p3640263"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="11%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0079615001_p26425925"><a name="zh-cn_topic_0079615001_p26425925"></a><a name="zh-cn_topic_0079615001_p26425925"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="75%" headers="mcps1.2.4.1.3 "><p id="p555410261514"><a name="p555410261514"></a><a name="p555410261514"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="zh-cn_topic_0079615001_d0e16631"></a>

**请求参数：**

请求参数的详细描述请参见[表2](公共参数.md#zh-cn_topic_0079614925_table60388168)。

**请求示例：**

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
                "image": "redis:3.0",
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

创建GPUpod示例：

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
                "image": "redis:3.0",
                "imagePullPolicy": "Always",
                "name": "test",
                "resources": {
                    "requests": {
                        "cpu": "4",
                        "memory": "32Gi", 
                        "nvidia.com/gpu-tesla-v100-16GB": "1"
                    },
                    "limits": {
                        "cpu": "4",
                        "memory": "32Gi"
                        "nvidia.com/gpu-tesla-v100-16GB": "1"
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

## 响应消息<a name="s23649bc4d7154135b7153a5743022fcd"></a>

**响应参数：**

响应参数的详细描述请参见[表2](公共参数.md#zh-cn_topic_0079614925_table60388168)。

**响应示例：**

```
{
  "kind": "Pod",
  "apiVersion": "v1",
  "metadata": {
    "name": "pod-test",
    "namespace": "namespace-test",
    "selfLink": "/api/v1/namespaces/namespace-test/pods/pod-test",
    "uid": "8b985a27-af74-11e8-9d5d-c88d83be759f",
    "resourceVersion": "5030599",
    "creationTimestamp": "2018-09-03T12:26:12Z",
    "labels": {
      "name": "pod-test"
    },
    "annotations": {
      "cri.cci.io/container-type": "secure-container"
    },
    "enable": true
  },
  "spec": {
    "containers": [
      {
        "name": "test",
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
        "imagePullPolicy": "Always"
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
    "phase": "Pending",
    "qosClass": "Guaranteed"
  }
}
```

## 状态码<a name="sbb2d9f14fc4a4197a3a609e7c568ab4d"></a>

[表3](#zh-cn_topic_0079615001_table20596071)描述API的状态码。

**表 3**  状态码

<a name="zh-cn_topic_0079615001_table20596071"></a>
<table><thead align="left"><tr id="zh-cn_topic_0079615001_row9746163"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p57545694203043"><a name="p57545694203043"></a><a name="p57545694203043"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p30689603203043"><a name="p30689603203043"></a><a name="p30689603203043"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0079615001_row48621261"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="zh-cn_topic_0079615001_p46008046"><a name="zh-cn_topic_0079615001_p46008046"></a><a name="zh-cn_topic_0079615001_p46008046"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="zh-cn_topic_0079615001_p35664277"><a name="zh-cn_topic_0079615001_p35664277"></a><a name="zh-cn_topic_0079615001_p35664277"></a>This operation succeeds, and a Pod resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

