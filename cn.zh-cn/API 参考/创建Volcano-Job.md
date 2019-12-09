# 创建Volcano Job<a name="cci_02_3133"></a>

## 功能介绍<a name="section19030251"></a>

创建Volcano Job。

## URI<a name="section37054533"></a>

POST /apis/batch.volcano.sh/v1alpha1/namespaces/\{namespace\}/jobs

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
<tbody><tr id="row61989525"><td class="cellrowborder" valign="top" width="20.407959204079592%" headers="mcps1.2.4.1.1 "><p id="p1834011925520"><a name="p1834011925520"></a><a name="p1834011925520"></a>namespace</p>
</td>
<td class="cellrowborder" valign="top" width="16.318368163183685%" headers="mcps1.2.4.1.2 "><p id="p1733951915512"><a name="p1733951915512"></a><a name="p1733951915512"></a>Yes</p>
</td>
<td class="cellrowborder" valign="top" width="63.273672632736734%" headers="mcps1.2.4.1.3 "><p id="p143381019155512"><a name="p143381019155512"></a><a name="p143381019155512"></a>object name and auth scope, such as for teams and projects</p>
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

请求参数的详细描述请参考[表144](数据结构.md#table1251082312812)。

**请求示例**：

```
{
    "apiVersion": "batch.volcano.sh/v1alpha1",
    "kind": "Job",
    "metadata": {
        "name": "openmpi-hello-2-com"
    },
    "spec": {
        "minAvailable": 1,
        "schedulerName": "volcano",
        "plugins": {
            "ssh": [],
            "env": [],
            "svc": []
        },
        "tasks": [
            {
                "replicas": 1,
                "name": "mpimaster",
                "policies": [
                    {
                        "event": "TaskCompleted",
                        "action": "CompleteJob"
                    }
                ],
                "template": {
                    "spec": {
                        "imagePullSecrets": [
                            {
                                "name": "default-secret"
                            }
                        ],
                        "containers": [
                            {
                                "command": [
                                    "/bin/sh",
                                    "-c",
                                    "MPI_HOST=`cat/etc/volcano/mpiworker.host|tr\"\\n\"\",\"`;\nmkdir-p/var/run/sshd;/usr/sbin/sshd;\nmpiexec--allow-run-as-root--host${\t\t\t\t\t\t\tMPI_HOST\t\t\t\t\t\t}-np2mpi_hello_world>/home/re\n"
                                ],
                                "image": "*.*.*.*: 20202/swr/openmpi-hello:3.28",
                                "name": "mpimaster",
                                "ports": [
                                    {
                                        "containerPort": 22,
                                        "name": "mpijob-port"
                                    }
                                ],
                                "resources": {
                                    "requests": {
                                        "cpu": "250m",
                                        "memory": "1Gi"
                                    },
                                    "limits": {
                                        "cpu": "250m",
                                        "memory": "1Gi"
                                    }
                                },
                                "workingDir": "/home"
                            }
                        ],
                        "restartPolicy": "OnFailure"
                    }
                }
            },
            {
                "replicas": 2,
                "name": "mpiworker",
                "template": {
                    "spec": {
                        "imagePullSecrets": [
                            {
                                "name": "default-secret"
                            }
                        ],
                        "containers": [
                            {
                                "command": [
                                    "/bin/sh",
                                    "-c",
                                    "mkdir-p/var/run/sshd;/usr/sbin/sshd-D;\n"
                                ],
                                "image": "*.*.*.*:20202/swr/openmpi-hello:3.28",
                                "name": "mpiworker",
                                "ports": [
                                    {
                                        "containerPort": 22,
                                        "name": "mpijob-port"
                                    }
                                ],
                                "workingDir": "/home",
                                "resources": {
                                    "requests": {
                                        "cpu": "250m",
                                        "memory": "1Gi"
                                    },
                                    "limits": {
                                        "cpu": "250m",
                                        "memory": "1Gi"
                                    }
                                }
                            }
                        ],
                        "restartPolicy": "OnFailure"
                    }
                }
            }
        ]
    }
}
```

## 响应消息<a name="section48627224"></a>

**响应参数：**

响应参数的详细描述请参考[表144](数据结构.md#table1251082312812)。

**响应示例**：

```
{
    "apiVersion": "batch.volcano.sh/v1alpha1",
    "kind": "Job",
    "metadata": {
        "creationTimestamp": "2019-06-26T06:24:50Z",
        "generation": 1,
        "name": "openmpi-hello-3-com",
        "namespace": "cci-namespace-42263891",
        "resourceVersion": "7681331",
        "selfLink": "/apis/batch.volcano.sh/v1alpha1/namespaces/cci-namespace-42263891/jobs/openmpi-hello-3-com",
        "uid": "1a32a8c4-97db-11e9-9d09-dc9914fb58e0"
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
<tr id="row378665516338"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p47871755163319"><a name="p47871755163319"></a><a name="p47871755163319"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1787955113318"><a name="p1787955113318"></a><a name="p1787955113318"></a>Created</p>
</td>
</tr>
<tr id="row276226123417"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1876246203420"><a name="p1876246203420"></a><a name="p1876246203420"></a>202</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p77622693411"><a name="p77622693411"></a><a name="p77622693411"></a>Accepted</p>
</td>
</tr>
<tr id="row17949182183412"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p14949421183410"><a name="p14949421183410"></a><a name="p14949421183410"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1794922133417"><a name="p1794922133417"></a><a name="p1794922133417"></a>Unauthorized</p>
</td>
</tr>
<tr id="row55491342202914"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1777215672810"><a name="p1777215672810"></a><a name="p1777215672810"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1877275619281"><a name="p1877275619281"></a><a name="p1877275619281"></a>Badrequest</p>
</td>
</tr>
<tr id="row12549164252917"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p114411511294"><a name="p114411511294"></a><a name="p114411511294"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p8144175192919"><a name="p8144175192919"></a><a name="p8144175192919"></a>Internal error</p>
</td>
</tr>
<tr id="row1208145212444"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p520911524449"><a name="p520911524449"></a><a name="p520911524449"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p32096525448"><a name="p32096525448"></a><a name="p32096525448"></a>Forbidden</p>
</td>
</tr>
</tbody>
</table>

