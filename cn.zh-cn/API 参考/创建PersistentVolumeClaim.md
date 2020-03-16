# 创建PersistentVolumeClaim<a name="cci_02_3085"></a>

## 功能介绍<a name="s0a28adc85c784085a2d82fe65fbfc112"></a>

创建PersistentVolumeClaim，主要适用于动态创建存储的场景，即存储资源未创建时，创建PVC会根据请求内容创建一个存储资源。

当前支持**创建EVS（云硬盘卷，块存储）和SFS（文件存储卷）**，使用时 spec.storageClassName 参数的取值如下：

-   sata：普通I/O云硬盘卷
-   sas：高I/O云硬盘卷
-   ssd：超高I/O云硬盘卷
-   nfs-rw：标准文件协议类型文件存储卷

若不指定spec.storageClassName，可在metadata.annotations中指定volume.beta.kubernetes.io/storage-class，取值含义与spec.storageClassName 相同，这两个参数选择其中一个即可。

若需要创建加密类型存储卷，对于云硬盘存储卷需要在metadata.annotations中增加paas.storage.io/cryptKeyId字段；对于文件存储卷需要增加paas.storage.io/cryptKeyId、paas.storage.io/cryptAlias和paas.storage.io/cryptDomainId字段。

## URI<a name="sdad79289da6f40bfb1b0726f426f9f1f"></a>

POST /api/v1/namespaces/\{namespace\}/persistentvolumeclaims

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

<a name="tbb39505880dd47b7952941b52626bf77"></a>
<table><thead align="left"><tr id="rf1f3422b7e214676bd6220a3089a0b6c"><th class="cellrowborder" valign="top" width="22.06%" id="mcps1.2.4.1.1"><p id="a301ecfa05ce3484b872abcfe0f9a0bd9"><a name="a301ecfa05ce3484b872abcfe0f9a0bd9"></a><a name="a301ecfa05ce3484b872abcfe0f9a0bd9"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.36%" id="mcps1.2.4.1.2"><p id="p7604122714332"><a name="p7604122714332"></a><a name="p7604122714332"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="60.58%" id="mcps1.2.4.1.3"><p id="p2607102713310"><a name="p2607102713310"></a><a name="p2607102713310"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="rdf1dc9140a3b4b3c92cc8f904603ea5b"><td class="cellrowborder" valign="top" width="22.06%" headers="mcps1.2.4.1.1 "><p id="ab1a2800ea10145d7bbb8d4a1d91b26c3"><a name="ab1a2800ea10145d7bbb8d4a1d91b26c3"></a><a name="ab1a2800ea10145d7bbb8d4a1d91b26c3"></a>pretty</p>
</td>
<td class="cellrowborder" valign="top" width="17.36%" headers="mcps1.2.4.1.2 "><p id="affc15999723c44ecabaa9a50d861b5bb"><a name="affc15999723c44ecabaa9a50d861b5bb"></a><a name="affc15999723c44ecabaa9a50d861b5bb"></a>No</p>
</td>
<td class="cellrowborder" valign="top" width="60.58%" headers="mcps1.2.4.1.3 "><p id="ad893e4b8017643c4b53c96cdf6e47507"><a name="ad893e4b8017643c4b53c96cdf6e47507"></a><a name="ad893e4b8017643c4b53c96cdf6e47507"></a>If 'true', then the output is pretty printed.</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="sa85d89666a35466388180b7b77d8c772"></a>

**请求参数：**

