# 创建PersistentVolumeClaim<a name="createCoreV1NamespacedPersistentVolumeClaim"></a>

## 功能介绍

创建PersistentVolumeClaim，主要适用于动态创建存储的场景，即存储资源未创建时，创建PVC会根据请求内容创建一个存储资源。

当前支持**创建EVS（云硬盘卷，块存储）和SFS（文件存储卷）**，使用时 spec.storageClassName 参数的取值如下：

-   sata：普通I/O云硬盘卷

-   sas：高I/O云硬盘卷

-   ssd：超高I/O云硬盘卷

-   nfs-rw：标准文件协议类型文件存储卷

-   csi-sfs：SFS 3.0容量型弹性文件服务


若不指定spec.storageClassName，可在metadata.annotations中指定volume.beta.kubernetes.io/storage-class，取值含义与spec.storageClassName 相同，这两个参数选择其中一个即可。

若需要创建加密类型存储卷，对于云硬盘存储卷需要在metadata.annotations中增加paas.storage.io/cryptKeyId字段；对于文件存储卷需要增加paas.storage.io/cryptKeyId、paas.storage.io/cryptAlias和paas.storage.io/cryptDomainId字段。

## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=CCI&api=createCoreV1NamespacedPersistentVolumeClaim)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

POST /api/v1/namespaces/\{namespace\}/persistentvolumeclaims

**表 1**  路径参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|namespace|是|String|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|pretty|否|String|If 'true', then the output is pretty printed.|


## 请求参数

**表 3**  请求Header参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|X-Auth-Token|是|String|用户Token。通过调用IAM服务获取用户Token接口获取（响应消息头中X-Subject-Token的值）。|
|Content-Type|是|String|消息体的类型（格式），默认取值为“application/json”缺省值：**application/json**|


**表 4**  请求Body参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|apiVersion|否|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|否|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|否|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|否|io.k8s.api.core.v1.PersistentVolumeClaimSpec object|Spec defines the desired characteristics of a volume requested by a pod author. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|
|status|否|io.k8s.api.core.v1.PersistentVolumeClaimStatus object|Status represents the current information/status of a persistent volume claim. Read-only. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|


**表 5**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta\_v3

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|annotations|否|Map<String,String>|Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations|
|clusterName|否|String|The name of the cluster which the object belongs to. This is used to distinguish resources with same name and namespace in different clusters. This field is not set anywhere right now and apiserver is going to ignore it if set in create or update request.|
|creationTimestamp|否|String|CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is represented in RFC3339 form and is in UTC.Populated by the system. Read-only. Null for lists. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|deletionGracePeriodSeconds|否|Long|Number of seconds allowed for this object to gracefully terminate before it will be removed from the system. Only set when deletionTimestamp is also set. May only be shortened. Read-only.|
|deletionTimestamp|否|String|DeletionTimestamp is RFC 3339 date and time at which this resource will be deleted. This field is set by the server when a graceful deletion is requested by the user, and is not directly settable by a client. The resource is expected to be deleted (no longer visible from resource lists, and not reachable by name) after the time in this field, once the finalizers list is empty. As long as the finalizers list contains items, deletion is blocked. Once the deletionTimestamp is set, this value may not be unset or be set further into the future, although it may be shortened or the resource may be deleted prior to this time. For example, a user may request that a pod is deleted in 30 seconds. The Kubelet will react by sending a graceful termination signal to the containers in the pod. After that 30 seconds, the Kubelet will send a hard termination signal (SIGKILL) to the container and after cleanup, remove the pod from the API. In the presence of network partitions, this object may still exist after this timestamp, until an administrator or automated process can determine the resource is fully terminated. If not set, graceful deletion of the object has not been requested.Populated by the system when a graceful deletion is requested. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|enable|否|Boolean|Enable identify whether the resource is available|
|finalizers|否|Array of strings|Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed.|
|generateName|否|String|GenerateName is an optional prefix, used by the server, to generate a unique name ONLY IF the Name field has not been provided. If this field is used, the name returned to the client will be different than the name passed. This value will also be combined with a unique suffix. The provided value has the same validation rules as the Name field, and may be truncated by the length of the suffix required to make the value unique on the server.If this field is specified and the generated name exists, the server will NOT return a 409 - instead, it will either return 201 Created or 500 with Reason ServerTimeout indicating a unique name could not be found in the time allotted, and the client should retry (optionally after the time indicated in the Retry-After header).Applied only if Name is not specified. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#idempotency|
|generation|否|Long|A sequence number representing a specific generation of the desired state. Populated by the system. Read-only.|
|initializers|否|io.k8s.apimachinery.pkg.apis.meta.v1.Initializers_v3 object|An initializer is a controller which enforces some system invariant at object creation time. This field is a list of initializers that have not yet acted on this object. If nil or empty, this object has been completely initialized. Otherwise, the object is considered uninitialized and is hidden (in list/watch and get calls) from clients that haven't explicitly asked to observe uninitialized objects.When an object is created, the system will populate this list with the current set of initializers. Only privileged users may set or modify this list. Once it is empty, it may not be modified further by any user.|
|labels|否|Map<String,String>|Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels|
|name|否|String|Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|namespace|否|String|Namespace defines the space within each name must be unique. An empty namespace is equivalent to the "default" namespace, but "default" is the canonical representation. Not all objects are required to be scoped to a namespace - the value of this field for those objects will be empty.Must be a DNS_LABEL. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/namespaces|
|ownerReferences|否|Array of io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference_v2 objects|List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller.|
|resourceVersion|否|String|An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources.Populated by the system. Read-only. Value must be treated as opaque by clients and . More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|否|String|SelfLink is a URL representing this object. Populated by the system. Read-only.|
|uid|否|String|UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations.Populated by the system. Read-only. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 6**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers\_v3

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|pending|是|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer_v2 objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|否|io.k8s.apimachinery.pkg.apis.meta.v1.Status_v3 object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 7**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer\_v2

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|name|是|String|name of the process that is responsible for initializing this object.|


