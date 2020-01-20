# 更新Volcano Job<a name="cci_02_3138"></a>

## 功能介绍<a name="section19030251"></a>

更新Volcano Job。

The following fields can be updated:

-   metadata.labels
-   metadata.generateName
-   metadata.annotations
-   spec.template
-   spec.replicas

## URI<a name="section37054533"></a>

PATCH /apis/batch.volcano.sh/v1alpha1/namespaces/\{namespace\}/jobs/\{name\}

**表 1**  Path参数

<a name="d0e45179"></a>
<table><thead align="left"><tr id="row64943380"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="p65652297517"><a name="p65652297517"></a><a name="p65652297517"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.318368163183685%" id="mcps1.2.4.1.2"><p id="p165661629135114"><a name="p165661629135114"></a><a name="p165661629135114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.273672632736734%" id="mcps1.2.4.1.3"><p id="p14567629115114"><a name="p14567629115114"></a><a name="p14567629115114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row61989525"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1834011925520"><a name="p1834011925520"></a><a name="p1834011925520"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1733951915512"><a name="p1733951915512"></a><a name="p1733951915512"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p143381019155512"><a name="p143381019155512"></a><a name="p143381019155512"></a>name of the Volcano Job</p>
</td>
</tr>
<tr id="row14378174819716"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p103785481977"><a name="p103785481977"></a><a name="p103785481977"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1844813188462"><a name="p1844813188462"></a><a name="p1844813188462"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p637815481078"><a name="p637815481078"></a><a name="p637815481078"></a>object name and auth scope, such as for teams and projects</p>
</td>
</tr>
</tbody>
</table>

**表 2**  Query参数

<a name="table11308949102120"></a>
<table><thead align="left"><tr id="row23131949192118"><th class="cellrowborder" valign="top" width="20.407959204079592%" id="mcps1.2.4.1.1"><p id="p8316349122119"><a name="p8316349122119"></a><a name="p8316349122119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="16.318368163183685%" id="mcps1.2.4.1.2"><p id="p1231884913215"><a name="p1231884913215"></a><a name="p1231884913215"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="63.273672632736734%" id="mcps1.2.4.1.3"><p id="p2321124920215"><a name="p2321124920215"></a><a name="p2321124920215"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1934684942112"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p7834175920549"><a name="p7834175920549"></a><a name="p7834175920549"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p8834105912542"><a name="p8834105912542"></a><a name="p8834105912542"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p1083315596543"><a name="p1083315596543"></a><a name="p1083315596543"></a>If 'true’, then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section65055348"></a>

**请求示例**：

```
{
    "metadata": {
        "labels": {
            "app": "patchlabel"
        }
    }
}
```

## 响应消息<a name="section48627224"></a>

**响应参数：**

