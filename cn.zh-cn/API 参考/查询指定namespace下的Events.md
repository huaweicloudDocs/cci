# 查询指定namespace下的Events<a name="listCoreV1NamespacedEvent"></a>

## 功能介绍

查询Namespace下所有Event的详细信息。

## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=CCI&api=listCoreV1NamespacedEvent)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

GET /api/v1/namespaces/\{namespace\}/events

**表 1**  路径参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|namespace|是|String|object name and auth scope, such as for teams and projects|


**表 2**  Query参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|continue|否|String|The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.|
|fieldSelector|否|String|A selector to restrict the list of returned objects by their fields. Defaults to everything.|
|includeUninitialized|否|Boolean|If true, partially initialized resources are included in the response.|
|labelSelector|否|String|A selector to restrict the list of returned objects by their labels. Defaults to everything.|
|limit|否|Integer|limit is a maximum number of responses to return for a list call. If more items exist, the server will set the *continue* field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.|
|resourceVersion|否|String|When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.|
|timeoutSeconds|否|Integer|Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.|
|watch|否|Boolean|Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.|
|pretty|否|String|If 'true', then the output is pretty printed.|


## 请求参数

**表 3**  请求Header参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|X-Auth-Token|是|String|用户Token。通过调用IAM服务获取用户Token接口获取（响应消息头中X-Subject-Token的值）。|


## 响应参数

**状态码： 200**

**表 4**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|items|Array of io.k8s.api.core.v1.Event objects|List of events|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta_v2 object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|


**表 5**  io.k8s.api.core.v1.Event

|参数|参数类型|描述|
|--|--|--|
|action|String|What action was taken/failed regarding to the Regarding object.|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|count|Integer|The number of times this event has occurred.|
|eventTime|String|Time when this Event was first observed.|
|firstTimestamp|String|The time at which the event was first recorded. (Time of server receipt is in TypeMeta.)|
|involvedObject|io.k8s.api.core.v1.ObjectReference object|The object that this event is about.|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|lastTimestamp|String|The time at which the most recent occurrence of this event was recorded.|
|message|String|A human-readable description of the status of this operation.|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|reason|String|This should be a short, machine understandable string that gives the reason for the transition into the object's current status.|
|related|io.k8s.api.core.v1.ObjectReference object|Optional secondary object for more complex actions.|
|reportingComponent|String|Name of the controller that emitted this Event, e.g. *kubernetes.io/kubelet*.|
|reportingInstance|String|ID of the controller instance, e.g. *kubelet-xyzf*.|
|series|io.k8s.api.core.v1.EventSeries object|Data about the Event series this event represents or nil if it's a singleton Event.|
|source|io.k8s.api.core.v1.EventSource object|The component reporting this event. Should be a short machine understandable string.|
|type|String|Type of this event (Normal, Warning), new types could be added in the future|


**表 6**  io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta\_v3

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


**表 7**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializers\_v3

|参数|参数类型|描述|
|--|--|--|
|pending|Array of io.k8s.apimachinery.pkg.apis.meta.v1.Initializer_v2 objects|Pending is a list of initializers that must execute in order before this object is visible. When the last pending initializer is removed, and no failing result is set, the initializers struct will be set to nil and the object is considered as initialized and visible to all clients.|
|result|io.k8s.apimachinery.pkg.apis.meta.v1.Status_v3 object|If result is set with the Failure field, the object will be persisted to storage and then deleted, ensuring that other clients can observe the deletion.|


**表 8**  io.k8s.apimachinery.pkg.apis.meta.v1.Initializer\_v2

|参数|参数类型|描述|
|--|--|--|
|name|String|name of the process that is responsible for initializing this object.|


**表 9**  io.k8s.apimachinery.pkg.apis.meta.v1.Status\_v3

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


**表 10**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusDetails\_v3