**表 8**  io.k8s.apimachinery.pkg.apis.meta.v1.Status\_v3

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|apiVersion|否|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|code|否|Integer|Suggested HTTP return code for this status, 0 if not set.|
|details|否|io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails_v3 object|Extended data associated with the reason. Each reason may define its own extended details. This field is optional and the data returned is not guaranteed to conform to any schema except that defined by the reason type.|
|kind|否|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|message|否|String|A human-readable description of the status of this operation.|
|metadata|否|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta_v2 object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|reason|否|String|A machine-readable description of why this operation is in the "Failure" status. If this value is empty there is no information available. A Reason clarifies an HTTP status code but does not override it.|
|status|否|String|Status of the operation. One of: "Success" or "Failure". More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|


**表 9**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|causes|否|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|否|String|The group attribute of the resource associated with the status StatusReason.|
|kind|否|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|否|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|否|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|否|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 10**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|field|否|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|否|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|否|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 11**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|continue|否|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|否|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|否|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 12**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|apiVersion|是|String|API version of the referent.|
|blockOwnerDeletion|否|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|否|Boolean|If true, this reference points to the managing controller.|
|kind|是|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|是|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|是|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 13**  io.k8s.api.core.v1.PersistentVolumeClaimSpec

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|accessModes|否|Array of strings|AccessModes contains the desired access modes the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|resources|否|io.k8s.api.core.v1.ResourceRequirements object|Resources represents the minimum resources the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#resources|
|selector|否|io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector object|A label query over volumes to consider for binding.|
|storageClassName|否|String|Name of the StorageClass required by the claim. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#class-1|
|volumeMode|否|String|volumeMode defines what type of volume is required by the claim. Value of Filesystem is implied when not included in claim spec. This is an alpha feature and may change in the future.|
|volumeName|否|String|VolumeName is the binding reference to the PersistentVolume backing this claim.|


**表 14**  io.k8s.api.core.v1.ResourceRequirements

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|limits|否|Map<String,String>|Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|
|requests|否|Map<String,String>|Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|


**表 15**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|matchExpressions|否|Array of io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement objects|matchExpressions is a list of label selector requirements. The requirements are ANDed.|
|matchLabels|否|Map<String,String>|matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.|


**表 16**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|key|是|String|key is the label key that the selector applies to.|
|operator|是|String|operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.|
|values|否|Array of strings|values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.|


**表 17**  io.k8s.api.core.v1.PersistentVolumeClaimStatus

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|accessModes|否|Array of strings|AccessModes contains the actual access modes the volume backing the PVC has. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|capacity|否|Map<String,String>|Represents the actual resources of the underlying volume.|
|conditions|否|Array of io.k8s.api.core.v1.PersistentVolumeClaimCondition objects|Current Condition of persistent volume claim. If underlying persistent volume is being resized then the Condition will be set to 'ResizeStarted'.|
|phase|否|String|Phase represents the current phase of PersistentVolumeClaim.|


