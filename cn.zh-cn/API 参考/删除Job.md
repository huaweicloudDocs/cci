# 删除Job<a name="cci_02_3040"></a>

## 功能介绍<a name="section41928453"></a>

删除Job。

## URI<a name="section41811761"></a>

DELETE /apis/batch/v1/namespaces/\{namespace\}/jobs/\{name\}

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

<a name="d0e40914"></a>
<table><thead align="left"><tr id="row55265855"><th class="cellrowborder" valign="top" width="24.19%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.82%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="55.989999999999995%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row64362693"><td class="cellrowborder" valign="top" width="24.19%" headers="mcps1.2.4.1.1 "><p id="p45995684"><a name="p45995684"></a><a name="p45995684"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="19.82%" headers="mcps1.2.4.1.2 "><p id="p34662956"><a name="p34662956"></a><a name="p34662956"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="55.989999999999995%" headers="mcps1.2.4.1.3 "><p id="p56236036"><a name="p56236036"></a><a name="p56236036"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
<tr id="row53231781"><td class="cellrowborder" valign="top" width="24.19%" headers="mcps1.2.4.1.1 "><p id="p16807041"><a name="p16807041"></a><a name="p16807041"></a>gracePeriodSeconds</p>
</td>
<td class="cellrowborder" valign="top" width="19.82%" headers="mcps1.2.4.1.2 "><p id="p19193048"><a name="p19193048"></a><a name="p19193048"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="55.989999999999995%" headers="mcps1.2.4.1.3 "><p id="p11133076"><a name="p11133076"></a><a name="p11133076"></a>The duration in seconds before the object should be deleted. Value must be a non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period for the specified type will be used. Defaults to a per object value if not specified. zero means delete immediately.</p>
</td>
</tr>
<tr id="row33088828"><td class="cellrowborder" valign="top" width="24.19%" headers="mcps1.2.4.1.1 "><p id="p62949386"><a name="p62949386"></a><a name="p62949386"></a>orphanDependents</p>
</td>
<td class="cellrowborder" valign="top" width="19.82%" headers="mcps1.2.4.1.2 "><p id="p65735472"><a name="p65735472"></a><a name="p65735472"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="55.989999999999995%" headers="mcps1.2.4.1.3 "><p id="p22973015"><a name="p22973015"></a><a name="p22973015"></a>Deprecated: please use the PropagationPolicy, this field will be deprecated in 1.7. Should the dependent objects be orphaned. If true/false, the "orphan" finalizer will be added to/removed from the object's finalizers list. Either this field or PropagationPolicy may be set, but not both.</p>
</td>
</tr>
<tr id="row5430546"><td class="cellrowborder" valign="top" width="24.19%" headers="mcps1.2.4.1.1 "><p id="p37221085"><a name="p37221085"></a><a name="p37221085"></a>propagationPolicy</p>
</td>
<td class="cellrowborder" valign="top" width="19.82%" headers="mcps1.2.4.1.2 "><p id="p62117884"><a name="p62117884"></a><a name="p62117884"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="55.989999999999995%" headers="mcps1.2.4.1.3 "><p id="p12794299614"><a name="p12794299614"></a><a name="p12794299614"></a>Whether and how garbage collection will be performed. Either this field or OrphanDependents may be set, but not both. The default policy is decided by the existing finalizer set in the metadata.finalizers and the resource-specific default policy. Acceptable values are: 'Orphan' - orphan the dependents; 'Background' - allow the garbage collector to delete the dependents in the background; 'Foreground' - a cascading policy that deletes all dependents in the foreground.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section40761536"></a>

**请求参数：**

请求参数如[表64](数据结构.md#zh-cn_topic_0091433700_d0e41006)所示。

**请求示例：**

-   只删除Job（对应Pod不删除）：

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "gracePeriodSeconds": 0,
        "propagationPolicy": "Orphan"
    }
    ```

-   前台级联删除（按照Pod-\>Job的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Foreground"
    }
    ```

-   后台级联删除（按照Job-\>Pod的顺序进行删除）

    ```
    {
        "kind": "DeleteOptions",
        "apiVersion": "v1",
        "propagationPolicy": "Background"
    }
    ```


## 响应消息<a name="section31309505"></a>

**响应参数：**

响应参数的详细描述请参见[表 JobStatus字段数据结构说明](数据结构.md#table28665255)。

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
        "resourceVersion": "5415127",
        "creationTimestamp": "2018-09-05T01:10:59Z",
        "deletionTimestamp": "2018-09-05T03:27:34Z",
        "deletionGracePeriodSeconds": 0,
        "labels": {
            "app": "test2",
            "controller-uid": "8c923079-b0a8-11e8-8bcb-f898ef6c78b4",
            "job-name": "pi"
        },
        "finalizers": [
            "orphan"
        ],
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
                                "memory": "1Gi",
                                "cpu": "500m"
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

## 状态码<a name="section13350095"></a>

[表3](#d0e41189)描述API的状态码。

**表 3**  状态码

<a name="d0e41189"></a>
<table><thead align="left"><tr id="row46934970"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p43636236"><a name="p43636236"></a><a name="p43636236"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p44874251"><a name="p44874251"></a><a name="p44874251"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row10935710"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p13377326"><a name="p13377326"></a><a name="p13377326"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p9821602"><a name="p9821602"></a><a name="p9821602"></a>Delete a Job resource object successfully.</p>
</td>
</tr>
</tbody>
</table>

更多状态码请参见[状态码](状态码.md)。

