# 替换Volcano Job<a name="replaceBatchVolcanoShV1alpha1NamespacedJob"></a>

## 功能介绍

替换Volcano Job。

The following fields can be updated:

-   metadata.labels

-   metadata.generateName

-   metadata.annotations

-   spec.template

-   spec.replicas


## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=CCI&api=replaceBatchVolcanoShV1alpha1NamespacedJob)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

PUT /apis/batch.volcano.sh/v1alpha1/namespaces/\{namespace\}/jobs/\{name\}

**表 1**  路径参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|name|是|String|name of the Volcano Job|
|namespace|是|String|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|dryRun|否|String|When present, indicates that modifications should not be persisted. An invalid or unrecognized dryRun directive will result in an error response and no further processing of the request. Valid values are: - All: all dry run stages will be processed|
|fieldManager|否|String|fieldManager is a name associated with the actor or entity that is making these changes. The value must be less than or 128 characters long, and only contain printable characters, as defined by https://golang.org/pkg/unicode/#IsPrint.|
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
|metadata|否|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|否|spec object|Specification of the desired behavior of a cron job, including the minAvailable|
|status|否|status object|Current status of Job|


**表 5**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|annotations|否|Map<String,String>|Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations|
|clusterName|否|String|The name of the cluster which the object belongs to. This is used to distinguish resources with same name and namespace in different clusters. This field is not set anywhere right now and apiserver is going to ignore it if set in create or update request.|
|creationTimestamp|否|String|CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is represented in RFC3339 form and is in UTC.Populated by the system. Read-only. Null for lists. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|deletionGracePeriodSeconds|否|Long|Number of seconds allowed for this object to gracefully terminate before it will be removed from the system. Only set when deletionTimestamp is also set. May only be shortened. Read-only.|
|deletionTimestamp|否|String|DeletionTimestamp is RFC 3339 date and time at which this resource will be deleted. This field is set by the server when a graceful deletion is requested by the user, and is not directly settable by a client. The resource is expected to be deleted (no longer visible from resource lists, and not reachable by name) after the time in this field, once the finalizers list is empty. As long as the finalizers list contains items, deletion is blocked. Once the deletionTimestamp is set, this value may not be unset or be set further into the future, although it may be shortened or the resource may be deleted prior to this time. For example, a user may request that a pod is deleted in 30 seconds. The Kubelet will react by sending a graceful termination signal to the containers in the pod. After that 30 seconds, the Kubelet will send a hard termination signal (SIGKILL) to the container and after cleanup, remove the pod from the API. In the presence of network partitions, this object may still exist after this timestamp, until an administrator or automated process can determine the resource is fully terminated. If not set, graceful deletion of the object has not been requested.Populated by the system when a graceful deletion is requested. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|finalizers|否|Array of strings|Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed.|
|generateName|否|String|GenerateName is an optional prefix, used by the server, to generate a unique name ONLY IF the Name field has not been provided. If this field is used, the name returned to the client will be different than the name passed. This value will also be combined with a unique suffix. The provided value has the same validation rules as the Name field, and may be truncated by the length of the suffix required to make the value unique on the server.If this field is specified and the generated name exists, the server will NOT return a 409 - instead, it will either return 201 Created or 500 with Reason ServerTimeout indicating a unique name could not be found in the time allotted, and the client should retry (optionally after the time indicated in the Retry-After header).Applied only if Name is not specified. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#idempotency|
|generation|否|Long|A sequence number representing a specific generation of the desired state. Populated by the system. Read-only.|
|initializers|否|io.k8s.apimachinery.pkg.apis.meta.v1.Initializers object|An initializer is a controller which enforces some system invariant at object creation time. This field is a list of initializers that have not yet acted on this object. If nil or empty, this object has been completely initialized. Otherwise, the object is considered uninitialized and is hidden (in list/watch and get calls) from clients that haven't explicitly asked to observe uninitialized objects.When an object is created, the system will populate this list with the current set of initializers. Only privileged users may set or modify this list. Once it is empty, it may not be modified further by any user.DEPRECATED - initializers are an alpha field and will be removed in v1.15.|
|labels|否|Map<String,String>|Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels|
|managedFields|否|Array of io.k8s.apimachinery.pkg.apis.meta.v1.ManagedFieldsEntry objects|ManagedFields maps workflow-id and version to the set of fields that are managed by that workflow. This is mostly for internal housekeeping, and users typically shouldn't need to set or understand this field. A workflow can be the user's name, a controller's name, or the name of a specific apply path like "ci-cd". The set of fields is always in the version that the workflow used when modifying the object.This field is alpha and can be changed or removed without notice.|
|name|否|String|Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|namespace|否|String|Namespace defines the space within each name must be unique. An empty namespace is equivalent to the "default" namespace, but "default" is the canonical representation. Not all objects are required to be scoped to a namespace - the value of this field for those objects will be empty.Must be a DNS_LABEL. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/namespaces|
|ownerReferences|否|Array of io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference objects|List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller.|
|resourceVersion|否|String|An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources.Populated by the system. Read-only. Value must be treated as opaque by clients and . More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|否|String|SelfLink is a URL representing this object. Populated by the system. Read-only.|
|uid|否|String|UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations.Populated by the system. Read-only. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 6**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|pending|是|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|否|io.k8s.apimachinery.pkg.apis.meta.v1.Status object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 7**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|name|是|String|name of the process that is responsible for initializing this object.|


