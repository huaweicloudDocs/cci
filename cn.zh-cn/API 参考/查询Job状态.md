# 查询Job状态<a name="cci_02_3044"></a>

## 功能介绍<a name="section872215"></a>

查询Job状态。

## URI<a name="section7849943"></a>

GET /apis/batch/v1/namespaces/\{namespace\}/jobs/\{name\}/status

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
<td class="cellrowborder" valign="top" width="76%" headers="mcps1.2.3.1.2 "><p id="p4984175851116"><a name="p4984175851116"></a><a name="p4984175851116"></a>Name of the Job.</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="d0e41637"></a>
<table><thead align="left"><tr id="row38510554"><th class="cellrowborder" valign="top" width="33.33333333333333%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.303030303030305%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row52377634"><td class="cellrowborder" valign="top" width="33.33333333333333%" headers="mcps1.2.4.1.1 "><p id="p14729974"><a name="p14729974"></a><a name="p14729974"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="30.303030303030305%" headers="mcps1.2.4.1.2 "><p id="p52277209"><a name="p52277209"></a><a name="p52277209"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.2.4.1.3 "><p id="p6595574"><a name="p6595574"></a><a name="p6595574"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section3540627"></a>

N/A

## 响应消息<a name="section31865643"></a>

**响应参数：**

响应参数的详细描述请参见[表98](公共参数.md#table8040885)。

**响应示例：**

```
{
  "kind": "Job",
  "apiVersion": "batch/v1",
  "metadata": {
    "name": "pi",
    "namespace": "namespace-test",
    "selfLink": "/apis/batch/v1/namespaces/namespace-test/jobs/pi/status",
    "uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
    "resourceVersion": "5391205",
    "creationTimestamp": "2018-09-05T01:10:59Z",
    "labels": {
      "controller-uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
      "job-name": "pi"
    },
    "enable": true
  },
  "spec": {
    "parallelism": 1,
    "completions": 1,
    "backoffLimit": 6,
    "selector": {
      "matchLabels": {
        "controller-uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4"
      }
    },
    "template": {
      "metadata": {
        "name": "pi",
        "creationTimestamp": null,
        "labels": {
          "job-name": "pi",
          "controller-uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4"
        },
        "annotations": {
          "cri.cci.io/container-type": "secure-container"
        },
        "enable": true
      },
      "spec": {
        "containers": [
          {
            "name": "pi",
            "image": "perl",
            "command": [
              "perl",
              "-Mbignum=bpi",
              "-wle",
              "print bpi(2000)"
            ],
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
        "restartPolicy": "Never",
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
    }
  },
  "status": {
    "startTime": "2018-09-05T01:10:59Z",
    "active": 1
  }
}
```

## 状态码<a name="section18355338"></a>

[表3](#d0e41716)描述API的状态码。

**表 3**  状态码

<a name="d0e41716"></a>
<table><thead align="left"><tr id="row49104241"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p18020555"><a name="p18020555"></a><a name="p18020555"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p50378833"><a name="p50378833"></a><a name="p50378833"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row54153709"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p24374276"><a name="p24374276"></a><a name="p24374276"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p28159360"><a name="p28159360"></a><a name="p28159360"></a>This operation succeeds, and a Job resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