**表 18**  io.k8s.api.core.v1.PersistentVolumeClaimCondition

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|lastProbeTime|否|String|Last time we probed the condition.|
|lastTransitionTime|否|String|Last time the condition transitioned from one status to another.|
|message|否|String|Human-readable message indicating details about last transition.|
|reason|否|String|Unique, this should be a short, machine understandable string that gives the reason for condition's last transition. If it reports "ResizeStarted" that means the underlying persistent volume is being resized.|
|status|是|String|status is the status of the condition.|
|type|是|String|type is the type of the condition.|


## 响应参数

**状态码： 200**

**表 19**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|io.k8s.api.core.v1.PersistentVolumeClaimSpec object|Spec defines the desired characteristics of a volume requested by a pod author. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|
|status|io.k8s.api.core.v1.PersistentVolumeClaimStatus object|Status represents the current information/status of a persistent volume claim. Read-only. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|


**表 20**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta\_v3

|参数|参数类型|描述|
|--|--|--|
|annotations|Map<String,String>|Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations|
|clusterName|String|The name of the cluster which the object belongs to. This is used to distinguish resources with same name and namespace in different clusters. This field is not set anywhere right now and apiserver is going to ignore it if set in create or update request.|
|creationTimestamp|String|CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is represented in RFC3339 form and is in UTC.Populated by the system. Read-only. Null for lists. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|deletionGracePeriodSeconds|Long|Number of seconds allowed for this object to gracefully terminate before it will be removed from the system. Only set when deletionTimestamp is also set. May only be shortened. Read-only.|
|deletionTimestamp|String|DeletionTimestamp is RFC 3339 date and time at which this resource will be deleted. This field is set by the server when a graceful deletion is requested by the user, and is not directly settable by a client. The resource is expected to be deleted (no longer visible from resource lists, and not reachable by name) after the time in this field, once the finalizers list is empty. As long as the finalizers list contains items, deletion is blocked. Once the deletionTimestamp is set, this value may not be unset or be set further into the future, although it may be shortened or the resource may be deleted prior to this time. For example, a user may request that a pod is deleted in 30 seconds. The Kubelet will react by sending a graceful termination signal to the containers in the pod. After that 30 seconds, the Kubelet will send a hard termination signal (SIGKILL) to the container and after cleanup, remove the pod from the API. In the presence of network partitions, this object may still exist after this timestamp, until an administrator or automated process can determine the resource is fully terminated. If not set, graceful deletion of the object has not been requested.Populated by the system when a graceful deletion is requested. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|enable|Boolean|Enable identify whether the resource is available|
|finalizers|Array of strings|Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed.|
|generateName|String|GenerateName is an optional prefix, used by the server, to generate a unique name ONLY IF the Name field has not been provided. If this field is used, the name returned to the client will be different than the name passed. This value will also be combined with a unique suffix. The provided value has the same validation rules as the Name field, and may be truncated by the length of the suffix required to make the value unique on the server.If this field is specified and the generated name exists, the server will NOT return a 409 - instead, it will either return 201 Created or 500 with Reason ServerTimeout indicating a unique name could not be found in the time allotted, and the client should retry (optionally after the time indicated in the Retry-After header).Applied only if Name is not specified. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#idempotency|
|generation|Long|A sequence number representing a specific generation of the desired state. Populated by the system. Read-only.|
|initializers|io.k8s.apimachinery.pkg.apis.meta.v1.Initializers_v3 object|An initializer is a controller which enforces some system invariant at object creation time. This field is a list of initializers that have not yet acted on this object. If nil or empty, this object has been completely initialized. Otherwise, the object is considered uninitialized and is hidden (in list/watch and get calls) from clients that haven't explicitly asked to observe uninitialized objects.When an object is created, the system will populate this list with the current set of initializers. Only privileged users may set or modify this list. Once it is empty, it may not be modified further by any user.|
|labels|Map<String,String>|Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels|
|name|String|Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|namespace|String|Namespace defines the space within each name must be unique. An empty namespace is equivalent to the "default" namespace, but "default" is the canonical representation. Not all objects are required to be scoped to a namespace - the value of this field for those objects will be empty.Must be a DNS_LABEL. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/namespaces|
|ownerReferences|Array of io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference_v2 objects|List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller.|
|resourceVersion|String|An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources.Populated by the system. Read-only. Value must be treated as opaque by clients and . More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|SelfLink is a URL representing this object. Populated by the system. Read-only.|
|uid|String|UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations.Populated by the system. Read-only. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 21**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers\_v3