**表 8**  io.k8s.apimachinery.pkg.apis.meta.v1.Status

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|apiVersion|否|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|code|否|Integer|Suggested HTTP return code for this status, 0 if not set.|
|details|否|io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails object|Extended data associated with the reason. Each reason may define its own extended details. This field is optional and the data returned is not guaranteed to conform to any schema except that defined by the reason type.|
|kind|否|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|message|否|String|A human-readable description of the status of this operation.|
|metadata|否|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|reason|否|String|A machine-readable description of why this operation is in the "Failure" status. If this value is empty there is no information available. A Reason clarifies an HTTP status code but does not override it.|
|status|否|String|Status of the operation. One of: "Success" or "Failure". More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|


**表 9**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|causes|否|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|否|String|The group attribute of the resource associated with the status StatusReason.|
|kind|否|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|否|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|否|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|否|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 10**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|field|否|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|否|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|否|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 11**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|continue|否|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a consistent list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response, unless you have received this token from an error message.|
|resourceVersion|否|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|否|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 12**  io.k8s.apimachinery.pkg.apis.meta.v1.ManagedFieldsEntry

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|apiVersion|否|String|APIVersion defines the version of this resource that this field set applies to. The format is "group/version" just like the top-level APIVersion field. It is necessary to track the version of a field set because it cannot be automatically converted.|
|fields|否|Object|Fields identifies a set of fields.|
|manager|否|String|Manager is an identifier of the workflow managing these fields.|
|operation|否|String|Operation is the type of operation which lead to this ManagedFieldsEntry being created. The only valid values for this field are 'Apply' and 'Update'.|
|time|否|String|Time is timestamp of when these fields were set. It should always be empty if Operation is 'Apply'|


**表 13**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|apiVersion|是|String|API version of the referent.|
|blockOwnerDeletion|否|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|否|Boolean|If true, this reference points to the managing controller.|
|kind|是|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|是|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|是|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 14**  spec

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|maxRetry|否|Integer|The limit for retrying submiting job, default is 3|
|minAvailable|否|Integer|The minimal available pods to run for this Job|
|plugins|否|Object|Enabled task plugins when creating job.|
|policies|否|Array of policies objects|Specifies the default lifecycle of tasks|
|queue|否|String|The name of the queue on which job should been created|
|schedulerName|否|String|SchedulerName is the default value of *tasks.template.spec.schedulerName*.|
|tasks|否|Array of tasks objects|Tasks specifies the task specification of Job|
|volumes|否|Array of volumes objects|The volumes for Job|


**表 15**  policies

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|action|否|String|The action that will be taken to the PodGroup according to Event. One of "Restart", "None". Default to None.|
|event|否|String|The Event recorded by scheduler; the controller takes actions according to this Event.|
|timeout|否|Object|Timeout is the grace period for controller to take actions. Default to nil (take action immediately).|


**表 16**  tasks

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|name|否|String|Name specifies the name of tasks|
|policies|否|Array of policies objects|Specifies the lifecycle of task|
|replicas|否|Integer|Replicas specifies the replicas of this TaskSpec in Job|
|template|否|Object|Specifies the pod that will be created for this TaskSpec when executing a Job|


**表 17**  policies

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|action|否|String|The action that will be taken to the PodGroup according to Event. One of "Restart", "None". Default to None.|
|event|否|String|The Event recorded by scheduler; the controller takes actions according to this Event.|
|timeout|否|Object|Timeout is the grace period for controller to take actions. Default to nil (take action immediately).|


**表 18**  volumes

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|mountPath|是|String|Path within the container at which the volume should be mounted. Must not contain ':'.|
|volumeClaim|否|io.k8s.api.core.v1.PersistentVolumeClaim object|VolumeClaim defines the PVC used by the VolumeMount.|
|volumeClaimName|否|String|The name of the volume claim.|


**表 19**  io.k8s.api.core.v1.PersistentVolumeClaim

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|apiVersion|否|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|否|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|否|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|否|io.k8s.api.core.v1.PersistentVolumeClaimSpec object|Spec defines the desired characteristics of a volume requested by a pod author. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|
|status|否|io.k8s.api.core.v1.PersistentVolumeClaimStatus object|Status represents the current information/status of a persistent volume claim. Read-only. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|


**表 20**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta\_v3

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


**表 21**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers\_v3

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|pending|是|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer_v2 objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|否|io.k8s.apimachinery.pkg.apis.meta.v1.Status_v3 object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 22**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer\_v2

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|name|是|String|name of the process that is responsible for initializing this object.|


**表 23**  io.k8s.apimachinery.pkg.apis.meta.v1.Status\_v3

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


**表 24**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|causes|否|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|否|String|The group attribute of the resource associated with the status StatusReason.|
|kind|否|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|否|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|否|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|否|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 25**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|field|否|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|否|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|否|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 26**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|continue|否|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|否|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|否|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 27**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|apiVersion|是|String|API version of the referent.|
|blockOwnerDeletion|否|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|否|Boolean|If true, this reference points to the managing controller.|
|kind|是|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|是|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|是|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 28**  io.k8s.api.core.v1.PersistentVolumeClaimSpec

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|accessModes|否|Array of strings|AccessModes contains the desired access modes the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|resources|否|io.k8s.api.core.v1.ResourceRequirements object|Resources represents the minimum resources the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#resources|
|selector|否|io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector object|A label query over volumes to consider for binding.|
|storageClassName|否|String|Name of the StorageClass required by the claim. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#class-1|
|volumeMode|否|String|volumeMode defines what type of volume is required by the claim. Value of Filesystem is implied when not included in claim spec. This is an alpha feature and may change in the future.|
|volumeName|否|String|VolumeName is the binding reference to the PersistentVolume backing this claim.|


**表 29**  io.k8s.api.core.v1.ResourceRequirements

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|limits|否|Map<String,String>|Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|
|requests|否|Map<String,String>|Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|


**表 30**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|matchExpressions|否|Array of io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement objects|matchExpressions is a list of label selector requirements. The requirements are ANDed.|
|matchLabels|否|Map<String,String>|matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.|


