# 云审计服务支持的CCI操作列表<a name="cci_01_0084"></a>

CCI通过云审计服务（Cloud Trace Service，简称CTS）为您提供云服务资源的操作记录，记录内容包括您从云管理控制台或者开放API发起的云服务资源操作请求以及每次请求的结果，供您查询、审计和回溯使用。

**表 1**  云审计服务支持的CCI操作列表

|操作名称|事件名称|
|--|--|
|创建一个Service对象|createService|
|删除一个Service对象|deleteService|
|删除指定Namespace下的所有Service对象|deleteServicesByNamespace|
|替换指定的Service对象|replaceService|
|更新指定的Service对象|updateService|
|删除一个Endpoint对象|deleteEndpoint|
|删除指定Namespace下的所有Endpoint对象|deleteEndpointsByNamespace|
|替换指定Namespace下的Endpoint对象|replaceEndpoint|
|更新指定Namespace下的Endpoint对象|updateEndpoint|
|创建一个Deployment对象|createDeployment|
|删除一个Deployment对象|deleteDeployment|
|删除指定Namespace下的所有Deployment对象|deleteDeploymentsByNamespace|
|替换指定Namespace下的Deployment对象|replaceDeployment|
|更新指定Namespace下的Deployment对象|updateDeployment|
|创建一个Statefulset对象|createStatefulset|
|删除一个Statefulset对象|deleteStatefulset|
|删除指定Namespace下的所有Statefulset对象|deleteStatefulsetsByNamespace|
|替换指定Namespace下的Statefulset对象|replaceStatefulset|
|更新指定Namespace下的Statefulset对象|updateStatefulset|
|创建一个Job对象|createJob|
|删除一个Job对象|deleteJob|
|删除指定Namespace下的所有Job对象|deleteJobsByNamespace|
|替换指定Namespace下的某个Job对象的状态|replaceJob|
|更新指定Namespace下的某个Job对象的状态|updateJob|
|创建一个Cronjob对象|createCronjob|
|删除一个Cronjob对象|deleteCronjob|
|删除指定Namespace下的所有Cronjob对象|deleteCronjobsByNamespace|
|替换指定Namespace下的某个Cronjob对象的状态|replaceCronjob|
|更新指定Namespace下的某个Cronjob对象的状态|updateCronjob|
|创建一个Ingress对象|createIngress|
|删除一个Ingress对象|deleteIngress|
|删除指定Namespace下的所有Ingress对象|deleteIngressesByNamespace|
|替换指定Namespace下的特定Ingress对象|replaceIngress|
|更新指定Namespace下的某个Ingress对象的状态|updateIngress|
|创建一个Namespace|createNamespace|
|删除一个Namespace|deleteNamespace|
|创建一个Pod|createPod|
|更新指定Pod|updatePod|
|替换指定Pod|replacePod|
|删除一个Pod|deletePod|
|删除Namespace下所有的Pod|deletePodsByNamespace|
|删除指定Event|deleteEvent|
|创建一个Configmap|createConfigmap|
|更新指定Configmap|updateConfigmap|
|替换指定Configmap|replaceConfigmap|
|删除一个Configmap|deleteConfigmap|
|删除指定Namespace下所有的Configmap|deleteConfigmapsByNamespace|
|创建一个Secret|createSecret|
|更新指定Secret|updateSecret|
|替换指定Secret|replaceSecret|
|删除指定Secret|deleteSecret|
|删除指定Namespace下所有的Secret|deleteSecretsByNamespace|
|删除指定Network|deleteNetwork|
|创建一个Network|createNetwork|
|删除指定Namespace下所有的Network|deleteNetworksByNamespace|
|更新指定Network|updateNetwork|
|替换指定Network|replaceNetwork|
|创建network-attachment-definition|createNetworkAttachmentDefinition|
|删除指定Namespace下所有的network-attachment-definitions|deleteNetworkAttachmentDefinitionsByNamespace|
|删除指定network-attachment-definition|deleteNetworkAttachmentDefinition|
|创建PV|createPersistentvolume|
|删除指定Namespace下所有的PV|deletePersistentvolumesByNamespace|
|替换指定PV|replacePersistentvolume|
|更新指定PV|updatePersistentvolume|
|删除指定PV|deletePersistentvolume|
|创建PVC|createPersistentvolumeclaim|
|导入已有PVC|createPersistentvolumeclaimByStorageInfo|
|删除指定Namespace下所有的PVC|deletePersistentvolumeclaimsByNamespace|
|替换指定PVC|replacePersistentvolumeclaim|
|更新指定PVC|updatePersistentvolumeclaim|
|删除指定PVC|deletePersistentvolumeclaim|
|购买一个套餐包|createPackageproduct|
|购买活动套餐包|createActiveproduct|
|创建Kubeflow job|createKubeflowJob|
|删除指定Namespace下所有的Kubeflow job|deleteKubeflowJobsByNamespace|
|替换指定Kubeflow job|replaceKubeflowJob|
|更新指定Kubeflow job|updateKubeflowJob|
|删除指定Kubeflow job|deleteKubeflowJob|
|创建Volcano job|createVolcanoJob|
|删除指定Namespace下所有的Volcano job|deleteVolcanoJobsByNamespace|
|替换指定Volcano job|replaceVolcanoJob|
|更新指定Volcano job|updateVolcanoJob|
|删除指定Volcano job|deleteVolcanoJob|
|创建Agency|createAgency|
|更新配额|modifyQuota|
|创建一个imagecache对象|createImagecache|
|删除一个imagecache对象|deleteImagecache|
|替换指定的imagecache对象|replaceImagecache|
|更新指定的imagecache对象|updateImagecache|
|上传模板|createChart|
|更新指定模板|updateChart|
|删除指定模板|deleteChart|
|上传插件|createAddon|
|更新指定插件|updateAddon|
|删除指定插件|deleteAddon|
|创建模板实例|createRelease|
|更新模板实例|updateRelease|
|删除模板实例|deleteRelease|
|创建插件实例|createAddonInstance|
|更新插件实例|updateAddonInstance|
|删除插件实例|deleteAddonInstance|
|创建插件readme|createAddonReadme|
|删除插件Readme|deleteAddonReadme|


