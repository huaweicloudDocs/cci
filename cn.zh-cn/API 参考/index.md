# API参考

-   [使用前必读]
    -   [概述](概述.md)
    -   [调用说明](调用说明.md)
    -   [终端节点](终端节点.md)
    -   [约束限制](约束限制.md)
    -   [基本概念](基本概念.md)
    -   [API版本选择建议](API版本选择建议.md)

-   [API概览](API概览.md)
-   [如何调用API]
    -   [构造请求](构造请求.md)
    -   [认证鉴权](认证鉴权.md)
    -   [返回结果](返回结果.md)

-   [快速入门](快速入门.md)
-   [API]
    -   [Network]
        -   [创建Network](创建Network.md)
        -   [查询Network](查询Network.md)
        -   [查询所有Network](查询所有Network.md)
        -   [查询Network状态](查询Network状态.md)
        -   [删除Network](删除Network.md)
        -   [删除所有Network](删除所有Network.md)

    -   [Extended PersistentVolumeClaim]
        -   [导入存储](导入存储.md)
        -   [查询导入的PVC](查询导入的PVC.md)
        -   [解绑存储](解绑存储.md)

    -   [迁移Namespace到专属集群](迁移Namespace到专属集群.md)

-   [Kubernetes API]
    -   [Namespace]
        -   [创建Namespace](创建Namespace.md)
        -   [查询Namespace](查询Namespace.md)
        -   [列出Namespace](列出Namespace.md)
        -   [删除Namespace](删除Namespace.md)

    -   [Pod]
        -   [创建Pod](创建Pod.md)
        -   [查询Pod](查询Pod.md)
        -   [查询指定Namespace下所有Pod](查询指定Namespace下所有Pod.md)
        -   [查询Pod状态](查询Pod状态.md)
        -   [查询Pod日志](查询Pod日志.md)
        -   [列出用户所有的Pod](列出用户所有的Pod.md)
        -   [替换Pod](替换Pod.md)
        -   [更新Pod](更新Pod.md)
        -   [删除Pod](删除Pod.md)
        -   [删除所有Pod](删除所有Pod.md)

    -   [Deployment]
        -   [创建Deployment](创建Deployment.md)
        -   [查询Deployment](查询Deployment.md)
        -   [查询Namespace下所有Deployment](查询Namespace下所有Deployment.md)
        -   [查询Deployment状态](查询Deployment状态.md)
        -   [查询Deployment的伸缩操作](查询Deployment的伸缩操作.md)
        -   [列出用户所有Deployment](列出用户所有Deployment.md)
        -   [替换Deployment](替换Deployment.md)
        -   [替换Deployment的伸缩操作](替换Deployment的伸缩操作.md)
        -   [更新Deployment](更新Deployment.md)
        -   [更新Deployment的伸缩操作](更新Deployment的伸缩操作.md)
        -   [删除Deployment](删除Deployment.md)
        -   [删除所有Deployment](删除所有Deployment.md)

    -   [StatefulSet]
        -   [创建StatefulSet](创建StatefulSet.md)
        -   [查询StatefulSet](查询StatefulSet.md)
        -   [查询指定namespace下所有StatefulSet](查询指定namespace下所有StatefulSet.md)
        -   [查询StatefulSet状态](查询StatefulSet状态.md)
        -   [列出用户所有的StatefulSet](列出用户所有的StatefulSet.md)
        -   [替换StatefulSet](替换StatefulSet.md)
        -   [更新StatefulSet](更新StatefulSet.md)
        -   [删除StatefulSet](删除StatefulSet.md)
        -   [删除所有StatefulSet](删除所有StatefulSet.md)

    -   [Job]
        -   [创建Job](创建Job.md)
        -   [查询Job](查询Job.md)
        -   [查询指定namespace下所有Job](查询指定namespace下所有Job.md)
        -   [查询Job状态](查询Job状态.md)
        -   [列出用户所有Job](列出用户所有Job.md)
        -   [替换Job](替换Job.md)
        -   [更新Job](更新Job.md)
        -   [删除Job](删除Job.md)
        -   [删除所有Job](删除所有Job.md)

    -   [Service]
        -   [创建Service](创建Service.md)
        -   [查询Service](查询Service.md)
        -   [查询所有Service](查询所有Service.md)
        -   [查询service状态](查询service状态.md)
        -   [删除Service](删除Service.md)

    -   [Ingress]
        -   [创建Ingress](创建Ingress.md)
        -   [查询Ingress](查询Ingress.md)
        -   [查询所有Ingress](查询所有Ingress.md)
        -   [查询Ingress状态](查询Ingress状态.md)
        -   [替换Ingress](替换Ingress.md)
        -   [更新Ingress](更新Ingress.md)
        -   [删除Ingress](删除Ingress.md)
        -   [删除所有ingress](删除所有ingress.md)

    -   [ConfigMap]
        -   [创建ConfigMap](创建ConfigMap.md)
        -   [查询ConfigMap](查询ConfigMap.md)
        -   [查询所有ConfigMap](查询所有ConfigMap.md)
        -   [替换ConfigMap](替换ConfigMap.md)
        -   [更新ConfigMap](更新ConfigMap.md)
        -   [删除ConfigMap](删除ConfigMap.md)
        -   [删除所有ConfigMap](删除所有ConfigMap.md)

    -   [Secret]
        -   [创建Secret](创建Secret.md)
        -   [替换Secret](替换Secret.md)
        -   [更新Secret](更新Secret.md)
        -   [删除Secret](删除Secret.md)
        -   [删除所有Secret](删除所有Secret.md)

    -   [PersistentVolumeClaim]
        -   [创建PersistentVolumeClaim](创建PersistentVolumeClaim.md)
        -   [查询PersistentVolumeClaim](查询PersistentVolumeClaim.md)
        -   [查询所有PersistentVolumeClaim](查询所有PersistentVolumeClaim.md)
        -   [删除PersistentVolumeClaim](删除PersistentVolumeClaim.md)

    -   [Event]
        -   [查询Event](查询Event.md)
        -   [查询所有Event](查询所有Event.md)
        -   [删除Event](删除Event.md)

    -   [API groups]
        -   [列出APIVersions](列出APIVersions.md)
        -   [列出APIGroups](列出APIGroups.md)
        -   [列出所有extensions/v1beta1版本的API](列出所有extensions-v1beta1版本的API.md)
        -   [列出所有apps/v1版本的API](列出所有apps-v1版本的API.md)
        -   [列出所有apps/v1beta1版本的API](列出所有apps-v1beta1版本的API.md)
        -   [列出所有batch/v1版本的API](列出所有batch-v1版本的API.md)
        -   [列出所有networking.cci.io/v1beta1版本的API](列出所有networking-cci-io-v1beta1版本的API.md)
        -   [列出所有v1版本的API](列出所有v1版本的API.md)

    -   [Endpoint]
        -   [查询Endpoint](查询Endpoint.md)
        -   [查询所有Endpoints](查询所有Endpoints.md)

    -   [ReplicaSet]
        -   [查询所有ReplicaSets](查询所有ReplicaSets.md)

    -   [VolcanoJob]
        -   [获取namespace下的所有Volcano Job](获取namespace下的所有Volcano-Job.md)
        -   [创建Volcano Job](创建Volcano-Job.md)
        -   [删除namespace下的所有Volcano Job](删除namespace下的所有Volcano-Job.md)
        -   [查询Volcano Job详情](查询Volcano-Job详情.md)
        -   [替换Volcano Job](替换Volcano-Job.md)
        -   [删除Volcano Job](删除Volcano-Job.md)
        -   [更新Volcano Job](更新Volcano-Job.md)

    -   [TFJob]
        -   [创建TFJob](创建TFJob.md)
        -   [查询TFJob](查询TFJob.md)
        -   [查询指定namespace下的所有TFJob](查询指定namespace下的所有TFJob.md)
        -   [删除namespace下的所有TFJob](删除namespace下的所有TFJob.md)
        -   [删除TFJob](删除TFJob.md)
        -   [更新TFJob](更新TFJob.md)
        -   [替换TFJob](替换TFJob.md)

    -   [MXJob]
        -   [创建MXJob](创建MXJob.md)
        -   [查询MXJob](查询MXJob.md)
        -   [查询指定namespace下的所有MXJob](查询指定namespace下的所有MXJob.md)
        -   [删除namespace下的所有MXJob](删除namespace下的所有MXJob.md)
        -   [删除MXJob](删除MXJob.md)
        -   [更新MXJob](更新MXJob.md)
        -   [替换MXJob](替换MXJob.md)

    -   [PyTorchJob]
        -   [创建PyTorchJob](创建PyTorchJob.md)
        -   [查询PyTorchJob](查询PyTorchJob.md)
        -   [查询指定namespace下的所有PyTorchJob](查询指定namespace下的所有PyTorchJob.md)
        -   [删除namespace下的所有PyTorchJob](删除namespace下的所有PyTorchJob.md)
        -   [删除PyTorchJob](删除PyTorchJob.md)
        -   [更新PyTorchJob](更新PyTorchJob.md)
        -   [替换PyTorchJob](替换PyTorchJob.md)

    -   [MPIJob]
        -   [创建MPIJob](创建MPIJob.md)
        -   [查询MPIJob](查询MPIJob.md)
        -   [查询指定namespace下的所有MPIJob](查询指定namespace下的所有MPIJob.md)
        -   [删除指定namespace下的所有MPIJob](删除指定namespace下的所有MPIJob.md)
        -   [删除MPIJob](删除MPIJob.md)
        -   [更新MPIJob](更新MPIJob.md)
        -   [替换MPIJob](替换MPIJob.md)

    -   [RBAC]
        -   [ClusterRole]
            -   [获取指定的ClusterRole](获取指定的ClusterRole.md)
            -   [获取ClusterRole列表](获取ClusterRole列表.md)

        -   [RoleBinding]
            -   [创建RoleBinding](创建RoleBinding.md)
            -   [更新指定的RoleBinding](更新指定的RoleBinding.md)
            -   [替换指定的RoleBinding](替换指定的RoleBinding.md)
            -   [删除指定的RoleBinding](删除指定的RoleBinding.md)
            -   [获取指定的RoleBinding](获取指定的RoleBinding.md)
            -   [获取指定namespace下RoleBinding列表](获取指定namespace下RoleBinding列表.md)
            -   [获取RoleBinding列表](获取RoleBinding列表.md)