**表 31**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|key|是|String|key is the label key that the selector applies to.|
|operator|是|String|operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.|
|values|否|Array of strings|values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.|


**表 32**  io.k8s.api.core.v1.PersistentVolumeClaimStatus

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|accessModes|否|Array of strings|AccessModes contains the actual access modes the volume backing the PVC has. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|capacity|否|Map<String,String>|Represents the actual resources of the underlying volume.|
|conditions|否|Array of io.k8s.api.core.v1.PersistentVolumeClaimCondition objects|Current Condition of persistent volume claim. If underlying persistent volume is being resized then the Condition will be set to 'ResizeStarted'.|
|phase|否|String|Phase represents the current phase of PersistentVolumeClaim.|


**表 33**  io.k8s.api.core.v1.PersistentVolumeClaimCondition

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|lastProbeTime|否|String|Last time we probed the condition.|
|lastTransitionTime|否|String|Last time the condition transitioned from one status to another.|
|message|否|String|Human-readable message indicating details about last transition.|
|reason|否|String|Unique, this should be a short, machine understandable string that gives the reason for condition's last transition. If it reports "ResizeStarted" that means the underlying persistent volume is being resized.|
|status|是|String|status is the status of the condition.|
|type|是|String|type is the type of the condition.|


**表 34**  status

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|ControlledResources|否|Map<String,String>|All of the resources that are controlled by this job.|
|Succeeded|否|Integer|The number of pods which reached phase Succeeded.|
|failed|否|Integer|The number of pods which reached phase Failed.|
|minAvailable|否|Integer|The minimal available pods to run for this Job|
|pending|否|Integer|The number of pending pods.|
|retryCount|否|Integer|The number that volcano retried to submit the job.|
|running|否|Integer|The number of running pods.|
|state|否|state object|Current state of Job.|
|version|否|Integer|Job's current version|


**表 35**  state

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|message|否|String|Human-readable message indicating details about last transition.|
|phase|否|String|The phase of Job|
|reason|否|String|Unique, one-word, CamelCase reason for the condition's last transition.|


## 响应参数

**状态码： 200**

**表 36**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|spec object|Specification of the desired behavior of a cron job, including the minAvailable|
|status|status object|Current status of Job|


**表 37**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta

|参数|参数类型|描述|
|--|--|--|
|annotations|Map<String,String>|Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations|
|clusterName|String|The name of the cluster which the object belongs to. This is used to distinguish resources with same name and namespace in different clusters. This field is not set anywhere right now and apiserver is going to ignore it if set in create or update request.|
|creationTimestamp|String|CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is represented in RFC3339 form and is in UTC.Populated by the system. Read-only. Null for lists. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|deletionGracePeriodSeconds|Long|Number of seconds allowed for this object to gracefully terminate before it will be removed from the system. Only set when deletionTimestamp is also set. May only be shortened. Read-only.|
|deletionTimestamp|String|DeletionTimestamp is RFC 3339 date and time at which this resource will be deleted. This field is set by the server when a graceful deletion is requested by the user, and is not directly settable by a client. The resource is expected to be deleted (no longer visible from resource lists, and not reachable by name) after the time in this field, once the finalizers list is empty. As long as the finalizers list contains items, deletion is blocked. Once the deletionTimestamp is set, this value may not be unset or be set further into the future, although it may be shortened or the resource may be deleted prior to this time. For example, a user may request that a pod is deleted in 30 seconds. The Kubelet will react by sending a graceful termination signal to the containers in the pod. After that 30 seconds, the Kubelet will send a hard termination signal (SIGKILL) to the container and after cleanup, remove the pod from the API. In the presence of network partitions, this object may still exist after this timestamp, until an administrator or automated process can determine the resource is fully terminated. If not set, graceful deletion of the object has not been requested.Populated by the system when a graceful deletion is requested. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|finalizers|Array of strings|Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed.|
|generateName|String|GenerateName is an optional prefix, used by the server, to generate a unique name ONLY IF the Name field has not been provided. If this field is used, the name returned to the client will be different than the name passed. This value will also be combined with a unique suffix. The provided value has the same validation rules as the Name field, and may be truncated by the length of the suffix required to make the value unique on the server.If this field is specified and the generated name exists, the server will NOT return a 409 - instead, it will either return 201 Created or 500 with Reason ServerTimeout indicating a unique name could not be found in the time allotted, and the client should retry (optionally after the time indicated in the Retry-After header).Applied only if Name is not specified. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#idempotency|
|generation|Long|A sequence number representing a specific generation of the desired state. Populated by the system. Read-only.|
|initializers|io.k8s.apimachinery.pkg.apis.meta.v1.Initializers object|An initializer is a controller which enforces some system invariant at object creation time. This field is a list of initializers that have not yet acted on this object. If nil or empty, this object has been completely initialized. Otherwise, the object is considered uninitialized and is hidden (in list/watch and get calls) from clients that haven't explicitly asked to observe uninitialized objects.When an object is created, the system will populate this list with the current set of initializers. Only privileged users may set or modify this list. Once it is empty, it may not be modified further by any user.DEPRECATED - initializers are an alpha field and will be removed in v1.15.|
|labels|Map<String,String>|Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels|
|managedFields|Array of io.k8s.apimachinery.pkg.apis.meta.v1.ManagedFieldsEntry objects|ManagedFields maps workflow-id and version to the set of fields that are managed by that workflow. This is mostly for internal housekeeping, and users typically shouldn't need to set or understand this field. A workflow can be the user's name, a controller's name, or the name of a specific apply path like "ci-cd". The set of fields is always in the version that the workflow used when modifying the object.This field is alpha and can be changed or removed without notice.|
|name|String|Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|namespace|String|Namespace defines the space within each name must be unique. An empty namespace is equivalent to the "default" namespace, but "default" is the canonical representation. Not all objects are required to be scoped to a namespace - the value of this field for those objects will be empty.Must be a DNS_LABEL. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/namespaces|
|ownerReferences|Array of io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference objects|List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller.|
|resourceVersion|String|An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources.Populated by the system. Read-only. Value must be treated as opaque by clients and . More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|SelfLink is a URL representing this object. Populated by the system. Read-only.|
|uid|String|UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations.Populated by the system. Read-only. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 38**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers

|参数|参数类型|描述|
|--|--|--|
|pending|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|io.k8s.apimachinery.pkg.apis.meta.v1.Status object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 39**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer

|参数|参数类型|描述|
|--|--|--|
|name|String|name of the process that is responsible for initializing this object.|


**表 40**  io.k8s.apimachinery.pkg.apis.meta.v1.Status

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|code|Integer|Suggested HTTP return code for this status, 0 if not set.|
|details|io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails object|Extended data associated with the reason. Each reason may define its own extended details. This field is optional and the data returned is not guaranteed to conform to any schema except that defined by the reason type.|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|message|String|A human-readable description of the status of this operation.|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|reason|String|A machine-readable description of why this operation is in the "Failure" status. If this value is empty there is no information available. A Reason clarifies an HTTP status code but does not override it.|
|status|String|Status of the operation. One of: "Success" or "Failure". More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|


**表 41**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 42**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 43**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a consistent list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response, unless you have received this token from an error message.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 44**  io.k8s.apimachinery.pkg.apis.meta.v1.ManagedFieldsEntry

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the version of this resource that this field set applies to. The format is "group/version" just like the top-level APIVersion field. It is necessary to track the version of a field set because it cannot be automatically converted.|
|fields|Object|Fields identifies a set of fields.|
|manager|String|Manager is an identifier of the workflow managing these fields.|
|operation|String|Operation is the type of operation which lead to this ManagedFieldsEntry being created. The only valid values for this field are 'Apply' and 'Update'.|
|time|String|Time is timestamp of when these fields were set. It should always be empty if Operation is 'Apply'|


**表 45**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 46**  spec

|参数|参数类型|描述|
|--|--|--|
|maxRetry|Integer|The limit for retrying submiting job, default is 3|
|minAvailable|Integer|The minimal available pods to run for this Job|
|plugins|Object|Enabled task plugins when creating job.|
|policies|Array of policies objects|Specifies the default lifecycle of tasks|
|queue|String|The name of the queue on which job should been created|
|schedulerName|String|SchedulerName is the default value of *tasks.template.spec.schedulerName*.|
|tasks|Array of tasks objects|Tasks specifies the task specification of Job|
|volumes|Array of volumes objects|The volumes for Job|


**表 47**  policies

|参数|参数类型|描述|
|--|--|--|
|action|String|The action that will be taken to the PodGroup according to Event. One of "Restart", "None". Default to None.|
|event|String|The Event recorded by scheduler; the controller takes actions according to this Event.|
|timeout|Object|Timeout is the grace period for controller to take actions. Default to nil (take action immediately).|


**表 48**  tasks

|参数|参数类型|描述|
|--|--|--|
|name|String|Name specifies the name of tasks|
|policies|Array of policies objects|Specifies the lifecycle of task|
|replicas|Integer|Replicas specifies the replicas of this TaskSpec in Job|
|template|Object|Specifies the pod that will be created for this TaskSpec when executing a Job|


**表 49**  policies

|参数|参数类型|描述|
|--|--|--|
|action|String|The action that will be taken to the PodGroup according to Event. One of "Restart", "None". Default to None.|
|event|String|The Event recorded by scheduler; the controller takes actions according to this Event.|
|timeout|Object|Timeout is the grace period for controller to take actions. Default to nil (take action immediately).|


**表 50**  volumes

|参数|参数类型|描述|
|--|--|--|
|mountPath|String|Path within the container at which the volume should be mounted. Must not contain ':'.|
|volumeClaim|io.k8s.api.core.v1.PersistentVolumeClaim object|VolumeClaim defines the PVC used by the VolumeMount.|
|volumeClaimName|String|The name of the volume claim.|


**表 51**  io.k8s.api.core.v1.PersistentVolumeClaim

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|io.k8s.api.core.v1.PersistentVolumeClaimSpec object|Spec defines the desired characteristics of a volume requested by a pod author. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|
|status|io.k8s.api.core.v1.PersistentVolumeClaimStatus object|Status represents the current information/status of a persistent volume claim. Read-only. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|


**表 52**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta\_v3

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


**表 53**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers\_v3

|参数|参数类型|描述|
|--|--|--|
|pending|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer_v2 objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|io.k8s.apimachinery.pkg.apis.meta.v1.Status_v3 object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 54**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer\_v2

|参数|参数类型|描述|
|--|--|--|
|name|String|name of the process that is responsible for initializing this object.|


**表 55**  io.k8s.apimachinery.pkg.apis.meta.v1.Status\_v3

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


**表 56**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 57**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 58**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 59**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 60**  io.k8s.api.core.v1.PersistentVolumeClaimSpec

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the desired access modes the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|resources|io.k8s.api.core.v1.ResourceRequirements object|Resources represents the minimum resources the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#resources|
|selector|io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector object|A label query over volumes to consider for binding.|
|storageClassName|String|Name of the StorageClass required by the claim. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#class-1|
|volumeMode|String|volumeMode defines what type of volume is required by the claim. Value of Filesystem is implied when not included in claim spec. This is an alpha feature and may change in the future.|
|volumeName|String|VolumeName is the binding reference to the PersistentVolume backing this claim.|


