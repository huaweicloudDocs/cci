# 查询Job<a name="cci_02_3042"></a>

## 功能介绍<a name="section34495516"></a>

查询Job的详细信息。

## URI<a name="section42024188"></a>

GET /apis/batch/v1/namespaces/\{namespace\}/jobs/\{name\}

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

<a name="d0e41471"></a>
<table><thead align="left"><tr id="row14497772"><th class="cellrowborder" valign="top" width="24.192419241924192%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.371937193719376%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="56.43564356435644%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row66636327"><td class="cellrowborder" valign="top" width="24.192419241924192%" headers="mcps1.2.4.1.1 "><p id="p28833370"><a name="p28833370"></a><a name="p28833370"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="19.371937193719376%" headers="mcps1.2.4.1.2 "><p id="p53801671"><a name="p53801671"></a><a name="p53801671"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="56.43564356435644%" headers="mcps1.2.4.1.3 "><p id="p62968084"><a name="p62968084"></a><a name="p62968084"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row50603201"><td class="cellrowborder" valign="top" width="24.192419241924192%" headers="mcps1.2.4.1.1 "><p id="p5218617"><a name="p5218617"></a><a name="p5218617"></a>exact</p>
</td>
<td class="cellrowborder" valign="top" width="19.371937193719376%" headers="mcps1.2.4.1.2 "><p id="p20054846"><a name="p20054846"></a><a name="p20054846"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="56.43564356435644%" headers="mcps1.2.4.1.3 "><p id="p13829815"><a name="p13829815"></a><a name="p13829815"></a>Should the export be exact. Exact export maintains cluster-specific fields like 'Namespace'.</p>
</td>
</tr>
<tr id="row57359475"><td class="cellrowborder" valign="top" width="24.192419241924192%" headers="mcps1.2.4.1.1 "><p id="p15605878"><a name="p15605878"></a><a name="p15605878"></a>export</p>
</td>
<td class="cellrowborder" valign="top" width="19.371937193719376%" headers="mcps1.2.4.1.2 "><p id="p56116577"><a name="p56116577"></a><a name="p56116577"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="56.43564356435644%" headers="mcps1.2.4.1.3 "><p id="p49148893"><a name="p49148893"></a><a name="p49148893"></a>Should this value be exported. Export strips fields that a user cannot specify.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section42673379"></a>

N/A

## 响应消息<a name="section48516097"></a>

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
        "resourceVersion": "5391205",
        "creationTimestamp": "2018-09-05T01:10:59Z",
        "labels": {
            "job-name": "pi",
            "controller-uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4"
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
    "status": {
        "startTime": "2018-09-05T01:10:59Z",
        "active": 1
    }
}
```

## 状态码<a name="section33991695"></a>

[表3](#d0e41570)描述API的状态码。

**表 3**  状态码

<a name="d0e41570"></a>
<table><thead align="left"><tr id="row22801529"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p34984551"><a name="p34984551"></a><a name="p34984551"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p15176386"><a name="p15176386"></a><a name="p15176386"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row21327729"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p49824477"><a name="p49824477"></a><a name="p49824477"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p9250797"><a name="p9250797"></a><a name="p9250797"></a>This operation succeeds, and a Job resource object is returned.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