请参见[表92](数据结构.md#t7aa9de1153e9466cbfcaa9af17a24772)。

**请求示例：**

-   创建一个大小为10G的加密云硬盘，类型为sata

    ```
    {
        "apiVersion": "v1",
        "kind": "PersistentVolumeClaim",
        "metadata": {
            "annotations": {
                "paas.storage.io/cryptKeyId":"ee9b610c-e356-11e9-aadc-d0efc1b3bb6b",
                "volume.beta.kubernetes.io/storage-class": "sata"
            },
            "name": "pvc-test",
            "namespace": "test-namespace"
        },
        "spec": {
            "accessModes": [
                "ReadWriteMany"
            ],
            "resources": {
                "requests": {
                    "storage": "10Gi"
                }
            }
        }
    }
    ```

-   创建一个大小为10G的加密文件存储卷

    ```
    {
        "apiVersion": "v1",
        "kind": "PersistentVolumeClaim",
        "metadata": {
            "annotations": {
               "paas.storage.io/cryptKeyId":"ee9b610c-e356-11e9-aadc-d0efc1b3bb6b",
               "paas.storage.io/cryptAlias":"sfs/default",
               "paas.storage.io/cryptDomainId":"d6912480-c3d6-4e9e-8c70-38afeea434c3",
               "volume.beta.kubernetes.io/storage-class": "nfs-rw"
            },
            "name": "pvc-test",
            "namespace": "test-namespace"
        },
        "spec": {
            "accessModes": [
                "ReadWriteMany"
            ],
            "resources": {
                "requests": {
                    "storage": "10Gi"
                }
            }
        }
    }
    ```


## 响应消息<a name="sfea287b75ddb40569f61ea90875869cb"></a>

**响应参数：**

响应参数的详细描述请参见[表92](数据结构.md#t7aa9de1153e9466cbfcaa9af17a24772)。

**响应示例：**

```
{
    "kind": "PersistentVolumeClaim",
    "apiVersion": "v1",
    "metadata": {
        "name": "pvc-test",
        "namespace": "test-namespace",
        "selfLink": "/api/v1/namespaces/ns-test/persistentvolumeclaims/pvc-test",
        "uid": "58d15f3e-efbd-11e8-8950-501d934409f3",
        "resourceVersion": "28156856",
        "creationTimestamp": "2018-11-24T07:48:35Z",
        "labels": {
            "app": "evs"
        },
        "annotations": {
            "paas.storage.io/cryptKeyId": "ee9b610c-e356-11e9-aadc-d0efc1b3bb6b",
            "pv.kubernetes.io/bind-completed": "yes",
            "pv.kubernetes.io/bound-by-controller": "yes",
            "volume.beta.kubernetes.io/storage-provisioner": "flexvolume-huawei.com/fuxivol"
        },
        "finalizers": [
            "kubernetes.io/pvc-protection"
        ]
    },
    "spec": {
        "accessModes": [
            "ReadWriteMany"
        ],
        "resources": {
            "requests": {
                "storage": "10Gi"
            }
        },
        "volumeName": "pvc-58d15f3e-efbd-11e8-8950-501d934409f3",
        "storageClassName": "sata"
    },
    "status": {
        "phase": "Bound",
        "accessModes": [
            "ReadWriteMany"
        ],
        "capacity": {
            "storage": "10Gi"
        }
    }
}
```

## 状态码<a name="s83847071f8aa4217be1335b90a09a193"></a>

[表3](#t395400749a4a48bdaa2c2d6467f593cd)描述API的状态码。

**表 3**  状态码

<a name="t395400749a4a48bdaa2c2d6467f593cd"></a>
<table><thead align="left"><tr id="rbe30eb05eac64354acc6ebc34daf65dc"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p1164219276335"><a name="p1164219276335"></a><a name="p1164219276335"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p18643192753317"><a name="p18643192753317"></a><a name="p18643192753317"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="r16588ef0f9eb42a78267e1bfe3ffde07"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="a714d32bf07ab434b9b247aafadab0e41"><a name="a714d32bf07ab434b9b247aafadab0e41"></a><a name="a714d32bf07ab434b9b247aafadab0e41"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="a5d57d5cda4e144c9a9688f3ed7abf5f0"><a name="a5d57d5cda4e144c9a9688f3ed7abf5f0"></a><a name="a5d57d5cda4e144c9a9688f3ed7abf5f0"></a>Created</p>
</td>
</tr>
<tr id="row453718139320"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p0537151373216"><a name="p0537151373216"></a><a name="p0537151373216"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1653711323212"><a name="p1653711323212"></a><a name="p1653711323212"></a>OK</p>
</td>
</tr>
<tr id="row971112288322"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1971119286322"><a name="p1971119286322"></a><a name="p1971119286322"></a>203</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p207111628193216"><a name="p207111628193216"></a><a name="p207111628193216"></a>Accepted</p>
</td>
</tr>
</tbody>
</table>