|参数|参数类型|描述|
|--|--|--|
|pending|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer_v2 objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|io.k8s.apimachinery.pkg.apis.meta.v1.Status_v3 object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 22**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer\_v2

|参数|参数类型|描述|
|--|--|--|
|name|String|name of the process that is responsible for initializing this object.|


**表 23**  io.k8s.apimachinery.pkg.apis.meta.v1.Status\_v3

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|code|Integer|Suggested HTTP return code for this status, 0 if not set.|
|details|io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails_v3 object|Extended data associated with the reason. Each reason may define its own extended details. This field is optional and the data returned is not guaranteed to conform to any schema except that defined by the reason type.|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|message|String|A human-readable description of the status of this operation.|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta_v2 object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|reason|String|A machine-readable description of why this operation is in the "Failure" status. If this value is empty there is no information available. A Reason clarifies an HTTP status code but does not override it.|
|status|String|Status of the operation. One of: "Success" or "Failure". More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|


**表 24**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 25**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 26**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 27**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 28**  io.k8s.api.core.v1.PersistentVolumeClaimSpec

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the desired access modes the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|resources|io.k8s.api.core.v1.ResourceRequirements object|Resources represents the minimum resources the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#resources|
|selector|io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector object|A label query over volumes to consider for binding.|
|storageClassName|String|Name of the StorageClass required by the claim. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#class-1|
|volumeMode|String|volumeMode defines what type of volume is required by the claim. Value of Filesystem is implied when not included in claim spec. This is an alpha feature and may change in the future.|
|volumeName|String|VolumeName is the binding reference to the PersistentVolume backing this claim.|


**表 29**  io.k8s.api.core.v1.ResourceRequirements

|参数|参数类型|描述|
|--|--|--|
|limits|Map<String,String>|Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|
|requests|Map<String,String>|Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|


**表 30**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector

|参数|参数类型|描述|
|--|--|--|
|matchExpressions|Array of io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement objects|matchExpressions is a list of label selector requirements. The requirements are ANDed.|
|matchLabels|Map<String,String>|matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.|


**表 31**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement

|参数|参数类型|描述|
|--|--|--|
|key|String|key is the label key that the selector applies to.|
|operator|String|operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.|
|values|Array of strings|values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.|


**表 32**  io.k8s.api.core.v1.PersistentVolumeClaimStatus

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the actual access modes the volume backing the PVC has. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|capacity|Map<String,String>|Represents the actual resources of the underlying volume.|
|conditions|Array of io.k8s.api.core.v1.PersistentVolumeClaimCondition objects|Current Condition of persistent volume claim. If underlying persistent volume is being resized then the Condition will be set to 'ResizeStarted'.|
|phase|String|Phase represents the current phase of PersistentVolumeClaim.|


**表 33**  io.k8s.api.core.v1.PersistentVolumeClaimCondition

|参数|参数类型|描述|
|--|--|--|
|lastProbeTime|String|Last time we probed the condition.|
|lastTransitionTime|String|Last time the condition transitioned from one status to another.|
|message|String|Human-readable message indicating details about last transition.|
|reason|String|Unique, this should be a short, machine understandable string that gives the reason for condition's last transition. If it reports "ResizeStarted" that means the underlying persistent volume is being resized.|
|status|String|status is the status of the condition.|
|type|String|type is the type of the condition.|


**状态码： 201**

**表 34**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|io.k8s.api.core.v1.PersistentVolumeClaimSpec object|Spec defines the desired characteristics of a volume requested by a pod author. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|
|status|io.k8s.api.core.v1.PersistentVolumeClaimStatus object|Status represents the current information/status of a persistent volume claim. Read-only. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|


**表 35**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta\_v3

