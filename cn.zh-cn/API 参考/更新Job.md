# 更新Job<a name="cci_02_3038"></a>

## 功能介绍<a name="section44235199"></a>

更新Job。

The following fields can be updated:

-   metadata.labels
-   spec.parallelism
-   spec.completions
-   spec.selector

## URI<a name="section62572474"></a>

PATCH /apis/batch/v1/namespaces/\{namespace\}/jobs/\{name\}

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

<a name="d0e42697"></a>
<table><thead align="left"><tr id="row25506777"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.169999999999998%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.61%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row43424386"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p27714369"><a name="p27714369"></a><a name="p27714369"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p30271441"><a name="p30271441"></a><a name="p30271441"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p36067674"><a name="p36067674"></a><a name="p36067674"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section26281361"></a>

**请求参数：**

“Content-Type“消息头说明请参见[PATCH请求方法操作说明](PATCH请求方法操作说明.md)。

**请求示例：**

为[创建Job](创建Job.md)创建的Job添加一个label。

```
Content-Type: application/merge-patch+json
```

```
{
    "metadata": {
        "labels": {
            "app": "test"
        }
    }
}
```

## 响应消息<a name="section35205659"></a>

**响应参数：**

响应参数的详细描述请参见[表97](数据结构.md#table8040885)。

**响应示例：**

```
{
    "kind": "Job",
    "apiVersion": "batch/v1",
    "metadata": {
        "name": "pi",
        "namespace": "namespace-test",
        "selfLink": "/apis/batch/v1/namespaces/namespace-test/jobs/pi",
        "uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
        "resourceVersion": "5398083",
        "creationTimestamp": "2018-09-05T01:10:59Z",
        "labels": {
            "app": "test",
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
                    "controller-uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
                    "job-name": "pi"
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
                "dnsPolicy": "ClusterFirst",
                "securityContext": {},
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

## 状态码<a name="section48415483"></a>

[表3](#d0e42791)描述API的状态码。

**表 3**  状态码

<a name="d0e42791"></a>
<table><thead align="left"><tr id="row7304508"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p54794282"><a name="p54794282"></a><a name="p54794282"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p9151897"><a name="p9151897"></a><a name="p9151897"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row3106225"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p50277657"><a name="p50277657"></a><a name="p50277657"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p45958393"><a name="p45958393"></a><a name="p45958393"></a>This operation succeeds, and a Job resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