**表 61**  io.k8s.api.core.v1.ResourceRequirements

|参数|参数类型|描述|
|--|--|--|
|limits|Map<String,String>|Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|
|requests|Map<String,String>|Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|


**表 62**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector

|参数|参数类型|描述|
|--|--|--|
|matchExpressions|Array of io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement objects|matchExpressions is a list of label selector requirements. The requirements are ANDed.|
|matchLabels|Map<String,String>|matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.|


**表 63**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement

|参数|参数类型|描述|
|--|--|--|
|key|String|key is the label key that the selector applies to.|
|operator|String|operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.|
|values|Array of strings|values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.|


**表 64**  io.k8s.api.core.v1.PersistentVolumeClaimStatus

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the actual access modes the volume backing the PVC has. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|capacity|Map<String,String>|Represents the actual resources of the underlying volume.|
|conditions|Array of io.k8s.api.core.v1.PersistentVolumeClaimCondition objects|Current Condition of persistent volume claim. If underlying persistent volume is being resized then the Condition will be set to 'ResizeStarted'.|
|phase|String|Phase represents the current phase of PersistentVolumeClaim.|


**表 65**  io.k8s.api.core.v1.PersistentVolumeClaimCondition

|参数|参数类型|描述|
|--|--|--|
|lastProbeTime|String|Last time we probed the condition.|
|lastTransitionTime|String|Last time the condition transitioned from one status to another.|
|message|String|Human-readable message indicating details about last transition.|
|reason|String|Unique, this should be a short, machine understandable string that gives the reason for condition's last transition. If it reports "ResizeStarted" that means the underlying persistent volume is being resized.|
|status|String|status is the status of the condition.|
|type|String|type is the type of the condition.|


**表 66**  status

|参数|参数类型|描述|
|--|--|--|
|ControlledResources|Map<String,String>|All of the resources that are controlled by this job.|
|Succeeded|Integer|The number of pods which reached phase Succeeded.|
|failed|Integer|The number of pods which reached phase Failed.|
|minAvailable|Integer|The minimal available pods to run for this Job|
|pending|Integer|The number of pending pods.|
|retryCount|Integer|The number that volcano retried to submit the job.|
|running|Integer|The number of running pods.|
|state|state object|Current state of Job.|
|version|Integer|Job's current version|


**表 67**  state

|参数|参数类型|描述|
|--|--|--|
|message|String|Human-readable message indicating details about last transition.|
|phase|String|The phase of Job|
|reason|String|Unique, one-word, CamelCase reason for the condition's last transition.|


**状态码： 201**

**表 68**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|spec object|Specification of the desired behavior of a cron job, including the minAvailable|
|status|status object|Current status of Job|


**表 69**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta

|参数|参数类型|描述|
|--|--|--|
|annotations|Map<String,String>|Annotations is an unstructured key value map stored with a resource that may be set by external tools to store and retrieve arbitrary metadata. They are not queryable and should be preserved when modifying objects. More info: http://kubernetes.io/docs/user-guide/annotations|
|clusterName|String|The name of the cluster which the object belongs to. This is used to distinguish resources with same name and namespace in different clusters. This field is not set anywhere right now and apiserver is going to ignore it if set in create or update request.|
|creationTimestamp|String|CreationTimestamp is a timestamp representing the server time when this object was created. It is not guaranteed to be set in happens-before order across separate operations. Clients may not set this value. It is represented in RFC3339 form and is in UTC.Populated by the system. Read-only. Null for lists. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|deletionGracePeriodSeconds|Long|Number of seconds allowed for this object to gracefully terminate before it will be removed from the system. Only set when deletionTimestamp is also set. May only be shortened. Read-only.|
|deletionTimestamp|String|DeletionTimestamp is RFC 3339 date and time at which this resource will be deleted. This field is set by the server when a graceful deletion is requested by the user, and is not directly settable by a client. The resource is expected to be deleted (no longer visible from resource lists, and not reachable by name) after the time in this field, once the finalizers list is empty. As long as the finalizers list contains items, deletion is blocked. Once the deletionTimestamp is set, this value may not be unset or be set further into the future, although it may be shortened or the resource may be deleted prior to this time. For example, a user may request that a pod is deleted in 30 seconds. The Kubelet will react by sending a graceful termination signal to the containers in the pod. After that 30 seconds, the Kubelet will send a hard termination signal (SIGKILL) to the container and after cleanup, remove the pod from the API. In the presence of network partitions, this object may still exist after this timestamp, until an administrator or automated process can determine the resource is fully terminated. If not set, graceful deletion of the object has not been requested.Populated by the system when a graceful deletion is requested. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|finalizers|Array of strings|Must be empty before the object is deleted from the registry. Each entry is an identifier for the responsible component that will remove the entry from the list. If the deletionTimestamp of the object is non-nil, entries in this list can only be removed.|
|generateName|String|GenerateName is an optional prefix, used by the server, to generate a unique name ONLY IF the Name field has not been provided. If this field is used, the name returned to the client will be different than the name passed. This value will also be combined with a unique suffix. The provided value has the same validation rules as the Name field, and may be truncated by the length of the suffix required to make the value unique on the server.If this field is specified and the generated name exists, the server will NOT return a 409 - instead, it will either return 201 Created or 500 with Reason ServerTimeout indicating a unique name could not be found in the time allotted, and the client should retry (optionally after the time indicated in the Retry-After header).Applied only if Name is not specified. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#idempotency|
|generation|Long|A sequence number representing a specific generation of the desired state. Populated by the system. Read-only.|
|initializers|io.k8s.apimachinery.pkg.apis.meta.v1.Initializers object|An initializer is a controller which enforces some system invariant at object creation time. This field is a list of initializers that have not yet acted on this object. If nil or empty, this object has been completely initialized. Otherwise, the object is considered uninitialized and is hidden (in list/watch and get calls) from clients that haven't explicitly asked to observe uninitialized objects.When an object is created, the system will populate this list with the current set of initializers. Only privileged users may set or modify this list. Once it is empty, it may not be modified further by any user.DEPRECATED - initializers are an alpha field and will be removed in v1.15.|
|labels|Map<String,String>|Map of string keys and values that can be used to organize and categorize (scope and select) objects. May match selectors of replication controllers and services. More info: http://kubernetes.io/docs/user-guide/labels|
|managedFields|Array of io.k8s.apimachinery.pkg.apis.meta.v1.ManagedFieldsEntry objects|ManagedFields maps workflow-id and version to the set of fields that are managed by that workflow. This is mostly for internal housekeeping, and users typically shouldn't need to set or understand this field. A workflow can be the user's name, a controller's name, or the name of a specific apply path like "ci-cd". The set of fields is always in the version that the workflow used when modifying the object.This field is alpha and can be changed or removed without notice.|
|name|String|Name must be unique within a namespace. Is required when creating resources, although some resources may allow a client to request the generation of an appropriate name automatically. Name is primarily intended for creation idempotence and configuration definition. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|namespace|String|Namespace defines the space within each name must be unique. An empty namespace is equivalent to the "default" namespace, but "default" is the canonical representation. Not all objects are required to be scoped to a namespace - the value of this field for those objects will be empty.Must be a DNS_LABEL. Cannot be updated. More info: http://kubernetes.io/docs/user-guide/namespaces|
|ownerReferences|Array of io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference objects|List of objects depended by this object. If ALL objects in the list have been deleted, this object will be garbage collected. If this object is managed by a controller, then an entry in this list will point to this controller, with the controller field set to true. There cannot be more than one managing controller.|
|resourceVersion|String|An opaque value that represents the internal version of this object that can be used by clients to determine when objects have changed. May be used for optimistic concurrency, change detection, and the watch operation on a resource or set of resources. Clients must treat these values as opaque and passed unmodified back to the server. They may only be valid for a particular resource or set of resources.Populated by the system. Read-only. Value must be treated as opaque by clients and . More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|SelfLink is a URL representing this object. Populated by the system. Read-only.|
|uid|String|UID is the unique in time and space value for this object. It is typically generated by the server on successful creation of a resource and is not allowed to change on PUT operations.Populated by the system. Read-only. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 70**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers

|参数|参数类型|描述|
|--|--|--|
|pending|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|io.k8s.apimachinery.pkg.apis.meta.v1.Status object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 71**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer

|参数|参数类型|描述|
|--|--|--|
|name|String|name of the process that is responsible for initializing this object.|


**表 72**  io.k8s.apimachinery.pkg.apis.meta.v1.Status

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|code|Integer|Suggested HTTP return code for this status, 0 if not set.|
|details|io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails object|Extended data associated with the reason. Each reason may define its own extended details. This field is optional and the data returned is not guaranteed to conform to any schema except that defined by the reason type.|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|message|String|A human-readable description of the status of this operation.|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|reason|String|A machine-readable description of why this operation is in the "Failure" status. If this value is empty there is no information available. A Reason clarifies an HTTP status code but does not override it.|
|status|String|Status of the operation. One of: "Success" or "Failure". More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|


**表 73**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 74**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 75**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a consistent list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response, unless you have received this token from an error message.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 76**  io.k8s.apimachinery.pkg.apis.meta.v1.ManagedFieldsEntry

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the version of this resource that this field set applies to. The format is "group/version" just like the top-level APIVersion field. It is necessary to track the version of a field set because it cannot be automatically converted.|
|fields|Object|Fields identifies a set of fields.|
|manager|String|Manager is an identifier of the workflow managing these fields.|
|operation|String|Operation is the type of operation which lead to this ManagedFieldsEntry being created. The only valid values for this field are 'Apply' and 'Update'.|
|time|String|Time is timestamp of when these fields were set. It should always be empty if Operation is 'Apply'|


**表 77**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 78**  spec

|参数|参数类型|描述|
|--|--|--|
|maxRetry|Integer|The limit for retrying submiting job, default is 3|
|minAvailable|Integer|The minimal available pods to run for this Job|
|plugins|Object|Enabled task plugins when creating job.|
|policies|Array of policies objects|Specifies the default lifecycle of tasks|
|queue|String|The name of the queue on which job should been created|
|schedulerName|String|SchedulerName is the default value of *tasks.template.spec.schedulerName*.|
|tasks|Array of tasks objects|Tasks specifies the task specification of Job|
|volumes|Array of volumes objects|The volumes for Job|


**表 79**  policies

|参数|参数类型|描述|
|--|--|--|
|action|String|The action that will be taken to the PodGroup according to Event. One of "Restart", "None". Default to None.|
|event|String|The Event recorded by scheduler; the controller takes actions according to this Event.|
|timeout|Object|Timeout is the grace period for controller to take actions. Default to nil (take action immediately).|


**表 80**  tasks

|参数|参数类型|描述|
|--|--|--|
|name|String|Name specifies the name of tasks|
|policies|Array of policies objects|Specifies the lifecycle of task|
|replicas|Integer|Replicas specifies the replicas of this TaskSpec in Job|
|template|Object|Specifies the pod that will be created for this TaskSpec when executing a Job|


**表 81**  policies

|参数|参数类型|描述|
|--|--|--|
|action|String|The action that will be taken to the PodGroup according to Event. One of "Restart", "None". Default to None.|
|event|String|The Event recorded by scheduler; the controller takes actions according to this Event.|
|timeout|Object|Timeout is the grace period for controller to take actions. Default to nil (take action immediately).|