|参数|参数类型|描述|
|--|--|--|
|annotations|Map<String,String>|Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations|
|clusterName|String|The name of the cluster which the object belongs to. This is used to distinguish resources with same name and namespace in different clusters. This field is not set anywhere right now and apiserver is going to ignore it if set in create or update request.|
|creationTimestamp|String|CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is represented in RFC3339 form and is in UTC.Populated by the system. Read-only. Null for lists. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|deletionGracePeriodSeconds|Long|Number of seconds allowed for this object to gracefully terminate before it will be removed from the system. Only set when deletionTimestamp is also set. May only be shortened. Read-only.|
|deletionTimestamp|String|DeletionTimestamp is RFC 3339 date and time at which this resource will be deleted. This field is set by the server when a graceful deletion is requested by the user, and is not directly settable by a client. The resource is expected to be deleted (no longer visible from resource lists, and not reachable by name) after the time in this field, once the finalizers list is empty. As long as the finalizers list contains items, deletion is blocked. Once the deletionTimestamp is set, this value may not be unset or be set further into the future, although it may be shortened or the resource may be deleted prior to this time. For example, a user may request that a pod is deleted in 30 seconds. The Kubelet will react by sending a graceful termination signal to the containers in the pod. After that 30 seconds, the Kubelet will send a hard termination signal (SIGKILL) to the container and after cleanup, remove the pod from the API. In the presence of network partitions, this object may still exist after this timestamp, until an administrator or automated process can determine the resource is fully terminated. If not set, graceful deletion of the object has not been requested.Populated by the system when a graceful deletion is requested. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|enable|Boolean|Enable identify whether the resource is available|
|finalizers|Array of strings|Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed.|
|generateName|String|GenerateName is an optional prefix, used by the server, to generate a unique name ONLY IF the Name field has not been provided. If this field is used, the name returned to the client will be different than the name passed. This value will also be combined with a unique suffix. The provided value has the same validation rules as the Name field, and may be truncated by the length of the suffix required to make the value unique on the server.If this field is specified and the generated name exists, the server will NOT return a 409 - instead, it will either return 201 Created or 500 with Reason ServerTimeout indicating a unique name could not be found in the time allotted, and the client should retry (optionally after the time indicated in the Retry-After header).Applied only if Name is not specified. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#idempotency|
|generation|Long|A sequence number representing a specific generation of the desired state. Populated by the system. Read-only.|
|initializers|io.k8s.apimachinery.pkg.apis.meta.v1.Initializers_v3 object|An initializer is a controller which enforces some system invariant at object creation time. This field is a list of initializers that have not yet acted on this object. If nil or empty, this object has been completely initialized. Otherwise, the object is considered uninitialized and is hidden (in list/watch and get calls) from clients that haven't explicitly asked to observe uninitialized objects.When an object is created, the system will populate this list with the current set of initializers. Only privileged users may set or modify this list. Once it is empty, it may not be modified further by any user.|
|labels|Map<String,String>|Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels|
|name|String|Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|namespace|String|Namespace defines the space within each name must be unique. An empty namespace is equivalent to the "default" namespace, but "default" is the canonical representation. Not all objects are required to be scoped to a namespace - the value of this field for those objects will be empty.Must be a DNS_LABEL. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/namespaces|
|ownerReferences|Array of io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference_v2 objects|List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller.|
|resourceVersion|String|An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources.Populated by the system. Read-only. Value must be treated as opaque by clients and . More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|SelfLink is a URL representing this object. Populated by the system. Read-only.|
|uid|String|UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations.Populated by the system. Read-only. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 36**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers\_v3

|参数|参数类型|描述|
|--|--|--|
|pending|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer_v2 objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|io.k8s.apimachinery.pkg.apis.meta.v1.Status_v3 object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 37**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer\_v2

|参数|参数类型|描述|
|--|--|--|
|name|String|name of the process that is responsible for initializing this object.|


**表 38**  io.k8s.apimachinery.pkg.apis.meta.v1.Status\_v3

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|code|Integer|Suggested HTTP return code for this status, 0 if not set.|
|details|io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails_v3 object|Extended data associated with the reason. Each reason may define its own extended details. This field is optional and the data returned is not guaranteed to conform to any schema except that defined by the reason type.|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|message|String|A human-readable description of the status of this operation.|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta_v2 object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|reason|String|A machine-readable description of why this operation is in the "Failure" status. If this value is empty there is no information available. A Reason clarifies an HTTP status code but does not override it.|
|status|String|Status of the operation. One of: "Success" or "Failure". More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|