响应参数的详细描述请参考[表145](数据结构.md#table1251082312812)。

**响应示例**：

```
{
    "apiVersion": "batch.volcano.sh/v1alpha1",
    "kind": "Job",
    "metadata": {
        "creationTimestamp": "2019-06-26T03:16:26Z",
        "generation": 1,
        "labels": {
            "app": "patchlabel"
        },
        "name": "openmpi-hello-2-com",
        "namespace": "cci-namespace-42263891",
        "resourceVersion": "7695210",
        "selfLink": "/apis/batch.volcano.sh/v1alpha1/namespaces/cci-namespace-42263891/jobs/openmpi-hello-2-com",
        "uid": "c84d86f0-97c0-11e9-9d09-dc9914fb58e0"
    },
    "spec": {
        "minAvailable": 1,
        "plugins": {
            "env": [],
            "ssh": [],
            "svc": []
        },
        "queue": "default",
        "schedulerName": "volcano",
        "tasks": [
            {
                "name": "mpimaster",
                "policies": [
                    {
                        "action": "CompleteJob",
                        "event": "TaskCompleted"
                    }
                ],
                "replicas": 1,
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "command": [
                                    "/bin/sh",
                                    "-c",
                                    "MPI_HOST=`cat /etc/volcano/mpiworker.host | tr \"\\n\" \",\"`;\nmkdir -p /var/run/sshd; /usr/sbin/sshd;\nmpiexec --allow-run-as-root --host ${MPI_HOST} -np 2 mpi_hello_world 003e /home/re\n"
                                ],
                                "image": "*.*.*.*:20202/swr/openmpi-hello:3.28",
                                "name": "mpimaster",
                                "ports": [
                                    {
                                        "containerPort": 22,
                                        "name": "mpijob-port"
                                    }
                                ],
                                "resources": {
                                    "limits": {
                                        "cpu": "250m",
                                        "memory": "1Gi"
                                    },
                                    "requests": {
                                        "cpu": "250m",
                                        "memory": "1Gi"
                                    }
                                },
                                "workingDir": "/home"
                            }
                        ],
                        "imagePullSecrets": [
                            {
                                "name": "default-secret"
                            }
                        ],
                        "restartPolicy": "OnFailure"
                    }
                }
            },
            {
                "name": "mpiworker",
                "replicas": 2,
                "template": {
                    "spec": {
                        "containers": [
                            {
                                "command": [
                                    "/bin/sh",
                                    "-c",
                                    "mkdir -p /var/run/sshd; /usr/sbin/sshd -D;\n"
                                ],
                                "image": "*.*.*.*:20202/swr/openmpi-hello:3.28",
                                "name": "mpiworker",
                                "ports": [
                                    {
                                        "containerPort": 22,
                                        "name": "mpijob-port"
                                    }
                                ],
                                "resources": {
                                    "limits": {
                                        "cpu": "250m",
                                        "memory": "1Gi"
                                    },
                                    "requests": {
                                        "cpu": "250m",
                                        "memory": "1Gi"
                                    }
                                },
                                "workingDir": "/home"
                            }
                        ],
                        "imagePullSecrets": [
                            {
                                "name": "default-secret"
                            }
                        ],
                        "restartPolicy": "OnFailure"
                    }
                }
            }
        ]
    },
    "status": {
        "controlledResources": {
            "plugin-env": "env",
            "plugin-ssh": "ssh",
            "plugin-svc": "svc"
        },
        "minAvailable": 1,
        "pending": 3,
        "state": {
            "lastTransitionTime": "2019-06-26T03:16:27Z",
            "phase": "Inqueue"
        }
    }
}
```

## 状态码<a name="section34991834"></a>

**表 3**  状态码

<a name="d0e45308"></a>
<table><thead align="left"><tr id="row6630185"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p174074"><a name="p174074"></a><a name="p174074"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p14100028"><a name="p14100028"></a><a name="p14100028"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1251606"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1367711985419"><a name="p1367711985419"></a><a name="p1367711985419"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1767541915544"><a name="p1767541915544"></a><a name="p1767541915544"></a>OK</p>
</td>
</tr>
<tr id="row199771021496"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p159789211912"><a name="p159789211912"></a><a name="p159789211912"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p8978621794"><a name="p8978621794"></a><a name="p8978621794"></a>Unauthorized</p>
</td>
</tr>
<tr id="row1265182419333"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p465162419332"><a name="p465162419332"></a><a name="p465162419332"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1465111243335"><a name="p1465111243335"></a><a name="p1465111243335"></a>Internal Error</p>
</td>
</tr>
<tr id="row161771840173312"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p01771340183317"><a name="p01771340183317"></a><a name="p01771340183317"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p3177154073314"><a name="p3177154073314"></a><a name="p3177154073314"></a>Forbidden</p>
</td>
</tr>
<tr id="row9581108183412"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1458219819340"><a name="p1458219819340"></a><a name="p1458219819340"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1358210873416"><a name="p1358210873416"></a><a name="p1358210873416"></a>Conflict</p>
</td>
</tr>
<tr id="row8512114963618"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1651274919367"><a name="p1651274919367"></a><a name="p1651274919367"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p13512164910364"><a name="p13512164910364"></a><a name="p13512164910364"></a>BadRequest</p>
</td>
</tr>
</tbody>
</table>

