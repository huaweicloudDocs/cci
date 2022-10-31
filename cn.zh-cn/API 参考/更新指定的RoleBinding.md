# 更新指定的RoleBinding<a name="patchRbacAuthorizationV1NamespacedRoleBinding"></a>

## 功能介绍

This API is used to partially update the specified RoleBinding

## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=CCI&api=patchRbacAuthorizationV1NamespacedRoleBinding)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

PATCH /apis/rbac.authorization.k8s.io/v1/namespaces/\{namespace\}/rolebindings/\{name\}

**表 1**  路径参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|name|是|String|name of the RoleBinding|
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
|Content-Type|是|String|目前支持两种类型的PATCH请求方法的操作。Merge Patch, Content-Type: application/merge-patch+json 在RFC7386协议的定义中，Merge Patch必须包含对一个资源对象的部分描述，即为JSON对象。该JSON对象被提交到服务端后与服务端的当前对象合并，即替换当前资源对象中的列表域，从而创建一个新的对象。Strategic Merge Patch, Content-Type: application/strategic-merge-patch+json Strategic Merge Patch是添加合法的元数据到API对象中，并通过这些新的元数据来决定哪个列表被合并，哪个列表不该被合并。当前这些元数据则作为结构标签。|


## 响应参数

**状态码： 200**

**表 4**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata.|
|roleRef|io.k8s.api.rbac.v1.RoleRef object|RoleRef can reference a Role in the current namespace or a ClusterRole in the global namespace. If the RoleRef cannot be resolved, the Authorizer must return an error.|
|subjects|Array of io.k8s.api.rbac.v1.Subject objects|Subjects holds references to the objects the role applies to.|


**表 5**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta\_v3

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


**表 6**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers\_v3

|参数|参数类型|描述|
|--|--|--|
|pending|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer_v2 objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|io.k8s.apimachinery.pkg.apis.meta.v1.Status_v3 object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 7**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer\_v2

|参数|参数类型|描述|
|--|--|--|
|name|String|name of the process that is responsible for initializing this object.|


**表 8**  io.k8s.apimachinery.pkg.apis.meta.v1.Status\_v3

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


**表 9**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 10**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 11**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


**表 12**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 13**  io.k8s.api.rbac.v1.RoleRef

|参数|参数类型|描述|
|--|--|--|
|apiGroup|String|APIGroup is the group for the resource being referenced|
|kind|String|Kind is the type of resource being referenced|
|name|String|Name is the name of resource being referenced|


**表 14**  io.k8s.api.rbac.v1.Subject

|参数|参数类型|描述|
|--|--|--|
|apiGroup|String|APIGroup holds the API group of the referenced subject. Defaults to "" for ServiceAccount subjects. Defaults to "rbac.authorization.k8s.io" for User and Group subjects.|
|kind|String|Kind of object being referenced. Values defined by this API group are "User", "Group", and "ServiceAccount". If the Authorizer does not recognized the kind value, the Authorizer should report an error.|
|name|String|Name of the object being referenced.|
|namespace|String|Namespace of the referenced object. If the object kind is non-namespace, such as "User" or "Group", and this value is not empty the Authorizer should report an error.|


## 请求示例

“Content-Type”的详细描述请参见 PATCH请求方法操作说明：https://support.huaweicloud.com/api-cci/cci\_02\_0070.html。

```
{
  "roleRef" : {
    "apiGroup" : "rbac.authorization.k8s.io",
    "kind" : "ClusterRole",
    "name" : "view"
  },
  "subjects" : [ {
    "apiGroup" : "rbac.authorization.k8s.io",
    "kind" : "User",
    "name" : "07b82a44a680d5661f01c00b448f8f50"
  }, {
    "apiGroup" : "rbac.authorization.k8s.io",
    "kind" : "Group",
    "name" : "07b8387fd080d2963f92c00bb9a7341e"
  } ]
}
```

## 响应示例

**状态码： 200**

OK

```
{
  "apiVersion" : "rbac.authorization.k8s.io/v1",
  "kind" : "RoleBinding",
  "metadata" : {
    "creationTimestamp" : "2020-04-07T08:25:46Z",
    "name" : "clusterrole_view_User_07b82a44a680d5661f01c00b448f8f50",
    "namespace" : "rbac-test",
    "resourceVersion" : "230608015",
    "selfLink" : "/apis/rbac.authorization.k8s.io/v1/namespaces/rbac-test/rolebindings/clusterrole_view_User_07b82a44a680d5661f01c00b448f8f50",
    "uid" : "6163c216-78a9-11ea-bcc5-340a9837e2a7"
  },
  "roleRef" : {
    "apiGroup" : "rbac.authorization.k8s.io",
    "kind" : "ClusterRole",
    "name" : "view"
  },
  "subjects" : [ {
    "apiGroup" : "rbac.authorization.k8s.io",
    "kind" : "User",
    "name" : "07b82a44a680d5661f01c00b448f8f50"
  }, {
    "apiGroup" : "rbac.authorization.k8s.io",
    "kind" : "Group",
    "name" : "07b8387fd080d2963f92c00bb9a7341e"
  } ]
}
```

## 状态码

|状态码|描述|
|--|--|
|200|OK|
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