**表 39**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 40**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 41**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 42**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 43**  io.k8s.api.core.v1.PersistentVolumeClaimSpec

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the desired access modes the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|resources|io.k8s.api.core.v1.ResourceRequirements object|Resources represents the minimum resources the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#resources|
|selector|io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector object|A label query over volumes to consider for binding.|
|storageClassName|String|Name of the StorageClass required by the claim. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#class-1|
|volumeMode|String|volumeMode defines what type of volume is required by the claim. Value of Filesystem is implied when not included in claim spec. This is an alpha feature and may change in the future.|
|volumeName|String|VolumeName is the binding reference to the PersistentVolume backing this claim.|


**表 44**  io.k8s.api.core.v1.ResourceRequirements

|参数|参数类型|描述|
|--|--|--|
|limits|Map<String,String>|Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|
|requests|Map<String,String>|Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|


**表 45**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector

|参数|参数类型|描述|
|--|--|--|
|matchExpressions|Array of io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement objects|matchExpressions is a list of label selector requirements. The requirements are ANDed.|
|matchLabels|Map<String,String>|matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.|


**表 46**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement

|参数|参数类型|描述|
|--|--|--|
|key|String|key is the label key that the selector applies to.|
|operator|String|operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.|
|values|Array of strings|values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.|


**表 47**  io.k8s.api.core.v1.PersistentVolumeClaimStatus

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the actual access modes the volume backing the PVC has. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|capacity|Map<String,String>|Represents the actual resources of the underlying volume.|
|conditions|Array of io.k8s.api.core.v1.PersistentVolumeClaimCondition objects|Current Condition of persistent volume claim. If underlying persistent volume is being resized then the Condition will be set to 'ResizeStarted'.|
|phase|String|Phase represents the current phase of PersistentVolumeClaim.|


**表 48**  io.k8s.api.core.v1.PersistentVolumeClaimCondition

|参数|参数类型|描述|
|--|--|--|
|lastProbeTime|String|Last time we probed the condition.|
|lastTransitionTime|String|Last time the condition transitioned from one status to another.|
|message|String|Human-readable message indicating details about last transition.|
|reason|String|Unique, this should be a short, machine understandable string that gives the reason for condition's last transition. If it reports "ResizeStarted" that means the underlying persistent volume is being resized.|
|status|String|status is the status of the condition.|
|type|String|type is the type of the condition.|


**状态码： 202**

**表 49**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|io.k8s.api.core.v1.PersistentVolumeClaimSpec object|Spec defines the desired characteristics of a volume requested by a pod author. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|
|status|io.k8s.api.core.v1.PersistentVolumeClaimStatus object|Status represents the current information/status of a persistent volume claim. Read-only. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|


**表 50**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta\_v3