-   [Kubernetes API （OLD VERSIONS）]
    -   [Deployment]
        -   [创建Deployment](创建Deployment（v1beta1）.md)
        -   [创建Deployment回滚](创建Deployment回滚（v1beta1）.md)
        -   [查询Deployment](查询Deployment（v1beta1）.md)
        -   [查询所有Deployment](查询所有Deployment（v1beta1）.md)
        -   [查询Deployment的状态](查询Deployment的状态（v1beta1）.md)
        -   [替换Deployment](替换Deployment（v1beta1）.md)
        -   [更新Deployment](更新Deployment（v1beta1）.md)
        -   [删除Deployment](删除Deployment（v1beta1）.md)
        -   [删除所有Deployment](删除所有Deployment（v1beta1）.md)

    -   [Statefulset]
        -   [创建StatefulSet](创建StatefulSet（v1beta1）.md)
        -   [查询StatefulSet](查询StatefulSet（v1beta1）.md)
        -   [查询所有StatefulSet](查询所有StatefulSet（v1beta1）.md)
        -   [查询StatefulSet状态](查询StatefulSet状态（v1beta1）.md)
        -   [替换StatefulSet](替换StatefulSet（v1beta1）.md)
        -   [更新StatefulSet](更新StatefulSet（v1beta1）.md)
        -   [删除StatefulSet](删除StatefulSet（v1beta1）.md)
        -   [删除所有StatefulSet](删除所有StatefulSet（v1beta1）.md)


-   [数据结构]
    -   [请求数据结构（OLD VERSIONS）](请求数据结构（OLD-VERSIONS）.md)
    -   [响应数据结构（OLD VERSIONS）](响应数据结构（OLD-VERSIONS）.md)
    -   [数据结构](数据结构.md)

-   [权限和授权项]
    -   [权限及授权项说明](权限及授权项说明.md)
    -   [授权项分类](授权项分类.md)

-   [附录]
    -   [PATCH请求方法操作说明](PATCH请求方法操作说明.md)
    -   [PATCH请求方法操作示例](PATCH请求方法操作示例.md)
    -   [状态码](状态码.md)
    -   [错误码](错误码.md)
    -   [获取项目ID](获取项目ID.md)
    -   [获取账号ID](获取账号ID.md)
    -   [获取Docker镜像地址](获取Docker镜像地址.md)
    -   [挂载OBS使用限制](挂载OBS使用限制.md)