|参数|参数类型|描述|
|--|--|--|
|causes|Array of io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause_v2 objects|The Causes array includes more details associated with the StatusReason failure. Not all StatusReasons may provide detailed causes.|
|group|String|The group attribute of the resource associated with the status StatusReason.|
|kind|String|The kind attribute of the resource associated with the status StatusReason. On some operations may differ from the requested resource Kind. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|The name attribute of the resource associated with the status StatusReason (when there is a single name which can be described).|
|retryAfterSeconds|Integer|If specified, the time in seconds before the operation should be retried. Some errors may indicate the client must take an alternate action - for those errors this field may indicate how long to wait before taking the alternate action.|
|uid|String|UID of the resource. (when there is a single resource which can be described). More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 11**  io.k8s.apimachinery.pkg.apis.meta.v1.StatusCause\_v2

|参数|参数类型|描述|
|--|--|--|
|field|String|The field of the resource that has caused this error, as named by its JSON serialization. May include dot and postfix notation for nested attributes. Arrays are zero-indexed.  Fields may appear more than once in an array of causes due to fields having multiple errors. Optional.Examples: "name" - the field "name" on the current resource "items[0].name" - the field "name" on the first array entry in "items"|
|message|String|A human-readable description of the cause of the error. This field may be presented as-is to a reader.|
|reason|String|A machine-readable description of the cause of the error. If this value is empty there is no information available.|


**表 12**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 13**  io.k8s.api.core.v1.ObjectReference

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|fieldPath|String|If referring to a piece of an object instead of an entire object, this string should contain a valid JSON/Go field access statement, such as desiredState.manifest.containers[2]. For example, if the object reference is to a container within a pod, this would take on a value like: "spec.containers{name}" (where "name" refers to the name of the container that triggered the event) or if no container name is specified "spec.containers[2]" (container with index 2 in this pod). This syntax is chosen only to have some well-defined way of referencing a part of an object.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|namespace|String|Namespace of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/|
|resourceVersion|String|Specific resourceVersion to which this reference is made, if any. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|uid|String|UID of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#uids|


**表 14**  io.k8s.api.core.v1.EventSeries

|参数|参数类型|描述|
|--|--|--|
|count|Integer|Number of occurrences in this series up to the last heartbeat time|
|lastObservedTime|String|Time of the last occurrence observed|
|state|String|State of this Series: Ongoing or Finished|


**表 15**  io.k8s.api.core.v1.EventSource

|参数|参数类型|描述|
|--|--|--|
|component|String|Component from which the event is generated.|
|host|String|Node name on which the event is generated.|


**表 16**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

|参数|参数类型|描述|
|--|--|--|
|continue|String|continue may be set if the user set a limit on the number of items returned, and indicates that the server has more data available. The value is opaque and may be used to issue another request to the endpoint that served this list to retrieve the next set of available objects. Continuing a list may not be possible if the server configuration has changed or more than a few minutes have passed. The resourceVersion field returned when using this continue value will be identical to the value in the first response.|
|resourceVersion|String|String that identifies the server's internal version of this object that can be used by clients to determine when objects have changed. Value must be treated as opaque by clients and passed unmodified back to the server. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|selfLink|String|selfLink is a URL representing this object. Populated by the system. Read-only.|


## 请求示例

无

## 响应示例

**状态码： 200**

OK