**表 82**  volumes

|参数|参数类型|描述|
|--|--|--|
|mountPath|String|Path within the container at which the volume should be mounted. Must not contain ':'.|
|volumeClaim|io.k8s.api.core.v1.PersistentVolumeClaim object|VolumeClaim defines the PVC used by the VolumeMount.|
|volumeClaimName|String|The name of the volume claim.|


**表 83**  io.k8s.api.core.v1.PersistentVolumeClaim

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|io.k8s.api.core.v1.PersistentVolumeClaimSpec object|Spec defines the desired characteristics of a volume requested by a pod author. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|
|status|io.k8s.api.core.v1.PersistentVolumeClaimStatus object|Status represents the current information/status of a persistent volume claim. Read-only. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|


**表 84**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta\_v3

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


**表 85**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers\_v3

|参数|参数类型|描述|
|--|--|--|
|pending|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer_v2 objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|io.k8s.apimachinery.pkg.apis.meta.v1.Status_v3 object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 86**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer\_v2

|参数|参数类型|描述|
|--|--|--|
|name|String|name of the process that is responsible for initializing this object.|


**表 87**  io.k8s.apimachinery.pkg.apis.meta.v1.Status\_v3

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


**表 88**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 89**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 90**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 91**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 92**  io.k8s.api.core.v1.PersistentVolumeClaimSpec

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the desired access modes the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|resources|io.k8s.api.core.v1.ResourceRequirements object|Resources represents the minimum resources the volume should have. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#resources|
|selector|io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector object|A label query over volumes to consider for binding.|
|storageClassName|String|Name of the StorageClass required by the claim. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#class-1|
|volumeMode|String|volumeMode defines what type of volume is required by the claim. Value of Filesystem is implied when not included in claim spec. This is an alpha feature and may change in the future.|
|volumeName|String|VolumeName is the binding reference to the PersistentVolume backing this claim.|


**表 93**  io.k8s.api.core.v1.ResourceRequirements

|参数|参数类型|描述|
|--|--|--|
|limits|Map<String,String>|Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|
|requests|Map<String,String>|Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|


**表 94**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector

|参数|参数类型|描述|
|--|--|--|
|matchExpressions|Array of io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement objects|matchExpressions is a list of label selector requirements. The requirements are ANDed.|
|matchLabels|Map<String,String>|matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.|


**表 95**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement

|参数|参数类型|描述|
|--|--|--|
|key|String|key is the label key that the selector applies to.|
|operator|String|operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.|
|values|Array of strings|values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.|


**表 96**  io.k8s.api.core.v1.PersistentVolumeClaimStatus

|参数|参数类型|描述|
|--|--|--|
|accessModes|Array of strings|AccessModes contains the actual access modes the volume backing the PVC has. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#access-modes-1|
|capacity|Map<String,String>|Represents the actual resources of the underlying volume.|
|conditions|Array of io.k8s.api.core.v1.PersistentVolumeClaimCondition objects|Current Condition of persistent volume claim. If underlying persistent volume is being resized then the Condition will be set to 'ResizeStarted'.|
|phase|String|Phase represents the current phase of PersistentVolumeClaim.|


**表 97**  io.k8s.api.core.v1.PersistentVolumeClaimCondition

|参数|参数类型|描述|
|--|--|--|
|lastProbeTime|String|Last time we probed the condition.|
|lastTransitionTime|String|Last time the condition transitioned from one status to another.|
|message|String|Human-readable message indicating details about last transition.|
|reason|String|Unique, this should be a short, machine understandable string that gives the reason for condition's last transition. If it reports "ResizeStarted" that means the underlying persistent volume is being resized.|
|status|String|status is the status of the condition.|
|type|String|type is the type of the condition.|


**表 98**  status

|参数|参数类型|描述|
|--|--|--|
|ControlledResources|Map<String,String>|All of the resources that are controlled by this job.|
|Succeeded|Integer|The number of pods which reached phase Succeeded.|
|failed|Integer|The number of pods which reached phase Failed.|
|minAvailable|Integer|The minimal available pods to run for this Job|
|pending|Integer|The number of pending pods.|
|retryCount|Integer|The number that volcano retried to submit the job.|
|running|Integer|The number of running pods.|
|state|state object|Current state of Job.|
|version|Integer|Job's current version|


**表 99**  state

|参数|参数类型|描述|
|--|--|--|
|message|String|Human-readable message indicating details about last transition.|
|phase|String|The phase of Job|
|reason|String|Unique, one-word, CamelCase reason for the condition's last transition.|


## 请求示例

将创建的Volcano Job的其中一个task的replicas从1修改为2：

