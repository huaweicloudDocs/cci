# 创建Job<a name="cci_02_3037"></a>

## 功能介绍<a name="section5825523"></a>

创建Job。

创建Job时挂载OBS的使用限制请参见[挂载OBS使用限制](挂载OBS使用限制.md)。

## URI<a name="section52429714"></a>

POST /apis/batch/v1/namespaces/\{namespace\}/jobs

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

<a name="table65625523"></a>
<table><thead align="left"><tr id="row19842874"><th class="cellrowborder" valign="top" width="22.220000000000002%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.169999999999998%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.61%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row8248038"><td class="cellrowborder" valign="top" width="22.220000000000002%" headers="mcps1.2.4.1.1 "><p id="p64111314"><a name="p64111314"></a><a name="p64111314"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.169999999999998%" headers="mcps1.2.4.1.2 "><p id="p25633971"><a name="p25633971"></a><a name="p25633971"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.61%" headers="mcps1.2.4.1.3 "><p id="p63085809"><a name="p63085809"></a><a name="p63085809"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section2105383"></a>

**请求参数：**

请求参数如[表97](数据结构.md#table8040885)所示。

**请求示例：**

```
{
    "apiVersion": "batch/v1",
    "kind": "Job",
    "metadata": {
        "name": "pi"
    },
    "spec": {
        "template": {
            "metadata": {
                "name": "pi"
            },
            "spec": {
                "containers": [
                    {
                        "name": "pi",
                        "image": "perl",
                        "resources": {
                            "limits": {
                                "cpu": "500m",
                                "memory": "1024Mi"
                            },
                            "requests": {
                                "cpu": "500m",
                                "memory": "1024Mi"
                            }
                        },
                        "command": [
                            "perl",
                            "-Mbignum=bpi",
                            "-wle",
                            "print bpi(2000)"
                        ]
                    }
                ],
                "imagePullSecrets": [
                    {
                        "name": "imagepull-secret"
                    }

                ],
                "restartPolicy": "Never",
                "priority": "0"
            }
        }
    }
}
```

## 响应消息<a name="section18948451"></a>

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
        "resourceVersion": "5391201",
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
                "priority": "0",
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
        }
    },
    "status": {}
}
```

## 状态码<a name="section36318335"></a>

[表3](#table30003806)描述API的状态码。

**表 3**  状态码

<a name="table30003806"></a>
<table><thead align="left"><tr id="row20731931"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p1564889"><a name="p1564889"></a><a name="p1564889"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p59647195"><a name="p59647195"></a><a name="p59647195"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row66693514"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p33465549"><a name="p33465549"></a><a name="p33465549"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p26354957"><a name="p26354957"></a><a name="p26354957"></a>The request has been fulfilled, resulting in the creation of a new resource.</p>
</td>
</tr>
</tbody>
</table>