```
{
  "apiVersion" : "v1",
  "items" : [ {
    "count" : 1,
    "eventTime" : null,
    "firstTimestamp" : "2018-09-03T12:58:07Z",
    "involvedObject" : {
      "apiVersion" : "v1",
      "kind" : "Pod",
      "name" : "deployment-test-57f7cff77c-5x5tw",
      "namespace" : "namespace-test",
      "resourceVersion" : "5036865",
      "uid" : "010fec39-af79-11e8-8f17-c81fbe371a17"
    },
    "lastTimestamp" : "2018-09-03T12:58:07Z",
    "message" : "Successfully assigned deployment-test-57f7cff77c-5x5tw to c0dd6256-195a-e811-90a2-10c17294fcbc",
    "metadata" : {
      "creationTimestamp" : "2018-09-03T12:58:07Z",
      "enable" : true,
      "name" : "deployment-test-57f7cff77c-5x5tw.1550e534d2d8a5ef",
      "namespace" : "namespace-test",
      "resourceVersion" : "760533",
      "selfLink" : "/api/v1/namespaces/namespace-test/events/deployment-test-57f7cff77c-5x5tw.1550e534d2d8a5ef",
      "uid" : "0122b5b2-af79-11e8-8f17-c81fbe371a17"
    },
    "reason" : "Scheduled",
    "reportingComponent" : "",
    "reportingInstance" : "",
    "source" : {
      "component" : "default-scheduler"
    },
    "type" : "Normal"
  }, {
    "count" : 2,
    "eventTime" : null,
    "firstTimestamp" : "2018-09-03T12:58:07Z",
    "involvedObject" : {
      "apiVersion" : "v1",
      "kind" : "Pod",
      "name" : "deployment-test-57f7cff77c-5x5tw",
      "namespace" : "namespace-test",
      "resourceVersion" : "5036870",
      "uid" : "010fec39-af79-11e8-8f17-c81fbe371a17"
    },
    "lastTimestamp" : "2018-09-03T12:58:12Z",
    "message" : "Successfully mounted volumes for pod \"deployment-test-57f7cff77c-5x5tw_namespace-test(010fec39-af79-11e8-8f17-c81fbe371a17)\"",
    "metadata" : {
      "creationTimestamp" : "2018-09-03T12:58:07Z",
      "enable" : true,
      "name" : "deployment-test-57f7cff77c-5x5tw.1550e534d3105acd",
      "namespace" : "namespace-test",
      "resourceVersion" : "760542",
      "selfLink" : "/api/v1/namespaces/namespace-test/events/deployment-test-57f7cff77c-5x5tw.1550e534d3105acd",
      "uid" : "0123faea-af79-11e8-8f17-c81fbe371a17"
    },
    "reason" : "SuccessfulMountVolume",
    "reportingComponent" : "",
    "reportingInstance" : "",
    "source" : {
      "component" : "kubelet",
      "host" : "c0dd6256-195a-e811-90a2-10c17294fcbc"
    },
    "type" : "Normal"
  }, {
    "count" : 1,
    "eventTime" : null,
    "firstTimestamp" : "2018-09-03T12:58:09Z",
    "involvedObject" : {
      "apiVersion" : "v1",
      "fieldPath" : "spec.containers{container-0}",
      "kind" : "Pod",
      "name" : "deployment-test-57f7cff77c-5x5tw",
      "namespace" : "namespace-test",
      "resourceVersion" : "5036870",
      "uid" : "010fec39-af79-11e8-8f17-c81fbe371a17"
    },
    "lastTimestamp" : "2018-09-03T12:58:09Z",
    "message" : "pulling image \"*.*.*.*:20202/cci/redis:V1\"",
    "metadata" : {
      "creationTimestamp" : "2018-09-03T12:58:09Z",
      "enable" : true,
      "name" : "deployment-test-57f7cff77c-5x5tw.1550e5354a5915e0",
      "namespace" : "namespace-test",
      "resourceVersion" : "760536",
      "selfLink" : "/api/v1/namespaces/namespace-test/events/deployment-test-57f7cff77c-5x5tw.1550e5354a5915e0",
      "uid" : "025554a4-af79-11e8-8f17-c81fbe371a17"
    },
    "reason" : "Pulling",
    "reportingComponent" : "",
    "reportingInstance" : "",
    "source" : {
      "component" : "kubelet",
      "host" : "c0dd6256-195a-e811-90a2-10c17294fcbc"
    },
    "type" : "Normal"
  } ],
  "kind" : "EventList",
  "metadata" : {
    "resourceVersion" : "764693",
    "selfLink" : "/api/v1/namespaces/namespace-test/events"
  }
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