```
{
  "apiVersion" : "batch.volcano.sh/v1alpha1",
  "kind" : "Job",
  "metadata" : {
    "name" : "openmpi-hello-2-com",
    "namespace" : "cci-gpu",
    "resourceVersion" : "125597961"
  },
  "spec" : {
    "minAvailable" : 2,
    "plugins" : {
      "env" : [ ],
      "ssh" : [ ],
      "svc" : [ ]
    },
    "queue" : "default",
    "schedulerName" : "volcano",
    "tasks" : [ {
      "name" : "mpimaster",
      "policies" : [ {
        "action" : "CompleteJob",
        "event" : "TaskCompleted"
      } ],
      "replicas" : 1,
      "template" : {
        "spec" : {
          "containers" : [ {
            "command" : [ "/bin/sh", "-c", "MPI_HOST=`cat /etc/volcano/mpiworker.host | tr \"\\n\" \",\"`;\nmkdir -p /var/run/sshd; /usr/sbin/sshd;\nmpiexec --allow-run-as-root --host ${MPI_HOST} -np 2 mpi_hello_world 003e /home/re" ],
            "image" : "*.*.*.*:20202/swr/openmpi-hello:3.28",
            "name" : "mpimaster",
            "ports" : [ {
              "containerPort" : 22,
              "name" : "mpijob-port"
            } ],
            "resources" : {
              "limits" : {
                "cpu" : "250m",
                "memory" : "1Gi"
              },
              "requests" : {
                "cpu" : "250m",
                "memory" : "1Gi"
              }
            },
            "workingDir" : "/home"
          } ],
          "imagePullSecrets" : [ {
            "name" : "default-secret"
          } ],
          "restartPolicy" : "OnFailure"
        }
      }
    }, {
      "name" : "mpiworker",
      "replicas" : 2,
      "template" : {
        "spec" : {
          "containers" : [ {
            "command" : [ "/bin/sh", "-c", "mkdir -p /var/run/sshd; /usr/sbin/sshd -D;" ],
            "image" : "*.*.*.*:20202/swr/openmpi-hello:3.28",
            "name" : "mpiworker",
            "ports" : [ {
              "containerPort" : 22,
              "name" : "mpijob-port"
            } ],
            "resources" : {
              "limits" : {
                "cpu" : "250m",
                "memory" : "1Gi"
              },
              "requests" : {
                "cpu" : "250m",
                "memory" : "1Gi"
              }
            },
            "workingDir" : "/home"
          } ],
          "imagePullSecrets" : [ {
            "name" : "default-secret"
          } ],
          "restartPolicy" : "OnFailure"
        }
      }
    } ]
  },
  "status" : {
    "minAvailable" : 1,
    "pending" : 3,
    "state" : {
      "lastTransitionTime" : "2019-07-11T08:09:45Z",
      "phase" : "Succeed"
    }
  }
}
```

## 响应示例

**状态码： 200**

OK

```
{
  "apiVersion" : "batch.volcano.sh/v1alpha1",
  "kind" : "Job",
  "metadata" : {
    "creationTimestamp" : "2019-07-11T08:09:41Z",
    "generation" : 2,
    "name" : "openmpi-hello-2-com",
    "namespace" : "zjh-gpu",
    "resourceVersion" : "125620754",
    "selfLink" : "/apis/batch.volcano.sh/v1alpha1/namespaces/zjh-gpu/jobs/openmpi-hello-2-com",
    "uid" : "3bdba739-a3b3-11e9-8865-501d93440997"
  },
  "spec" : {
    "minAvailable" : 2,
    "plugins" : {
      "env" : [ ],
      "ssh" : [ ],
      "svc" : [ ]
    },
    "queue" : "default",
    "schedulerName" : "volcano",
    "tasks" : [ {
      "name" : "mpimaster",
      "policies" : [ {
        "action" : "CompleteJob",
        "event" : "TaskCompleted"
      } ],
      "replicas" : 1,
      "template" : {
        "spec" : {
          "containers" : [ {
            "command" : [ "/bin/sh", "-c", "MPI_HOST=`cat /etc/volcano/mpiworker.host | tr \"\\n\" \",\"`;\nmkdir -p /var/run/sshd; /usr/sbin/sshd;\nmpiexec --allow-run-as-root --host ${MPI_HOST} -np 2 mpi_hello_world 003e /home/re" ],
            "image" : "*.*.*.*:20202/swr/openmpi-hello:3.28",
            "name" : "mpimaster",
            "ports" : [ {
              "containerPort" : 22,
              "name" : "mpijob-port"
            } ],
            "resources" : {
              "limits" : {
                "cpu" : "250m",
                "memory" : "1Gi"
              },
              "requests" : {
                "cpu" : "250m",
                "memory" : "1Gi"
              }
            },
            "workingDir" : "/home"
          } ],
          "imagePullSecrets" : [ {
            "name" : "default-secret"
          } ],
          "restartPolicy" : "OnFailure"
        }
      }
    }, {
      "name" : "mpiworker",
      "replicas" : 2,
      "template" : {
        "spec" : {
          "containers" : [ {
            "command" : [ "/bin/sh", "-c", "mkdir -p /var/run/sshd; /usr/sbin/sshd -D;" ],
            "image" : "*.*.*.*:20202/swr/openmpi-hello:3.28",
            "name" : "mpiworker",
            "ports" : [ {
              "containerPort" : 22,
              "name" : "mpijob-port"
            } ],
            "resources" : {
              "limits" : {
                "cpu" : "250m",
                "memory" : "1Gi"
              },
              "requests" : {
                "cpu" : "250m",
                "memory" : "1Gi"
              }
            },
            "workingDir" : "/home"
          } ],
          "imagePullSecrets" : [ {
            "name" : "default-secret"
          } ],
          "restartPolicy" : "OnFailure"
        }
      }
    } ]
  },
  "status" : {
    "controlledResources" : {
      "plugin-env" : "env",
      "plugin-ssh" : "ssh",
      "plugin-svc" : "svc"
    },
    "minAvailable" : 1,
    "pending" : 3,
    "state" : {
      "lastTransitionTime" : "2019-07-11T08:09:45Z",
      "phase" : "Inqueue"
    }
  }
}
```

## 状态码

|状态码|描述|
|--|--|
|200|OK|
|201|Created|
|400|BadRequest|
|401|Unauthorized|
|403|Forbidden|
|404|NotFound|
|405|MethodNotAllowed|
|406|NotAcceptable|
|409|Conflict|
|415|UnsupportedMediaType|
|422|Invalid|
|429|TooManyRequests|
|500|InternalError|
|503|ServiceUnavailable|
|504|ServerTimeout|


