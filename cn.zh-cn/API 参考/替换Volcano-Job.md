# 替换Volcano Job<a name="cci_02_3136"></a>

## 功能介绍<a name="section19030251"></a>

替换Volcano Job。

The following fields can be updated:

-   metadata.labels
-   metadata.generateName
-   metadata.annotations
-   spec.template
-   spec.replicas

## URI<a name="section37054533"></a>

PUT /apis/batch.volcano.sh/v1alpha1/namespaces/\{namespace\}/jobs/\{name\}

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
<tr id="row644831834616"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p134481718134616"><a name="p134481718134616"></a><a name="p134481718134616"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1844813188462"><a name="p1844813188462"></a><a name="p1844813188462"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p14448101814611"><a name="p14448101814611"></a><a name="p14448101814611"></a>object name and auth scope, such as for teams and projects</p>
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

请求参数的详细描述请参考[表145](数据结构.md#table1251082312812)。

**请求示例**：

将创建的Volcano Job的其中一个task的replicas从1修改为2：

```
{
    "apiVersion": "batch.volcano.sh/v1alpha1",
    "kind": "Job",
    "metadata": {
        "name": "openmpi-hello-2-com",
        "namespace": "cci-gpu",
        "resourceVersion": "125597961"
    },
    "spec": {
        "minAvailable": 2,
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
        "minAvailable": 1,
        "pending": 3,
        "state": {
            "lastTransitionTime": "2019-07-11T08:09:45Z",
            "phase": "Succeed"
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
        "creationTimestamp": "2019-07-11T08:09:41Z",
        "generation": 2,
        "name": "openmpi-hello-2-com",
        "namespace": "zjh-gpu",
        "resourceVersion": "125620754",
        "selfLink": "/apis/batch.volcano.sh/v1alpha1/namespaces/zjh-gpu/jobs/openmpi-hello-2-com",
        "uid": "3bdba739-a3b3-11e9-8865-501d93440997"
    },
    "spec": {
        "minAvailable": 2,
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
            "lastTransitionTime": "2019-07-11T08:09:45Z",
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
<tr id="row879116173917"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1679211153918"><a name="p1679211153918"></a><a name="p1679211153918"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p579251183914"><a name="p579251183914"></a><a name="p579251183914"></a>Created</p>
</td>
</tr>
<tr id="row6258191313397"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p11258313193912"><a name="p11258313193912"></a><a name="p11258313193912"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p10258181323910"><a name="p10258181323910"></a><a name="p10258181323910"></a>Unauthorized</p>
</td>
</tr>
<tr id="row134001428173217"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p6401028123219"><a name="p6401028123219"></a><a name="p6401028123219"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p5401122818324"><a name="p5401122818324"></a><a name="p5401122818324"></a>BadRequest</p>
</td>
</tr>
<tr id="row349744213329"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p34973426329"><a name="p34973426329"></a><a name="p34973426329"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p144971442123219"><a name="p144971442123219"></a><a name="p144971442123219"></a>Internal Error</p>
</td>
</tr>
<tr id="row166175823710"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p19660581370"><a name="p19660581370"></a><a name="p19660581370"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1266175883714"><a name="p1266175883714"></a><a name="p1266175883714"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