|参数|参数类型|描述|
|--|--|--|
|annotations|Map<String,String>|Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations|
|clusterName|String|The name of the cluster which the object belongs to. This is used to distinguish resources with same name and namespace in different clusters. This field is not set anywhere right now and apiserver is going to ignore it if set in create or update request.|
|creationTimestamp|String|CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is represented in RFC3339 form and is in UTC.Populated by the system. Read-only. Null for lists. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|deletionGracePeriodSeconds|Long|Number of seconds allowed for this object to gracefully terminate before it will be removed from the system. Only set when deletionTimestamp is also set. May only be shortened. Read-only.|
|deletionTimestamp|String|DeletionTimestamp is RFC 3339 date and time at which this resource will be deleted. This field is set by the server when a graceful deletion is requested by the user, and is not directly settable by a client. The resource is expected to be deleted (no longer visible from resource lists, and not reachable by name) after the time in this field, once the finalizers list is empty. As long as the finalizers list contains items, deletion is blocked. Once the deletionTimestamp is set, this value may not be unset or be set further into the future, although it may be shortened or the resource may be deleted prior to this time. For example, a user may request that a pod is deleted in 30 seconds. The Kubelet will react by sending a graceful termination signal to the containers in the pod. After that 30 seconds, the Kubelet will send a hard termination signal (SIGKILL) to the container and after cleanup, remove the pod from the API. In the presence of network partitions, this object may still exist after this timestamp, until an administrator or automated process can determine the resource is fully terminated. If not set, graceful deletion of the object has not been requested.Populated by the system when a graceful deletion is requested. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|enable|Boolean|Enable identify whether the resource is available|
|finalizers|Array of strings|Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed.|
|generateName|String|GenerateName is an optional prefix, used by the server, to generate a unique name ONLY IF the Name field has not been provided. If this field is used, the name returned to the client will be different than the name passed. This value will also be combined with a unique suffix. The provided value has the same validation rules as the Name field, and may be truncated by the length of the suffix required to make the value unique on the server.If this field is specified and the generated name exists, the server will NOT return a 409 - instead, it will either return 201 Created or 500 with Reason ServerTimeout indicating a unique name could not be found in the time allotted, and the client should retry (optionally after the time indicated in the Retry-After header).Applied only if Name is not specified. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#idempotency|
|generation|Long|A sequence number representing a specific generation of the desired state. Populated by the system. Read-only.|
|initializers|io.k8s.apimachinery.pkg.apis.meta.v1.Initializers_v3 object|An initializer is a controller which enforces some system invariant at object creation time. This field is a list of initializers that have not yet acted on this object. If nil or empty, this object has been completely initialized. Otherwise, the object is considered uninitialized and is hidden (in list/watch and get calls) from clients that haven't explicitly asked to observe uninitialized objects.When an object is created, the system will populate this list with the current set of initializers. Only privileged users may set or modify this list. Once it is empty, it may not be modified further by any user.|
|labels|Map<String,String>|Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels|
|name|String|Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|namespace|String|Namespace defines the space within each name must be unique. An empty namespace is equivalent to the "default" namespace, but "default" is the canonical representation. Not all objects are required to be scoped to a namespace - the value of this field for those objects will be empty.Must be a DNS_LABEL. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/namespaces|
|ownerReferences|Array of io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference_v2 objects|List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller.|
|resourceVersion|String|An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources.Populated by the system. Read-only. Value must be treated as opaque by clients and . More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|SelfLink is a URL representing this object. Populated by the system. Read-only.|
|uid|String|UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations.Populated by the system. Read-only. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 51**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers\_v3

|参数|参数类型|描述|
|--|--|--|
|pending|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer_v2 objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|io.k8s.apimachinery.pkg.apis.meta.v1.Status_v3 object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 52**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer\_v2

|参数|参数类型|描述|
|--|--|--|
|name|String|name of the process that is responsible for initializing this object.|


**表 53**  io.k8s.apimachinery.pkg.apis.meta.v1.Status\_v3

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|code|Integer|Suggested HTTP return code for this status, 0 if not set.|
|details|io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails_v3 object|Extended data associated with the reason. Each reason may define its own extended details. This field is optional and the data returned is not guaranteed to conform to any schema except that defined by the reason type.|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|message|String|A human-readable description of the status of this operation.|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta_v2 object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|reason|String|A machine-readable description of why this operation is in the "Failure" status. If this value is empty there is no information available. A Reason clarifies an HTTP status code but does not override it.|
|status|String|Status of the operation. One of: "Success" or "Failure". More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|


**表 54**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 55**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 56**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 57**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 58**  io.k8s.api.core.v1.PersistentVolumeClaimSpec

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the desired access modes the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|resources|io.k8s.api.core.v1.ResourceRequirements object|Resources represents the minimum resources the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#resources|
|selector|io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector object|A label query over volumes to consider for binding.|
|storageClassName|String|Name of the StorageClass required by the claim. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#class-1|
|volumeMode|String|volumeMode defines what type of volume is required by the claim. Value of Filesystem is implied when not included in claim spec. This is an alpha feature and may change in the future.|
|volumeName|String|VolumeName is the binding reference to the PersistentVolume backing this claim.|


**表 59**  io.k8s.api.core.v1.ResourceRequirements

|参数|参数类型|描述|
|--|--|--|
|limits|Map<String,String>|Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|
|requests|Map<String,String>|Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|


**表 60**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector

|参数|参数类型|描述|
|--|--|--|
|matchExpressions|Array of io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement objects|matchExpressions is a list of label selector requirements. The requirements are ANDed.|
|matchLabels|Map<String,String>|matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.|


**表 61**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement

|参数|参数类型|描述|
|--|--|--|
|key|String|key is the label key that the selector applies to.|
|operator|String|operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.|
|values|Array of strings|values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.|


**表 62**  io.k8s.api.core.v1.PersistentVolumeClaimStatus

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the actual access modes the volume backing the PVC has. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|capacity|Map<String,String>|Represents the actual resources of the underlying volume.|
|conditions|Array of io.k8s.api.core.v1.PersistentVolumeClaimCondition objects|Current Condition of persistent volume claim. If underlying persistent volume is being resized then the Condition will be set to 'ResizeStarted'.|
|phase|String|Phase represents the current phase of PersistentVolumeClaim.|


