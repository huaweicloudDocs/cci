# 查询导入的PVC<a name="cci_02_2022"></a>

## 功能介绍<a name="section54875957"></a>

查询指定命名空间下的PVC。

## URI<a name="section24121565"></a>

GET /api/v1/namespaces/\{namespace\}/extended-persistentvolumeclaims

**表 1**  Path参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|namespace|Yes|String|命名空间。|


**表 2**  Query参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|storageType|No|String|Type of storage，目前支持：bs: 云硬盘存储nfs: 文件存储efs:  极速文件存储如果本参数未指定，将默认返回当前命名空间下bs(云硬盘存储)类型的PVC信息。|


## 请求消息<a name="section15767494"></a>

N/A

## 响应消息<a name="section7689721"></a>

**响应参数**

**表 3**  响应参数

|参数|参数类型|描述|
|--|--|--|
|PersistentVolumeClaim|Object|详情请参见表175。|
|PersistentVolume|Object|详情请参见表184。|
|StorageInfo|Object|详情请参见表199。|


**响应示例**

```
[
    {
        "persistentVolumeClaim": {
            "metadata": {
                "name": "cci-evs-jxzqegxe-k1z3",
                "namespace": "test-namespace",
                "selfLink": "/api/v1/namespaces/csms/persistentvolumeclaims/cci-evs-jxzqegxe-k1z3",
                "uid": "e82c1574-a46d-11e9-be8a-b44326d0c915",
                "resourceVersion": "65003551",
                "creationTimestamp": "2019-07-12T06:25:56Z",
                "annotations": {
                    "pv.kubernetes.io/bind-completed": "yes",
                    "pv.kubernetes.io/bound-by-controller": "yes",
                    "volume.beta.kubernetes.io/storage-provisioner": "flexvolume-huawei.com/fuxivol"
                },
                "finalizers": [
                    "kubernetes.io/pvc-protection"
                ],
                "enable": true
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
                "volumeName": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
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
        },
        "persistentVolume": {
            "metadata": {
                "name": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                "selfLink": "/api/v1/persistentvolumes/pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                "uid": "eb0a0ca1-a46d-11e9-be8a-b44326d0c915",
                "resourceVersion": "65003549",
                "creationTimestamp": "2019-07-12T06:26:01Z",
                "labels": {
                    "tenant.kubernetes.io/domain-id": "f0c61dbd65974140956ed37a91ea860f",
                    "tenant.kubernetes.io/project-id": "cdb4249297a44665a63eec4f27ad09bf"
                },
                "annotations": {
                    "kubernetes.io/createdby": "huawei.com/fuxivol-dynamic-provisioner",
                    "pv.kubernetes.io/bound-by-controller": "yes",
                    "pv.kubernetes.io/namespace": "test-namespace",
                    "pv.kubernetes.io/provisioned-by": "flexvolume-huawei.com/fuxivol",
                    "tenant.kubernetes.io/domain-id": "f0c61dbd65974140956ed37a91ea860f",
                    "tenant.kubernetes.io/project-id": "cdb4249297a44665a63eec4f27ad09bf"
                },
                "finalizers": [
                    "kubernetes.io/pv-protection"
                ]
            },
            "spec": {
                "capacity": {
                    "storage": "10Gi"
                },
                "flexVolume": {
                    "driver": "huawei.com/fuxivol",
                    "fsType": "ext4",
                    "options": {
                        "fsType": "ext4",
                        "volumeID": "06e10708-6412-4190-8496-f9531fb5fd0c"
                    }
                },
                "accessModes": [
                    "ReadWriteMany"
                ],
                "claimRef": {
                    "kind": "PersistentVolumeClaim",
                    "namespace": "test-namespace",
                    "name": "cci-evs-jxzqegxe-k1z3",
                    "uid": "e82c1574-a46d-11e9-be8a-b44326d0c915",
                    "apiVersion": "v1",
                    "resourceVersion": "65003516"
                },
                "persistentVolumeReclaimPolicy": "Delete",
                "storageClassName": "sata"
            },
            "status": {
                "phase": "Bound"
            }
        },
        "storageInfo": {
            "kind": "Volume",
            "apiVersion": "paas/v1beta1",
            "metadata": {
                "name": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                "creationTimestamp": "2019-07-12T06:25:56Z",
                "labels": {
                    "__system__volume_name": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                    "hw:passthrough": "true",
                    "kubernetes.io/namespace": "test-namespace",
                    "tenant.kubernetes.io/domain-id": "f0c61dbd65974140956ed37a91ea860f",
                    "tenant.kubernetes.io/project-id": "cdb4249297a44665a63eec4f27ad09bf"
                }
            },
            "spec": {
                "name": "pvc-e82c1574-a46d-11e9-be8a-b44326d0c915",
                "size": 10,
                "inresourcepool": false,
                "availability_zone": "cn-north-1a",
                "volume_type": "sata",
                "multiattach": true,
                "access": {
                    "": {
                        "access_type": "",
                        "access_to": "",
                        "access_level": "",
                        "id": "",
                        "state": ""
                    }
                },
                "vpc_id": ""
            },
            "status": {
                "id": "06e10708-6412-4190-8496-f9531fb5fd0c",
                "status": "available",
                "created_at": "2019-07-12T06:25:56Z",
                "attachments": null,
                "app_info": null
            }
        }
    }
]
```

## 状态码<a name="section2098632"></a>

**表 4**  状态码

|状态码|描述|
|--|--|
|200|查询成功，并返回结果。|


更多状态码请参见[状态码](状态码.md)。