**表 63**  io.k8s.api.core.v1.PersistentVolumeClaimCondition

|参数|参数类型|描述|
|--|--|--|
|lastProbeTime|String|Last time we probed the condition.|
|lastTransitionTime|String|Last time the condition transitioned from one status to another.|
|message|String|Human-readable message indicating details about last transition.|
|reason|String|Unique, this should be a short, machine understandable string that gives the reason for condition's last transition. If it reports "ResizeStarted" that means the underlying persistent volume is being resized.|
|status|String|status is the status of the condition.|
|type|String|type is the type of the condition.|


## 请求示例

-   创建一个大小为10G的加密云硬盘，类型为sata

    ```
    {
      "apiVersion" : "v1",
      "kind" : "PersistentVolumeClaim",
      "metadata" : {
        "annotations" : {
          "paas.storage.io/cryptKeyId" : "ee9b610c-e356-11e9-aadc-d0efc1b3bb6b",
          "volume.beta.kubernetes.io/storage-class" : "sata"
        },
        "name" : "pvc-test",
        "namespace" : "test-namespace"
      },
      "spec" : {
        "accessModes" : [ "ReadWriteMany" ],
        "resources" : {
          "requests" : {
            "storage" : "10Gi"
          }
        }
      }
    }
    ```

-   创建一个大小为10G的加密文件存储卷

    ```
    {
      "apiVersion" : "v1",
      "kind" : "PersistentVolumeClaim",
      "metadata" : {
        "annotations" : {
          "paas.storage.io/cryptAlias" : "sfs/default",
          "paas.storage.io/cryptDomainId" : "d6912480-c3d6-4e9e-8c70-38afeea434c3",
          "paas.storage.io/cryptKeyId" : "ee9b610c-e356-11e9-aadc-d0efc1b3bb6b",
          "volume.beta.kubernetes.io/storage-class" : "nfs-rw"
        },
        "name" : "pvc-test",
        "namespace" : "test-namespace"
      },
      "spec" : {
        "accessModes" : [ "ReadWriteMany" ],
        "resources" : {
          "requests" : {
            "storage" : "10Gi"
          }
        }
      }
    }
    ```


## 响应示例

**状态码： 200**

OK

```
{
  "apiVersion" : "v1",
  "kind" : "PersistentVolumeClaim",
  "metadata" : {
    "annotations" : {
      "paas.storage.io/cryptKeyId" : "ee9b610c-e356-11e9-aadc-d0efc1b3bb6b",
      "pv.kubernetes.io/bind-completed" : "yes",
      "pv.kubernetes.io/bound-by-controller" : "yes",
      "volume.beta.kubernetes.io/storage-provisioner" : "flexvolume-huawei.com/fuxivol"
    },
    "creationTimestamp" : "2018-11-24T07:48:35Z",
    "finalizers" : [ "kubernetes.io/pvc-protection" ],
    "labels" : {
      "app" : "evs"
    },
    "name" : "pvc-test",
    "namespace" : "test-namespace",
    "resourceVersion" : "28156856",
    "selfLink" : "/api/v1/namespaces/ns-test/persistentvolumeclaims/pvc-test",
    "uid" : "58d15f3e-efbd-11e8-8950-501d934409f3"
  },
  "spec" : {
    "accessModes" : [ "ReadWriteMany" ],
    "resources" : {
      "requests" : {
        "storage" : "10Gi"
      }
    },
    "storageClassName" : "sata",
    "volumeName" : "pvc-58d15f3e-efbd-11e8-8950-501d934409f3"
  },
  "status" : {
    "accessModes" : [ "ReadWriteMany" ],
    "capacity" : {
      "storage" : "10Gi"
    },
    "phase" : "Bound"
  }
}
```

## 状态码

|状态码|描述|
|--|--|
|200|OK|
|201|Created|
|202|Accepted|
|400|BadRequest|
|401|Unauthorized|
|403|Forbidden|
|404|NotFound|
|405|MethodNotAllowed|
|406|NotAcceptable|
|409|AlreadyExists|
|415|UnsupportedMediaType|
|422|Invalid|
|429|TooManyRequests|
|500|InternalError|
|503|ServiceUnavailable|
|504|ServerTimeout|


