# 查询用户所有的Pods<a name="listCoreV1PodForAllNamespaces"></a>

## 功能介绍

该API用于获取一个Pod列表。

## 调试<a name="atuogenerate_1"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=CCI&api=listCoreV1PodForAllNamespaces)中调试该接口，支持自动认证鉴权。API Explorer可以自动生成SDK代码示例，并提供SDK代码示例调试功能。

## URI

GET /api/v1/pods

**表 1**  Query参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|continue|否|String|The continue option should be set when retrieving more results from the server. Since this value is server defined, clients may only use the continue value from a previous query result with identical query parameters (except for the value of continue) and the server may reject a continue value it does not recognize. If the specified continue value is no longer valid whether due to expiration (generally five to fifteen minutes) or a configuration change on the server the server will respond with a 410 ResourceExpired error indicating the client must restart their list without the continue field. This field is not supported when watch is true. Clients may start a watch from the last resourceVersion value returned by the server and not miss any modifications.|
|fieldSelector|否|String|A selector to restrict the list of returned objects by their fields. Defaults to everything.|
|includeUninitialized|否|Boolean|If true, partially initialized resources are included in the response.|
|labelSelector|否|String|A selector to restrict the list of returned objects by their labels. Defaults to everything.|
|limit|否|Integer|limit is a maximum number of responses to return for a list call. If more items exist, the server will set the *continue* field on the list metadata to a value that can be used with the same initial query to retrieve the next set of results. Setting a limit may return fewer than the requested amount of items (up to zero items) in the event all requested objects are filtered out and clients should only use the presence of the continue field to determine whether more results are available. Servers may choose not to support the limit argument and will return all of the available results. If limit is specified and the continue field is empty, clients may assume that no more results are available. This field is not supported if watch is true.The server guarantees that the objects returned when using continue will be identical to issuing a single list call without a limit - that is, no objects created, modified, or deleted after the first request is issued will be included in any subsequent continued requests. This is sometimes referred to as a consistent snapshot, and ensures that a client that is using limit to receive smaller chunks of a very large result can ensure they see all possible objects. If objects are updated during a chunked list the version of the object that was present at the time the first list result was calculated is returned.|
|pretty|否|String|If 'true', then the output is pretty printed.|
|resourceVersion|否|String|When specified with a watch call, shows changes that occur after that particular version of a resource. Defaults to changes from the beginning of history. When specified for list: - if unset, then the result is returned from remote storage based on quorum-read flag; - if it's 0, then we simply return what we currently have in cache, no guarantee; - if set to non zero, then the result is at least as fresh as given rv.|
|timeoutSeconds|否|Integer|Timeout for the list/watch call. This limits the duration of the call, regardless of any activity or inactivity.|
|watch|否|Boolean|Watch for changes to the described resources and return them as a stream of add, update, and remove notifications. Specify resourceVersion.|


## 请求参数

**表 2**  请求Header参数

|参数|是否必选|参数类型|描述|
|--|--|--|--|
|X-Auth-Token|是|String|用户Token。通过调用IAM服务获取用户Token接口获取（响应消息头中X-Subject-Token的值）。|


## 响应参数

**状态码： 200**

**表 3**  响应Body参数

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|items|Array of io.k8s.api.core.v1.Pod objects|List of pods. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta_v2 object|Standard list metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|


**表 4**  io.k8s.api.core.v1.Pod

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|APIVersion defines the versioned schema of this representation of an object. Servers should convert recognized schemas to the latest internal value, and may reject unrecognized values. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#resources|
|kind|String|Kind is a string value representing the REST resource this object represents. Servers may infer this from the endpoint the client submits requests to. Cannot be updated. In CamelCase. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|metadata|io.k8s.apimachinery.pkg.apis.meta.v1.ObjectMeta_v3 object|Standard object's metadata. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#metadata|
|spec|io.k8s.api.core.v1.PodSpec object|Specification of the desired behavpkg/controller/replicaset/replica_set_utils.goior of the pod. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|
|status|io.k8s.api.core.v1.PodStatus object|Most recently observed status of the pod. This data may not be up to date. Populated by the system. Read-only. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#spec-and-status|


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


**表 11**  io.k8s.apimachinery.pkg.apis.meta.v1.OwnerReference\_v2

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|blockOwnerDeletion|Boolean|If true, AND if the owner has the "foregroundDeletion" finalizer, then the owner cannot be deleted from the key-value store until this reference is removed. Defaults to false. To set this field, a user needs "delete" permission of the owner, otherwise 422 (Unprocessable Entity) will be returned.|
|controller|Boolean|If true, this reference points to the managing controller.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#names|
|uid|String|UID of the referent. More info: http://kubernetes.io/docs/user-guide/identifiers#uids|


**表 12**  io.k8s.api.core.v1.PodSpec

|参数|参数类型|描述|
|--|--|--|
|activeDeadlineSeconds|Long|Optional duration in seconds the pod may be active on the node relative to StartTime before the system will actively try to mark it failed and kill associated containers. Value must be a positive integer.|
|affinity|io.k8s.api.core.v1.Affinity object|If specified, the pod's scheduling constraints|
|automountServiceAccountToken|Boolean|AutomountServiceAccountToken indicates whether a service account token should be automatically mounted.|
|containers|Array of io.k8s.api.core.v1.Container objects|List of containers belonging to the pod. Containers cannot currently be added or removed. There must be at least one container in a Pod. Cannot be updated.|
|dnsConfig|io.k8s.api.core.v1.PodDNSConfig object|Specifies the DNS parameters of a pod. Parameters specified here will be merged to the generated DNS configuration based on DNSPolicy.|
|dnsPolicy|String|Set DNS policy for the pod. Defaults to "ClusterFirst". Valid values are 'ClusterFirstWithHostNet', 'ClusterFirst', 'Default' or 'None'. DNS parameters given in DNSConfig will be merged with the policy selected with DNSPolicy. To have DNS options set along with hostNetwork, you have to specify DNS policy explicitly to 'ClusterFirstWithHostNet'.|
|hostAliases|Array of io.k8s.api.core.v1.HostAlias objects|HostAliases is an optional list of hosts and IPs that will be injected into the pod's hosts file if specified. This is only valid for non-hostNetwork pods.|
|hostIPC|Boolean|Use the host's ipc namespace. Optional: Default to false.|
|hostNetwork|Boolean|Host networking requested for this pod. Use the host's network namespace. If this option is set, the ports that will be used must be specified. Default to false.|
|hostPID|Boolean|Use the host's pid namespace. Optional: Default to false.|
|hostname|String|Specifies the hostname of the Pod If not specified, the pod's hostname will be set to a system-defined value.|
|imagePullSecrets|Array of io.k8s.api.core.v1.LocalObjectReference objects|ImagePullSecrets is an optional list of references to secrets in the same namespace to use for pulling any of the images used by this PodSpec. If specified, these secrets will be passed to individual puller implementations for them to use. For example, in the case of docker, only DockerConfig type secrets are honored. More info: https://kubernetes.io/docs/concepts/containers/images#specifying-imagepullsecrets-on-a-pod|
|initContainers|Array of io.k8s.api.core.v1.Container objects|List of initialization containers belonging to the pod. Init containers are executed in order prior to containers being started. If any init container fails, the pod is considered to have failed and is handled according to its restartPolicy. The name for an init container or normal container must be unique among all containers. Init containers may not have Lifecycle actions, Readiness probes, or Liveness probes. The resourceRequirements of an init container are taken into account during scheduling by finding the highest request/limit for each resource type, and then using the max of of that value or the sum of the normal containers. Limits are applied to init containers in a similar fashion. Init containers cannot currently be added or removed. Cannot be updated. More info: https://kubernetes.io/docs/concepts/workloads/pods/init-containers/|
|nodeName|String|NodeName is a request to schedule this pod onto a specific node. If it is non-empty, the scheduler simply schedules this pod onto that node, assuming that it fits resource requirements.|
|nodeSelector|Map<String,String>|NodeSelector is a selector which must be true for the pod to fit on a node. Selector which must match a node's labels for the pod to be scheduled on that node. More info: https://kubernetes.io/docs/concepts/configuration/assign-pod-node/|
|priority|Integer|The priority value. Various system components use this field to find the priority of the pod. When Priority Admission Controller is enabled, it prevents users from setting this field. The admission controller populates this field from PriorityClassName. The higher the value, the higher the priority.|
|priorityClassName|String|If specified, indicates the pod's priority. "system-node-critical" and "system-cluster-critical" are two special keywords which indicate the highest priorities with the former being the highest priority. Any other name must be defined by creating a PriorityClass object with that name. If not specified, the pod priority will be default or zero if there is no default.|
|processes|Array of io.k8s.api.core.v1.Process objects|Processes is a request to deploy a pod in VMApplication|
|readinessGates|Array of io.k8s.api.core.v1.PodReadinessGate objects|If specified, all readiness gates will be evaluated for pod readiness. A pod is ready when all its containers are ready AND all conditions specified in the readiness gates have status equal to "True" More info: https://github.com/kubernetes/community/blob/master/keps/sig-network/0007-pod-ready%2B%2B.md|
|restartPolicy|String|Restart policy for all containers within the pod. One of Always, OnFailure, Never. Default to Always. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle/#restart-policy|
|schedulerName|String|If specified, the pod will be dispatched by specified scheduler. If not specified, the pod will be dispatched by default scheduler.|
|securityContext|io.k8s.api.core.v1.PodSecurityContext object|SecurityContext holds pod-level security attributes and common container settings. Optional: Defaults to empty.  See type description for default values of each field.|
|serviceAccount|String|DeprecatedServiceAccount is a depreciated alias for ServiceAccountName. Deprecated: Use serviceAccountName instead.|
|serviceAccountName|String|ServiceAccountName is the name of the ServiceAccount to use to run this pod. More info: https://kubernetes.io/docs/tasks/configure-pod-container/configure-service-account/|
|shareProcessNamespace|Boolean|Share a single process namespace between all of the containers in a pod. When this is set containers will be able to view and signal processes from other containers in the same pod, and the first process in each container will not be assigned PID 1. HostPID and ShareProcessNamespace cannot both be set. Optional: Default to false. This field is alpha-level and is honored only by servers that enable the PodShareProcessNamespace feature.|
|subdomain|String|If specified, the fully qualified Pod hostname will be "...svc.". If not specified, the pod will not have a domainname at all.|
|terminationGracePeriodSeconds|Long|Optional duration in seconds the pod needs to terminate gracefully. May be decreased in delete request. Value must be non-negative integer. The value zero indicates delete immediately. If this value is nil, the default grace period will be used instead. The grace period is the duration in seconds after the processes running in the pod are sent a termination signal and the time when the processes are forcibly halted with a kill signal. Set this value longer than the expected cleanup time for your process. Defaults to 30 seconds.|
|tolerations|Array of io.k8s.api.core.v1.Toleration objects|If specified, the pod's tolerations.|
|volumes|Array of io.k8s.api.core.v1.Volume objects|List of volumes that can be mounted by containers belonging to the pod. More info: https://kubernetes.io/docs/concepts/storage/volumes|


**表 13**  io.k8s.api.core.v1.Affinity

|参数|参数类型|描述|
|--|--|--|
|nodeAffinity|io.k8s.api.core.v1.NodeAffinity object|Describes node affinity scheduling rules for the pod.|
|podAffinity|io.k8s.api.core.v1.PodAffinity object|Describes pod affinity scheduling rules (e.g. co-locate this pod in the same node, zone, etc. as some other pod(s)).|
|podAntiAffinity|io.k8s.api.core.v1.PodAntiAffinity object|Describes pod anti-affinity scheduling rules (e.g. avoid putting this pod in the same node, zone, etc. as some other pod(s)).|


**表 14**  io.k8s.api.core.v1.NodeAffinity

|参数|参数类型|描述|
|--|--|--|
|preferredDuringSchedulingIgnoredDuringExecution|Array of io.k8s.api.core.v1.PreferredSchedulingTerm objects|The scheduler will prefer to schedule pods to nodes that satisfy the affinity expressions specified by this field, but it may choose a node that violates one or more of the expressions. The node that is most preferred is the one with the greatest sum of weights, i.e. for each node that meets all of the scheduling requirements (resource request, requiredDuringScheduling affinity expressions, etc.), compute a sum by iterating through the elements of this field and adding "weight" to the sum if the node matches the corresponding matchExpressions; the node(s) with the highest sum are the most preferred.|
|requiredDuringSchedulingIgnoredDuringExecution|io.k8s.api.core.v1.NodeSelector object|If the affinity requirements specified by this field are not met at scheduling time, the pod will not be scheduled onto the node. If the affinity requirements specified by this field cease to be met at some point during pod execution (e.g. due to an update), the system may or may not try to eventually evict the pod from its node.|


**表 15**  io.k8s.api.core.v1.PreferredSchedulingTerm

|参数|参数类型|描述|
|--|--|--|
|preference|io.k8s.api.core.v1.NodeSelectorTerm object|A node selector term, associated with the corresponding weight.|
|weight|Integer|Weight associated with matching the corresponding nodeSelectorTerm, in the range 1-100.|


**表 16**  io.k8s.api.core.v1.NodeSelectorTerm

|参数|参数类型|描述|
|--|--|--|
|matchExpressions|Array of io.k8s.api.core.v1.NodeSelectorRequirement objects|A list of node selector requirements by node's labels.|
|matchFields|Array of io.k8s.api.core.v1.NodeSelectorRequirement objects|A list of node selector requirements by node's fields.|


**表 17**  io.k8s.api.core.v1.NodeSelector

|参数|参数类型|描述|
|--|--|--|
|nodeSelectorTerms|Array of io.k8s.api.core.v1.NodeSelectorTerm objects|Required. A list of node selector terms. The terms are ORed.|


**表 18**  io.k8s.api.core.v1.NodeSelectorRequirement

|参数|参数类型|描述|
|--|--|--|
|key|String|The label key that the selector applies to.|
|operator|String|Represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists, DoesNotExist. Gt, and Lt.|
|values|Array of strings|An array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. If the operator is Gt or Lt, the values array must have a single element, which will be interpreted as an integer. This array is replaced during a strategic merge patch.|


**表 19**  io.k8s.api.core.v1.PodAffinity

|参数|参数类型|描述|
|--|--|--|
|preferredDuringSchedulingIgnoredDuringExecution|Array of io.k8s.api.core.v1.WeightedPodAffinityTerm objects|The scheduler will prefer to schedule pods to nodes that satisfy the affinity expressions specified by this field, but it may choose a node that violates one or more of the expressions. The node that is most preferred is the one with the greatest sum of weights, i.e. for each node that meets all of the scheduling requirements (resource request, requiredDuringScheduling affinity expressions, etc.), compute a sum by iterating through the elements of this field and adding "weight" to the sum if the node has pods which matches the corresponding podAffinityTerm; the node(s) with the highest sum are the most preferred.|
|requiredDuringSchedulingIgnoredDuringExecution|Array of io.k8s.api.core.v1.PodAffinityTerm objects|If the affinity requirements specified by this field are not met at scheduling time, the pod will not be scheduled onto the node. If the affinity requirements specified by this field cease to be met at some point during pod execution (e.g. due to a pod label update), the system may or may not try to eventually evict the pod from its node. When there are multiple elements, the lists of nodes corresponding to each podAffinityTerm are intersected, i.e. all terms must be satisfied.|


**表 20**  io.k8s.api.core.v1.PodAntiAffinity

|参数|参数类型|描述|
|--|--|--|
|preferredDuringSchedulingIgnoredDuringExecution|Array of io.k8s.api.core.v1.WeightedPodAffinityTerm objects|The scheduler will prefer to schedule pods to nodes that satisfy the anti-affinity expressions specified by this field, but it may choose a node that violates one or more of the expressions. The node that is most preferred is the one with the greatest sum of weights, i.e. for each node that meets all of the scheduling requirements (resource request, requiredDuringScheduling anti-affinity expressions, etc.), compute a sum by iterating through the elements of this field and adding "weight" to the sum if the node has pods which matches the corresponding podAffinityTerm; the node(s) with the highest sum are the most preferred.|
|requiredDuringSchedulingIgnoredDuringExecution|Array of io.k8s.api.core.v1.PodAffinityTerm objects|If the anti-affinity requirements specified by this field are not met at scheduling time, the pod will not be scheduled onto the node. If the anti-affinity requirements specified by this field cease to be met at some point during pod execution (e.g. due to a pod label update), the system may or may not try to eventually evict the pod from its node. When there are multiple elements, the lists of nodes corresponding to each podAffinityTerm are intersected, i.e. all terms must be satisfied.|


**表 21**  io.k8s.api.core.v1.WeightedPodAffinityTerm

|参数|参数类型|描述|
|--|--|--|
|podAffinityTerm|io.k8s.api.core.v1.PodAffinityTerm object|Required. A pod affinity term, associated with the corresponding weight.|
|weight|Integer|weight associated with matching the corresponding podAffinityTerm, in the range 1-100.|


**表 22**  io.k8s.api.core.v1.PodAffinityTerm

|参数|参数类型|描述|
|--|--|--|
|labelSelector|io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector object|A label query over a set of resources, in this case pods.|
|namespaces|Array of strings|namespaces specifies which namespaces the labelSelector applies to (matches against); null or empty list means "this pod's namespace"|
|numOfMatchingPods|String|NumOfMatchingPods specifies the minimal number of pod that matching the selector; the term is considered to be matched if and only if the matching number is larger than NumOfMatchingPods. The behavior is different when it is used with affinity vs. anti-affinity:When used with anti-affinity, a node N is eligible only if the number of pods matching the LabelSelector that are running on nodes with the same value for key TopologyKey as N has is less than NumOfMatchingPods. For example, if NumOfMatchingPods is 1 (the default), then after this pod is scheduled to node M, there will not be more than one pod from the set selected by the LabelSelector running on nodes with M's value for key TopologyKey.When used with affinity (not implemented yet), a node N is eligible only if the number of pods matching the LabelSelector that are running on nodes with the same value for key TopologyKey as N has is greater or equal to NumOfMatchingPods. For example, if NumOfMatchingPods is 1 (the default), then after this pod is scheduled to node M, there will be at least one pods from the set selected by the LabelSelector running on nodes with M's value for key TopologyKey. The default value is 1.|
|topologyKey|String|This pod should be co-located (affinity) or not co-located (anti-affinity) with the pods matching the labelSelector in the specified namespaces, where co-located is defined as running on a node whose value of the label with key topologyKey matches that of any node on which any of the selected pods is running. For PreferredDuringScheduling pod anti-affinity, empty topologyKey is interpreted as "all topologies" ("all topologies" here means all the topologyKeys indicated by scheduler command-line argument --failure-domains); for affinity and for RequiredDuringScheduling pod anti-affinity, empty topologyKey is not allowed.|


**表 23**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelector

|参数|参数类型|描述|
|--|--|--|
|matchExpressions|Array of io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement objects|matchExpressions is a list of label selector requirements. The requirements are ANDed.|
|matchLabels|Map<String,String>|matchLabels is a map of {key,value} pairs. A single {key,value} in the matchLabels map is equivalent to an element of matchExpressions, whose key field is "key", the operator is "In", and the values array contains only "value". The requirements are ANDed.|


**表 24**  io.k8s.apimachinery.pkg.apis.meta.v1.LabelSelectorRequirement

|参数|参数类型|描述|
|--|--|--|
|key|String|key is the label key that the selector applies to.|
|operator|String|operator represents a key's relationship to a set of values. Valid operators are In, NotIn, Exists and DoesNotExist.|
|values|Array of strings|values is an array of string values. If the operator is In or NotIn, the values array must be non-empty. If the operator is Exists or DoesNotExist, the values array must be empty. This array is replaced during a strategic merge patch.|


**表 25**  io.k8s.api.core.v1.PodDNSConfig

|参数|参数类型|描述|
|--|--|--|
|nameservers|Array of strings|A list of DNS name server IP addresses. This will be appended to the base nameservers generated from DNSPolicy. Duplicated nameservers will be removed.|
|options|Array of io.k8s.api.core.v1.PodDNSConfigOption objects|A list of DNS resolver options. This will be merged with the base options generated from DNSPolicy. Duplicated entries will be removed. Resolution options given in Options will override those that appear in the base DNSPolicy.|
|searches|Array of strings|A list of DNS search domains for host-name lookup. This will be appended to the base search paths generated from DNSPolicy. Duplicated search paths will be removed.|


**表 26**  io.k8s.api.core.v1.PodDNSConfigOption

|参数|参数类型|描述|
|--|--|--|
|name|String|Required.|
|value|String|value is the value of the option|


**表 27**  io.k8s.api.core.v1.HostAlias

|参数|参数类型|描述|
|--|--|--|
|hostnames|Array of strings|Hostnames for the above IP address.|
|ip|String|IP address of the host file entry.|


**表 28**  io.k8s.api.core.v1.LocalObjectReference

|参数|参数类型|描述|
|--|--|--|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|


**表 29**  io.k8s.api.core.v1.Container

|参数|参数类型|描述|
|--|--|--|
|args|Array of strings|Arguments to the entrypoint. The docker image's CMD is used if this is not provided. Variable references $(VAR_NAME) are expanded using the container's environment. If a variable cannot be resolved, the reference in the input string will be unchanged. The $(VAR_NAME) syntax can be escaped with a double $$, ie: $$(VAR_NAME). Escaped references will never be expanded, regardless of whether the variable exists or not. Cannot be updated. More info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell|
|command|Array of strings|Entrypoint array. Not executed within a shell. The docker image's ENTRYPOINT is used if this is not provided. Variable references $(VAR_NAME) are expanded using the container's environment. If a variable cannot be resolved, the reference in the input string will be unchanged. The $(VAR_NAME) syntax can be escaped with a double $$, ie: $$(VAR_NAME). Escaped references will never be expanded, regardless of whether the variable exists or not. Cannot be updated. More info: https://kubernetes.io/docs/tasks/inject-data-application/define-command-argument-container/#running-a-command-in-a-shell|
|env|Array of io.k8s.api.core.v1.EnvVar objects|List of environment variables to set in the container. Cannot be updated.|
|envFrom|Array of io.k8s.api.core.v1.EnvFromSource objects|List of sources to populate environment variables in the container. The keys defined within a source must be a C_IDENTIFIER. All invalid keys will be reported as an event when the container is starting. When a key exists in multiple sources, the value associated with the last source will take precedence. Values defined by an Env with a duplicate key will take precedence. Cannot be updated.|
|image|String|Docker image name. More info: https://kubernetes.io/docs/concepts/containers/images This field is optional to allow higher level config management to default or override container images in workload controllers like Deployments and StatefulSets.|
|imagePullPolicy|String|Image pull policy. One of Always, Never, IfNotPresent. Defaults to Always if :latest tag is specified, or IfNotPresent otherwise. Cannot be updated. More info: https://kubernetes.io/docs/concepts/containers/images#updating-images|
|lifecycle|io.k8s.api.core.v1.Lifecycle object|Actions that the management system should take in response to container lifecycle events. Cannot be updated.|
|livenessProbe|io.k8s.api.core.v1.Probe object|Periodic probe of container liveness. Container will be restarted if the probe fails. Cannot be updated. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes|
|name|String|Name of the container specified as a DNS_LABEL. Each container in a pod must have a unique name (DNS_LABEL). Cannot be updated.|
|ports|Array of io.k8s.api.core.v1.ContainerPort objects|List of ports to expose from the container. Exposing a port here gives the system additional information about the network connections a container uses, but is primarily informational. Not specifying a port here DOES NOT prevent that port from being exposed. Any port which is listening on the default "0.0.0.0" address inside a container will be accessible from the network. Cannot be updated.|
|readinessProbe|io.k8s.api.core.v1.Probe object|Periodic probe of container service readiness. Container will be removed from service endpoints if the probe fails. Cannot be updated. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes|
|resources|io.k8s.api.core.v1.ResourceRequirements object|Compute Resources required by this container. Cannot be updated. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#resources|
|securityContext|io.k8s.api.core.v1.SecurityContext object|Security options the pod should run with. More info: https://kubernetes.io/docs/concepts/policy/security-context/ More info: https://kubernetes.io/docs/tasks/configure-pod-container/security-context/|
|stdin|Boolean|Whether this container should allocate a buffer for stdin in the container runtime. If this is not set, reads from stdin in the container will always result in EOF. Default is false.|
|stdinOnce|Boolean|Whether the container runtime should close the stdin channel after it has been opened by a single attach. When stdin is true the stdin stream will remain open across multiple attach sessions. If stdinOnce is set to true, stdin is opened on container start, is empty until the first client attaches to stdin, and then remains open and accepts data until the client disconnects, at which time stdin is closed and remains closed until the container is restarted. If this flag is false, a container processes that reads from stdin will never receive an EOF. Default is false|
|terminationMessagePath|String|Optional: Path at which the file to which the container's termination message will be written is mounted into the container's filesystem. Message written is intended to be brief final status, such as an assertion failure message. Will be truncated by the node if greater than 4096 bytes. The total message length across all containers will be limited to 12kb. Defaults to /dev/termination-log. Cannot be updated.|
|terminationMessagePolicy|String|Indicate how the termination message should be populated. File will use the contents of terminationMessagePath to populate the container status message on both success and failure. FallbackToLogsOnError will use the last chunk of container log output if the termination message file is empty and the container exited with an error. The log output is limited to 2048 bytes or 80 lines, whichever is smaller. Defaults to File. Cannot be updated.|
|tty|Boolean|Whether this container should allocate a TTY for itself, also requires 'stdin' to be true. Default is false.|
|volumeDevices|Array of io.k8s.api.core.v1.VolumeDevice objects|volumeDevices is the list of block devices to be used by the container. This is an alpha feature and may change in the future.|
|volumeMounts|Array of io.k8s.api.core.v1.VolumeMount objects|Pod volumes to mount into the container's filesystem. Cannot be updated.|
|workingDir|String|Container's working directory. If not specified, the container runtime's default will be used, which might be configured in the container image. Cannot be updated.|


**表 30**  io.k8s.api.core.v1.EnvFromSource

|参数|参数类型|描述|
|--|--|--|
|configMapRef|io.k8s.api.core.v1.ConfigMapEnvSource object|The ConfigMap to select from|
|prefix|String|An optional identifier to prepend to each key in the ConfigMap. Must be a C_IDENTIFIER.|
|secretRef|io.k8s.api.core.v1.SecretEnvSource object|The Secret to select from|


**表 31**  io.k8s.api.core.v1.ConfigMapEnvSource

|参数|参数类型|描述|
|--|--|--|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|optional|Boolean|Specify whether the ConfigMap must be defined|


**表 32**  io.k8s.api.core.v1.SecretEnvSource

|参数|参数类型|描述|
|--|--|--|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|optional|Boolean|Specify whether the Secret must be defined|


**表 33**  io.k8s.api.core.v1.ContainerPort

|参数|参数类型|描述|
|--|--|--|
|containerPort|Integer|Number of port to expose on the pod's IP address. This must be a valid port number, 0 < x < 65536.|
|hostIP|String|What host IP to bind the external port to.|
|hostPort|Integer|Number of port to expose on the host. If specified, this must be a valid port number, 0 < x < 65536. If HostNetwork is specified, this must match ContainerPort. Most containers do not need this.|
|name|String|If specified, this must be an IANA_SVC_NAME and unique within the pod. Each named port in a pod must have a unique name. Name for the port that can be referred to by services.|
|protocol|String|Protocol for port. Must be UDP or TCP. Defaults to "TCP".|


**表 34**  io.k8s.api.core.v1.SecurityContext

|参数|参数类型|描述|
|--|--|--|
|allowPrivilegeEscalation|Boolean|AllowPrivilegeEscalation controls whether a process can gain more privileges than its parent process. This bool directly controls if the no_new_privs flag will be set on the container process. AllowPrivilegeEscalation is true always when the container is: 1) run as Privileged 2) has CAP_SYS_ADMIN|
|capabilities|io.k8s.api.core.v1.Capabilities object|The capabilities to add/drop when running containers. Defaults to the default set of capabilities granted by the container runtime.|
|privileged|Boolean|Run container in privileged mode. Processes in privileged containers are essentially equivalent to root on the host. Defaults to false.|
|readOnlyRootFilesystem|Boolean|Whether this container has a read-only root filesystem. Default is false.|
|runAsGroup|Long|The GID to run the entrypoint of the container process. Uses runtime default if unset. May also be set in PodSecurityContext. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence.|
|runAsNonRoot|Boolean|Indicates that the container must run as a non-root user. If true, the Kubelet will validate the image at runtime to ensure that it does not run as UID 0 (root) and fail to start the container if it does. If unset or false, no such validation will be performed. May also be set in PodSecurityContext. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence.|
|runAsUser|Long|The UID to run the entrypoint of the container process. Defaults to user specified in image metadata if unspecified. May also be set in PodSecurityContext. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence.|
|seLinuxOptions|io.k8s.api.core.v1.SELinuxOptions object|The SELinux context to be applied to the container. If unspecified, the container runtime will allocate a random SELinux context for each container. May also be set in PodSecurityContext. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence.|


**表 35**  io.k8s.api.core.v1.Capabilities

|参数|参数类型|描述|
|--|--|--|
|add|Array of strings|Added capabilities|
|drop|Array of strings|Removed capabilities|


**表 36**  io.k8s.api.core.v1.VolumeDevice

|参数|参数类型|描述|
|--|--|--|
|devicePath|String|devicePath is the path inside of the container that the device will be mapped to.|
|name|String|name must match the name of a persistentVolumeClaim in the pod|


**表 37**  io.k8s.api.core.v1.Process

|参数|参数类型|描述|
|--|--|--|
|depends|Array of strings|Process depends: define the installation order|
|env|Array of io.k8s.api.core.v1.EnvVar objects|The env in one VM application|
|lifecycle|io.k8s.api.core.v1.Lifecycle object|Actions that the management system should take in response to process lifecycle events. Cannot be updated.|
|lifecyclePlan|io.k8s.api.core.v1.ObjectReference object|Actions that the management system should take in response to process lifecycle events. User can redefine|
|livenessProbe|io.k8s.api.core.v1.Probe object|Periodic probe of process liveness. Process will be restarted if the probe fails. Cannot be updated.|
|name|String|Each Process in a pod must have a unique name.|
|package|String|Required: Package is the resource/location of VM application installation package Package is a url to download the package, should not be blank|
|processPorts|Array of io.k8s.api.core.v1.Port objects|The process ports in the VM application|
|readinessProbe|io.k8s.api.core.v1.Probe object|Periodic probe of process service readiness. process will be removed from service endpoints if the probe fails.|
|resources|io.k8s.api.core.v1.ResourceRequirements object|Compute resource requirements.|
|runtime|Array of strings|Process runtime: define the installation mode.|
|volumeMounts|Array of io.k8s.api.core.v1.VolumeMount objects|Pod volumes to mount into the process's filesyste. Cannot be updated.|


**表 38**  io.k8s.api.core.v1.EnvVar

|参数|参数类型|描述|
|--|--|--|
|name|String|Name of the environment variable. Must be a C_IDENTIFIER.|
|value|String|Variable references $(VAR_NAME) are expanded using the previous defined environment variables in the container and any service environment variables. If a variable cannot be resolved, the reference in the input string will be unchanged. The $(VAR_NAME) syntax can be escaped with a double $$, ie: $$(VAR_NAME). Escaped references will never be expanded, regardless of whether the variable exists or not. Defaults to "".|
|valueFrom|io.k8s.api.core.v1.EnvVarSource object|Source for the environment variable's value. Cannot be used if value is not empty.|


**表 39**  io.k8s.api.core.v1.EnvVarSource

|参数|参数类型|描述|
|--|--|--|
|configMapKeyRef|io.k8s.api.core.v1.ConfigMapKeySelector object|Selects a key of a ConfigMap.|
|fieldRef|io.k8s.api.core.v1.ObjectFieldSelector object|Selects a field of the pod: supports metadata.name, metadata.namespace, metadata.labels, metadata.annotations, spec.nodeName, spec.serviceAccountName, status.hostIP, status.podIP.|
|processResourceFieldRef|io.k8s.api.core.v1.ProcessResourceFieldSelector object|Selects a resource of the process: only resources limits and requests (limits.cpu, limits.memory, requests.cpu and requests.memory) are currently supported.|
|resourceFieldRef|io.k8s.api.core.v1.ResourceFieldSelector object|Selects a resource of the container: only resources limits and requests (limits.cpu, limits.memory, limits.ephemeral-storage, requests.cpu, requests.memory and requests.ephemeral-storage) are currently supported.|
|secretKeyRef|io.k8s.api.core.v1.SecretKeySelector object|Selects a key of a secret in the pod's namespace|


**表 40**  io.k8s.api.core.v1.ConfigMapKeySelector

|参数|参数类型|描述|
|--|--|--|
|key|String|The key to select.|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|optional|Boolean|Specify whether the ConfigMap or it's key must be defined|


**表 41**  io.k8s.api.core.v1.ProcessResourceFieldSelector

|参数|参数类型|描述|
|--|--|--|
|divisor|String|Specifies the output format of the exposed resources, defaults to "1"|
|processName|String|Process name: required for volumes, optional for env vars|
|resource|String|Required: resource to select|


**表 42**  io.k8s.api.core.v1.SecretKeySelector

|参数|参数类型|描述|
|--|--|--|
|key|String|The key of the secret to select from. Must be a valid secret key.|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|optional|Boolean|Specify whether the Secret or it's key must be defined|


**表 43**  io.k8s.api.core.v1.Lifecycle

|参数|参数类型|描述|
|--|--|--|
|active|io.k8s.api.core.v1.Handler object|Active is called to change a container/process from standby mode to active mode. The reason for termination is passed to the handler.|
|configure|io.k8s.api.core.v1.Handler object|Configure is called immediately before a container/process started. The reason for termination is passed to the handler.|
|install|io.k8s.api.core.v1.Handler object|Install is called immediately after a container/process created. The reason for termination is passed to the handler.|
|postStart|io.k8s.api.core.v1.Handler object|PostStart is called immediately after a container is created. If the handler fails, the container is terminated and restarted according to its restart policy. Other management of the container blocks until the hook completes. More info: https://kubernetes.io/docs/concepts/containers/container-lifecycle-hooks/#container-hooks|
|preStop|io.k8s.api.core.v1.Handler object|PreStop is called immediately before a container is terminated. The container is terminated after the handler completes. The reason for termination is passed to the handler. Regardless of the outcome of the handler, the container is eventually terminated. Other management of the container blocks until the hook completes. More info: https://kubernetes.io/docs/concepts/containers/container-lifecycle-hooks/#container-hooks|
|reconfigure|io.k8s.api.core.v1.Handler object|Reconfigure is called when ConfigMap changed. The reason for termination is passed to the handler.|
|restart|io.k8s.api.core.v1.Handler object|Restart is called to restart a container/process. The reason for termination is passed to the handler.|
|rollback|io.k8s.api.core.v1.Handler object|Rollback is called to rollback a container/process. The reason for termination is passed to the handler.|
|scaleIn|io.k8s.api.core.v1.Handler object|ScaleIn is called when pod instance decreased. The reason for termination is passed to the handler.|
|scaleOut|io.k8s.api.core.v1.Handler object|ScaleOut is called when pod instance increased. The reason for termination is passed to the handler.|
|standby|io.k8s.api.core.v1.Handler object|Standby is called to change a container/process from active mode to standby mode. The reason for termination is passed to the handler.|
|start|io.k8s.api.core.v1.Handler object|Start is used to start a container/process. The reason for termination is passed to the handler.|
|stop|io.k8s.api.core.v1.Handler object|Stop is called to stop a container/process. The reason for termination is passed to the handler.|
|uninstall|io.k8s.api.core.v1.Handler object|Uninstall is called immediately before a container/process destroyed. The reason for termination is passed to the handler.|
|update|io.k8s.api.core.v1.Handler object|Update is called to update a container/process. The reason for termination is passed to the handler.|


**表 44**  io.k8s.api.core.v1.Handler

|参数|参数类型|描述|
|--|--|--|
|exec|io.k8s.api.core.v1.ExecAction object|One and only one of the following should be specified. Exec specifies the action to take.|
|httpGet|io.k8s.api.core.v1.HTTPGetAction object|HTTPGet specifies the http request to perform.|
|tcpSocket|io.k8s.api.core.v1.TCPSocketAction object|TCPSocket specifies an action involving a TCP port. TCP hooks not yet supported|


**表 45**  io.k8s.api.core.v1.ObjectReference

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|API version of the referent.|
|fieldPath|String|If referring to a piece of an object instead of an entire object, this string should contain a valid JSON/Go field access statement, such as desiredState.manifest.containers[2]. For example, if the object reference is to a container within a pod, this would take on a value like: "spec.containers{name}" (where "name" refers to the name of the container that triggered the event) or if no container name is specified "spec.containers[2]" (container with index 2 in this pod). This syntax is chosen only to have some well-defined way of referencing a part of an object.|
|kind|String|Kind of the referent. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#types-kinds|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|namespace|String|Namespace of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/namespaces/|
|resourceVersion|String|Specific resourceVersion to which this reference is made, if any. More info: https://git.k8s.io/community/contributors/devel/api-conventions.md#concurrency-control-and-consistency|
|uid|String|UID of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#uids|


**表 46**  io.k8s.api.core.v1.Port

|参数|参数类型|描述|
|--|--|--|
|name|String|If specified, this must be an IANA_SVC_NAME and unique within the pod. Each named port in a pod must have a unique name. Name for the port that can be referred to by services.|
|port|Integer|Number of port to expose on the pod's IP address. This must be a valid port number, 0 < x < 65536.|
|protocol|String|Protocol for port. Must be UDP or TCP. Defaults to "TCP".|


**表 47**  io.k8s.api.core.v1.Probe

|参数|参数类型|描述|
|--|--|--|
|exec|io.k8s.api.core.v1.ExecAction object|One and only one of the following should be specified. Exec specifies the action to take.|
|failureThreshold|Integer|Minimum consecutive failures for the probe to be considered failed after having succeeded. Defaults to 3. Minimum value is 1.|
|httpGet|io.k8s.api.core.v1.HTTPGetAction object|HTTPGet specifies the http request to perform.|
|initialDelaySeconds|Integer|Number of seconds after the container has started before liveness probes are initiated. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes|
|periodSeconds|Integer|How often (in seconds) to perform the probe. Default to 10 seconds. Minimum value is 1.|
|successThreshold|Integer|Minimum consecutive successes for the probe to be considered successful after having failed. Defaults to 1. Must be 1 for liveness. Minimum value is 1.|
|tcpSocket|io.k8s.api.core.v1.TCPSocketAction object|TCPSocket specifies an action involving a TCP port. TCP hooks not yet supported|
|timeoutSeconds|Integer|Number of seconds after which the probe times out. Defaults to 1 second. Minimum value is 1. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#container-probes|


**表 48**  io.k8s.api.core.v1.ExecAction

|参数|参数类型|描述|
|--|--|--|
|command|Array of strings|Command is the command line to execute inside the container, the working directory for the command is root ('/') in the container's filesystem. The command is simply exec'd, it is not run inside a shell, so traditional shell instructions ('|', etc) won't work. To use a shell, you need to explicitly call out to that shell. Exit status of 0 is treated as live/healthy and non-zero is unhealthy.|


**表 49**  io.k8s.api.core.v1.HTTPGetAction

|参数|参数类型|描述|
|--|--|--|
|host|String|Host name to connect to, defaults to the pod IP. You probably want to set "Host" in httpHeaders instead.|
|httpHeaders|Array of io.k8s.api.core.v1.HTTPHeader objects|Custom headers to set in the request. HTTP allows repeated headers.|
|path|String|Path to access on the HTTP server.|
|port|String|Name or number of the port to access on the container. Number must be in the range 1 to 65535. Name must be an IANA_SVC_NAME.|
|scheme|String|Scheme to use for connecting to the host. Defaults to HTTP.|


**表 50**  io.k8s.api.core.v1.HTTPHeader

|参数|参数类型|描述|
|--|--|--|
|name|String|The header field name|
|value|String|The header field value|


**表 51**  io.k8s.api.core.v1.TCPSocketAction

|参数|参数类型|描述|
|--|--|--|
|host|String|Optional: Host name to connect to, defaults to the pod IP.|
|port|String|Number or name of the port to access on the container. Number must be in the range 1 to 65535. Name must be an IANA_SVC_NAME.|


**表 52**  io.k8s.api.core.v1.ResourceRequirements

|参数|参数类型|描述|
|--|--|--|
|limits|Map<String,String>|Limits describes the maximum amount of compute resources allowed. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|
|requests|Map<String,String>|Requests describes the minimum amount of compute resources required. If Requests is omitted for a container, it defaults to Limits if that is explicitly specified, otherwise to an implementation-defined value. More info: https://kubernetes.io/docs/concepts/configuration/manage-compute-resources-container/|


**表 53**  io.k8s.api.core.v1.VolumeMount

|参数|参数类型|描述|
|--|--|--|
|extendPathMode|String|Extend the volume path by appending the pod metadata to the path according to specified pattern. which provide a way of directory isolation and help prevent the writing conflict between different pods.|
|mountPath|String|Path within the container at which the volume should be mounted. Must not contain ':'.|
|mountPropagation|String|mountPropagation determines how mounts are propagated from the host to container and the other way around. When not set, MountPropagationNone is used. This field is beta in 1.10.|
|name|String|This must match the Name of a Volume.|
|policy|io.k8s.api.core.v1.Policy object|VolumeMount Policy.|
|readOnly|Boolean|Mounted read-only if true, read-write otherwise (false or unspecified). Defaults to false.|
|subPath|String|Path within the volume from which the container's volume should be mounted. Defaults to "" (volume's root).|


**表 54**  io.k8s.api.core.v1.Policy

|参数|参数类型|描述|
|--|--|--|
|logs|io.k8s.api.core.v1.Logs object|Logs describes log Volume and its rotate strategy.|


**表 55**  io.k8s.api.core.v1.Logs

|参数|参数类型|描述|
|--|--|--|
|annotations|Map<String,String>|Annotations for log.|
|rotate|String|Rotate strategy, including 'Daily' 'Hourly' 'Weekly'.|


**表 56**  io.k8s.api.core.v1.PodReadinessGate

|参数|参数类型|描述|
|--|--|--|
|conditionType|String|ConditionType refers to a condition in the pod's condition list with matching type.|


**表 57**  io.k8s.api.core.v1.PodSecurityContext

|参数|参数类型|描述|
|--|--|--|
|fsGroup|Long|A special supplemental group that applies to all containers in a pod. Some volume types allow the Kubelet to change the ownership of that volume to be owned by the pod:The owning GID will be the FSGroup 2. The setgid bit is set (new files created in the volume will be owned by FSGroup) 3. The permission bits are OR'd with rw-rw----If unset, the Kubelet will not modify the ownership and permissions of any volume.|
|fsOwner|Long|A special supplemental owner that applies to all containers in a pod. Some volume types allow the Kubelet to change the ownership of that volume to be owned by the pod:The owning UID will be the FSOwner 2. The setgid bit is set (new files created in the volume will be owned by FSOwner) 3. The permission bits are OR'd with rw-------If unset, the Kubelet will not modify the ownership and permissions of any volume.|
|runAsGroup|Long|The GID to run the entrypoint of the container process. Uses runtime default if unset. May also be set in SecurityContext. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence for that container.|
|runAsNonRoot|Boolean|Indicates that the container must run as a non-root user. If true, the Kubelet will validate the image at runtime to ensure that it does not run as UID 0 (root) and fail to start the container if it does. If unset or false, no such validation will be performed. May also be set in SecurityContext. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence.|
|runAsUser|Long|The UID to run the entrypoint of the container process. Defaults to user specified in image metadata if unspecified. May also be set in SecurityContext. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence for that container.|
|seLinuxOptions|io.k8s.api.core.v1.SELinuxOptions object|The SELinux context to be applied to all containers. If unspecified, the container runtime will allocate a random SELinux context for each container. May also be set in SecurityContext. If set in both SecurityContext and PodSecurityContext, the value specified in SecurityContext takes precedence for that container.|
|supplementalGroups|Array of integers|A list of groups applied to the first process run in each container, in addition to the container's primary GID. If unspecified, no groups will be added to any container.|
|sysctls|Array of io.k8s.api.core.v1.Sysctl objects|Sysctls hold a list of namespaced sysctls used for the pod. Pods with unsupported sysctls (by the container runtime) might fail to launch.|


**表 58**  io.k8s.api.core.v1.SELinuxOptions

|参数|参数类型|描述|
|--|--|--|
|level|String|Level is SELinux level label that applies to the container.|
|role|String|Role is a SELinux role label that applies to the container.|
|type|String|Type is a SELinux type label that applies to the container.|
|user|String|User is a SELinux user label that applies to the container.|


**表 59**  io.k8s.api.core.v1.Sysctl

|参数|参数类型|描述|
|--|--|--|
|name|String|Name of a property to set|
|value|String|Value of a property to set|


**表 60**  io.k8s.api.core.v1.Toleration

|参数|参数类型|描述|
|--|--|--|
|effect|String|Effect indicates the taint effect to match. Empty means match all taint effects. When specified, allowed values are NoSchedule, PreferNoSchedule and NoExecute.|
|key|String|Key is the taint key that the toleration applies to. Empty means match all taint keys. If the key is empty, operator must be Exists; this combination means to match all values and all keys.|
|operator|String|Operator represents a key's relationship to the value. Valid operators are Exists and Equal. Defaults to Equal. Exists is equivalent to wildcard for value, so that a pod can tolerate all taints of a particular category.|
|tolerationSeconds|Long|TolerationSeconds represents the period of time the toleration (which must be of effect NoExecute, otherwise this field is ignored) tolerates the taint. By default, it is not set, which means tolerate the taint forever (do not evict). Zero and negative values will be treated as 0 (evict immediately) by the system.|
|value|String|Value is the taint value the toleration matches to. If the operator is Exists, the value should be empty, otherwise just a regular string.|


**表 61**  io.k8s.api.core.v1.Volume

|参数|参数类型|描述|
|--|--|--|
|awsElasticBlockStore|io.k8s.api.core.v1.AWSElasticBlockStoreVolumeSource object|AWSElasticBlockStore represents an AWS Disk resource that is attached to a kubelet's host machine and then exposed to the pod. More info: https://kubernetes.io/docs/concepts/storage/volumes#awselasticblockstore|
|azureDisk|io.k8s.api.core.v1.AzureDiskVolumeSource object|AzureDisk represents an Azure Data Disk mount on the host and bind mount to the pod.|
|azureFile|io.k8s.api.core.v1.AzureFileVolumeSource object|AzureFile represents an Azure File Service mount on the host and bind mount to the pod.|
|cephfs|io.k8s.api.core.v1.CephFSVolumeSource object|CephFS represents a Ceph FS mount on the host that shares a pod's lifetime|
|cinder|io.k8s.api.core.v1.CinderVolumeSource object|Cinder represents a cinder volume attached and mounted on kubelets host machine More info: https://releases.k8s.io/HEAD/examples/mysql-cinder-pd/README.md|
|configMap|io.k8s.api.core.v1.ConfigMapVolumeSource object|ConfigMap represents a configMap that should populate this volume|
|downwardAPI|io.k8s.api.core.v1.DownwardAPIVolumeSource object|DownwardAPI represents downward API about the pod that should populate this volume|
|emptyDir|io.k8s.api.core.v1.EmptyDirVolumeSource object|EmptyDir represents a temporary directory that shares a pod's lifetime. More info: https://kubernetes.io/docs/concepts/storage/volumes#emptydir|
|fc|io.k8s.api.core.v1.FCVolumeSource object|FC represents a Fibre Channel resource that is attached to a kubelet's host machine and then exposed to the pod.|
|flexVolume|io.k8s.api.core.v1.FlexVolumeSource object|FlexVolume represents a generic volume resource that is provisioned/attached using an exec based plugin.|
|flocker|io.k8s.api.core.v1.FlockerVolumeSource object|Flocker represents a Flocker volume attached to a kubelet's host machine. This depends on the Flocker control service being running|
|gcePersistentDisk|io.k8s.api.core.v1.GCEPersistentDiskVolumeSource object|GCEPersistentDisk represents a GCE Disk resource that is attached to a kubelet's host machine and then exposed to the pod. More info: https://kubernetes.io/docs/concepts/storage/volumes#gcepersistentdisk|
|gitRepo|io.k8s.api.core.v1.GitRepoVolumeSource object|GitRepo represents a git repository at a particular revision. DEPRECATED: GitRepo is deprecated. To provision a container with a git repo, mount an EmptyDir into an InitContainer that clones the repo using git, then mount the EmptyDir into the Pod's container.|
|glusterfs|io.k8s.api.core.v1.GlusterfsVolumeSource object|Glusterfs represents a Glusterfs mount on the host that shares a pod's lifetime. More info: https://releases.k8s.io/HEAD/examples/volumes/glusterfs/README.md|
|hostPath|io.k8s.api.core.v1.HostPathVolumeSource object|HostPath represents a pre-existing file or directory on the host machine that is directly exposed to the container. This is generally used for system agents or other privileged things that are allowed to see the host machine. Most containers will NOT need this. More info: https://kubernetes.io/docs/concepts/storage/volumes#hostpath|
|iscsi|io.k8s.api.core.v1.ISCSIVolumeSource object|ISCSI represents an ISCSI Disk resource that is attached to a kubelet's host machine and then exposed to the pod. More info: https://releases.k8s.io/HEAD/examples/volumes/iscsi/README.md|
|localDir|io.k8s.api.core.v1.LocalDirVolumeSource object|LocalDir represents a LocalDir volume that is created by LVM and mounted into the pod|
|name|String|Volume's name. Must be a DNS_LABEL and unique within the pod. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|nfs|io.k8s.api.core.v1.NFSVolumeSource object|NFS represents an NFS mount on the host that shares a pod's lifetime More info: https://kubernetes.io/docs/concepts/storage/volumes#nfs|
|persistentVolumeClaim|io.k8s.api.core.v1.PersistentVolumeClaimVolumeSource object|PersistentVolumeClaimVolumeSource represents a reference to a PersistentVolumeClaim in the same namespace. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|
|photonPersistentDisk|io.k8s.api.core.v1.PhotonPersistentDiskVolumeSource object|PhotonPersistentDisk represents a PhotonController persistent disk attached and mounted on kubelets host machine|
|portworxVolume|io.k8s.api.core.v1.PortworxVolumeSource object|PortworxVolume represents a portworx volume attached and mounted on kubelets host machine|
|projected|io.k8s.api.core.v1.ProjectedVolumeSource object|Items for all in one resources secrets, configmaps, and downward API|
|quobyte|io.k8s.api.core.v1.QuobyteVolumeSource object|Quobyte represents a Quobyte mount on the host that shares a pod's lifetime|
|rbd|io.k8s.api.core.v1.RBDVolumeSource object|RBD represents a Rados Block Device mount on the host that shares a pod's lifetime. More info: https://releases.k8s.io/HEAD/examples/volumes/rbd/README.md|
|scaleIO|io.k8s.api.core.v1.ScaleIOVolumeSource object|ScaleIO represents a ScaleIO persistent volume attached and mounted on Kubernetes nodes.|
|secret|io.k8s.api.core.v1.SecretVolumeSource object|Secret represents a secret that should populate this volume. More info: https://kubernetes.io/docs/concepts/storage/volumes#secret|
|storageos|io.k8s.api.core.v1.StorageOSVolumeSource object|StorageOS represents a StorageOS volume attached and mounted on Kubernetes nodes.|
|vsphereVolume|io.k8s.api.core.v1.VsphereVirtualDiskVolumeSource object|VsphereVolume represents a vSphere volume attached and mounted on kubelets host machine|


**表 62**  io.k8s.api.core.v1.AWSElasticBlockStoreVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|Filesystem type of the volume that you want to mount. Tip: Ensure that the filesystem type is supported by the host operating system. Examples: "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified. More info: https://kubernetes.io/docs/concepts/storage/volumes#awselasticblockstore|
|partition|Integer|The partition in the volume that you want to mount. If omitted, the default is to mount by volume name. Examples: For volume /dev/sda1, you specify the partition as "1". Similarly, the volume partition for /dev/sda is "0" (or you can leave the property empty).|
|readOnly|Boolean|Specify "true" to force and set the ReadOnly property in VolumeMounts to "true". If omitted, the default is "false". More info: https://kubernetes.io/docs/concepts/storage/volumes#awselasticblockstore|
|volumeID|String|Unique ID of the persistent disk resource in AWS (Amazon EBS volume). More info: https://kubernetes.io/docs/concepts/storage/volumes#awselasticblockstore|


**表 63**  io.k8s.api.core.v1.AzureDiskVolumeSource

|参数|参数类型|描述|
|--|--|--|
|cachingMode|String|Host Caching mode: None, Read Only, Read Write.|
|diskName|String|The Name of the data disk in the blob storage|
|diskURI|String|The URI the data disk in the blob storage|
|fsType|String|Filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified.|
|kind|String|Expected values Shared: multiple blob disks per storage account  Dedicated: single blob disk per storage account  Managed: azure managed data disk (only in managed availability set). defaults to shared|
|readOnly|Boolean|Defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts.|


**表 64**  io.k8s.api.core.v1.AzureFileVolumeSource

|参数|参数类型|描述|
|--|--|--|
|readOnly|Boolean|Defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts.|
|secretName|String|the name of secret that contains Azure Storage Account Name and Key|
|shareName|String|Share Name|


**表 65**  io.k8s.api.core.v1.CephFSVolumeSource

|参数|参数类型|描述|
|--|--|--|
|monitors|Array of strings|Required: Monitors is a collection of Ceph monitors More info: https://releases.k8s.io/HEAD/examples/volumes/cephfs/README.md#how-to-use-it|
|path|String|Optional: Used as the mounted root, rather than the full Ceph tree, default is /|
|readOnly|Boolean|Optional: Defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts. More info: https://releases.k8s.io/HEAD/examples/volumes/cephfs/README.md#how-to-use-it|
|secretFile|String|Optional: SecretFile is the path to key ring for User, default is /etc/ceph/user.secret More info: https://releases.k8s.io/HEAD/examples/volumes/cephfs/README.md#how-to-use-it|
|secretRef|io.k8s.api.core.v1.LocalObjectReference object|Optional: SecretRef is reference to the authentication secret for User, default is empty. More info: https://releases.k8s.io/HEAD/examples/volumes/cephfs/README.md#how-to-use-it|
|user|String|Optional: User is the rados user name, default is admin More info: https://releases.k8s.io/HEAD/examples/volumes/cephfs/README.md#how-to-use-it|


**表 66**  io.k8s.api.core.v1.CinderVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|Filesystem type to mount. Must be a filesystem type supported by the host operating system. Examples: "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified. More info: https://releases.k8s.io/HEAD/examples/mysql-cinder-pd/README.md|
|readOnly|Boolean|Optional: Defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts. More info: https://releases.k8s.io/HEAD/examples/mysql-cinder-pd/README.md|
|secretRef|io.k8s.api.core.v1.LocalObjectReference object|Optional: points to a secret object containing parameters used to connect to OpenStack.|
|volumeID|String|volume id used to identify the volume in cinder More info: https://releases.k8s.io/HEAD/examples/mysql-cinder-pd/README.md|


**表 67**  io.k8s.api.core.v1.ConfigMapVolumeSource

|参数|参数类型|描述|
|--|--|--|
|defaultMode|Integer|Optional: mode bits to use on created files by default. Must be a value between 0 and 0777. Defaults to 0644. Directories within the path are not affected by this setting. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set.|
|items|Array of io.k8s.api.core.v1.KeyToPath objects|If unspecified, each key-value pair in the Data field of the referenced ConfigMap will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the ConfigMap, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'.|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|optional|Boolean|Specify whether the ConfigMap or it's keys must be defined|


**表 68**  io.k8s.api.core.v1.DownwardAPIVolumeSource

|参数|参数类型|描述|
|--|--|--|
|defaultMode|Integer|Optional: mode bits to use on created files by default. Must be a value between 0 and 0777. Defaults to 0644. Directories within the path are not affected by this setting. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set.|
|items|Array of io.k8s.api.core.v1.DownwardAPIVolumeFile objects|Items is a list of downward API volume file|


**表 69**  io.k8s.api.core.v1.EmptyDirVolumeSource

|参数|参数类型|描述|
|--|--|--|
|medium|String|What type of storage medium should back this directory. The default is "" which means to use the node's default medium. Must be an empty string (default) or Memory. More info: https://kubernetes.io/docs/concepts/storage/volumes#emptydir|
|sizeLimit|String|Total amount of local storage required for this EmptyDir volume. The size limit is also applicable for memory medium. The maximum usage on memory medium EmptyDir would be the minimum value between the SizeLimit specified here and the sum of memory limits of all containers in a pod. The default is nil which means that the limit is undefined. More info: http://kubernetes.io/docs/user-guide/volumes#emptydir|


**表 70**  io.k8s.api.core.v1.FCVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|Filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified.|
|lun|Integer|Optional: FC target lun number|
|readOnly|Boolean|Optional: Defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts.|
|targetWWNs|Array of strings|Optional: FC target worldwide names (WWNs)|
|wwids|Array of strings|Optional: FC volume world wide identifiers (wwids) Either wwids or combination of targetWWNs and lun must be set, but not both simultaneously.|


**表 71**  io.k8s.api.core.v1.FlexVolumeSource

|参数|参数类型|描述|
|--|--|--|
|driver|String|Driver is the name of the driver to use for this volume.|
|fsType|String|Filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. "ext4", "xfs", "ntfs". The default filesystem depends on FlexVolume script.|
|options|Map<String,String>|Optional: Extra command options if any.|
|readOnly|Boolean|Optional: Defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts.|
|secretRef|io.k8s.api.core.v1.LocalObjectReference object|Optional: SecretRef is reference to the secret object containing sensitive information to pass to the plugin scripts. This may be empty if no secret object is specified. If the secret object contains more than one secret, all secrets are passed to the plugin scripts.|


**表 72**  io.k8s.api.core.v1.FlockerVolumeSource

|参数|参数类型|描述|
|--|--|--|
|datasetName|String|Name of the dataset stored as metadata -> name on the dataset for Flocker should be considered as deprecated|
|datasetUUID|String|UUID of the dataset. This is unique identifier of a Flocker dataset|


**表 73**  io.k8s.api.core.v1.GCEPersistentDiskVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|Filesystem type of the volume that you want to mount. Tip: Ensure that the filesystem type is supported by the host operating system. Examples: "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified. More info: https://kubernetes.io/docs/concepts/storage/volumes#gcepersistentdisk|
|partition|Integer|The partition in the volume that you want to mount. If omitted, the default is to mount by volume name. Examples: For volume /dev/sda1, you specify the partition as "1". Similarly, the volume partition for /dev/sda is "0" (or you can leave the property empty). More info: https://kubernetes.io/docs/concepts/storage/volumes#gcepersistentdisk|
|pdName|String|Unique name of the PD resource in GCE. Used to identify the disk in GCE. More info: https://kubernetes.io/docs/concepts/storage/volumes#gcepersistentdisk|
|readOnly|Boolean|ReadOnly here will force the ReadOnly setting in VolumeMounts. Defaults to false. More info: https://kubernetes.io/docs/concepts/storage/volumes#gcepersistentdisk|


**表 74**  io.k8s.api.core.v1.GitRepoVolumeSource

|参数|参数类型|描述|
|--|--|--|
|directory|String|Target directory name. Must not contain or start with '..'. If '.' is supplied, the volume directory will be the git repository. Otherwise, if specified, the volume will contain the git repository in the subdirectory with the given name.|
|repository|String|Repository URL|
|revision|String|Commit hash for the specified revision.|


**表 75**  io.k8s.api.core.v1.GlusterfsVolumeSource

|参数|参数类型|描述|
|--|--|--|
|endpoints|String|EndpointsName is the endpoint name that details Glusterfs topology. More info: https://releases.k8s.io/HEAD/examples/volumes/glusterfs/README.md#create-a-pod|
|path|String|Path is the Glusterfs volume path. More info: https://releases.k8s.io/HEAD/examples/volumes/glusterfs/README.md#create-a-pod|
|readOnly|Boolean|ReadOnly here will force the Glusterfs volume to be mounted with read-only permissions. Defaults to false. More info: https://releases.k8s.io/HEAD/examples/volumes/glusterfs/README.md#create-a-pod|


**表 76**  io.k8s.api.core.v1.HostPathVolumeSource

|参数|参数类型|描述|
|--|--|--|
|path|String|Path of the directory on the host. If the path is a symlink, it will follow the link to the real path. More info: https://kubernetes.io/docs/concepts/storage/volumes#hostpath|
|type|String|Type for HostPath Volume Defaults to "" More info: https://kubernetes.io/docs/concepts/storage/volumes#hostpath|


**表 77**  io.k8s.api.core.v1.ISCSIVolumeSource

|参数|参数类型|描述|
|--|--|--|
|chapAuthDiscovery|Boolean|whether support iSCSI Discovery CHAP authentication|
|chapAuthSession|Boolean|whether support iSCSI Session CHAP authentication|
|fsType|String|Filesystem type of the volume that you want to mount. Tip: Ensure that the filesystem type is supported by the host operating system. Examples: "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified. More info: https://kubernetes.io/docs/concepts/storage/volumes#iscsi|
|initiatorName|String|Custom iSCSI Initiator Name. If initiatorName is specified with iscsiInterface simultaneously, new iSCSI interface : will be created for the connection.|
|iqn|String|Target iSCSI Qualified Name.|
|iscsiInterface|String|iSCSI Interface Name that uses an iSCSI transport. Defaults to 'default' (tcp).|
|lun|Integer|iSCSI Target Lun number.|
|portals|Array of strings|iSCSI Target Portal List. The portal is either an IP or ip_addr:port if the port is other than default (typically TCP ports 860 and 3260).|
|readOnly|Boolean|ReadOnly here will force the ReadOnly setting in VolumeMounts. Defaults to false.|
|secretRef|io.k8s.api.core.v1.LocalObjectReference object|CHAP Secret for iSCSI target and initiator authentication|
|targetPortal|String|iSCSI Target Portal. The Portal is either an IP or ip_addr:port if the port is other than default (typically TCP ports 860 and 3260).|


**表 78**  io.k8s.api.core.v1.LocalDirVolumeSource

|参数|参数类型|描述|
|--|--|--|
|sizeLimit|String|Quantity is a fixed-point representation of a number. It provides convenient marshaling/unmarshaling in JSON and YAML, in addition to String() and Int64() accessors.The serialization format is:::=  (Note that  may be empty, from the "" case in .)            ::= 0 | 1 | ... | 9           ::=  |            ::=  | . | . | .             ::= "+" | "-"     ::=  |            ::=  |  |          ::= Ki | Mi | Gi | Ti | Pi | Ei (International System of units; See: http://physics.nist.gov/cuu/Units/binary.html)        ::= m | "" | k | M | G | T | P | E (Note that 1024 = 1Ki but 1000 = 1k; I didn't choose the capitalization.)  ::= "e"  | "E"No matter which of the three exponent forms is used, no quantity may represent a number greater than 2^63-1 in magnitude, nor may it have more than 3 decimal places. Numbers larger or more precise will be capped or rounded up. (E.g.: 0.1m will rounded up to 1m.) This may be extended in the future if we require larger or smaller quantities.When a Quantity is parsed from a string, it will remember the type of suffix it had, and will use the same type again when it is serialized.Before serializing, Quantity will be put in "canonical form". This means that Exponent/suffix will be adjusted up or down (with a corresponding increase or decrease in Mantissa) such that: a. No precision is lost b. No fractional digits will be emitted c. The exponent (or suffix) is as large as possible. The sign will be omitted unless the number is negative.Examples: 1.5 will be serialized as "1500m" 1.5Gi will be serialized as "1536Mi"NOTE: We reserve the right to amend this canonical format, perhaps to allow 1.5 to be canonical. or after March 2015.Note that the quantity will NEVER be internally represented by a floating point number. That is the whole point of this exercise.Non-canonical values will still parse as long as they are well formed, but will be re-emitted in their canonical form. (So always use canonical form, or don't diff.)This format is intended to make it difficult to use these numbers without writing some sort of special handling code in the hopes that that will cause implementors to also use a fixed point implementation.|


**表 79**  io.k8s.api.core.v1.NFSVolumeSource

|参数|参数类型|描述|
|--|--|--|
|path|String|Path that is exported by the NFS server. More info: https://kubernetes.io/docs/concepts/storage/volumes#nfs|
|readOnly|Boolean|ReadOnly here will force the NFS export to be mounted with read-only permissions. Defaults to false. More info: https://kubernetes.io/docs/concepts/storage/volumes#nfs|
|server|String|Server is the hostname or IP address of the NFS server. More info: https://kubernetes.io/docs/concepts/storage/volumes#nfs|


**表 80**  io.k8s.api.core.v1.PersistentVolumeClaimVolumeSource

|参数|参数类型|描述|
|--|--|--|
|claimName|String|ClaimName is the name of a PersistentVolumeClaim in the same namespace as the pod using this volume. More info: https://kubernetes.io/docs/concepts/storage/persistent-volumes#persistentvolumeclaims|
|readOnly|Boolean|Will force the ReadOnly setting in VolumeMounts. Default false.|


**表 81**  io.k8s.api.core.v1.PhotonPersistentDiskVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|Filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified.|
|pdID|String|ID that identifies Photon Controller persistent disk|


**表 82**  io.k8s.api.core.v1.PortworxVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|FSType represents the filesystem type to mount Must be a filesystem type supported by the host operating system. Ex. "ext4", "xfs". Implicitly inferred to be "ext4" if unspecified.|
|readOnly|Boolean|Defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts.|
|volumeID|String|VolumeID uniquely identifies a Portworx volume|


**表 83**  io.k8s.api.core.v1.ProjectedVolumeSource

|参数|参数类型|描述|
|--|--|--|
|defaultMode|Integer|Mode bits to use on created files by default. Must be a value between 0 and 0777. Directories within the path are not affected by this setting. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set.|
|sources|Array of io.k8s.api.core.v1.VolumeProjection objects|list of volume projections|


**表 84**  io.k8s.api.core.v1.VolumeProjection

|参数|参数类型|描述|
|--|--|--|
|configMap|io.k8s.api.core.v1.ConfigMapProjection object|information about the configMap data to project|
|downwardAPI|io.k8s.api.core.v1.DownwardAPIProjection object|information about the downwardAPI data to project|
|secret|io.k8s.api.core.v1.SecretProjection object|information about the secret data to project|
|serviceAccountToken|io.k8s.api.core.v1.ServiceAccountTokenProjection object|information about the serviceAccountToken data to project|


**表 85**  io.k8s.api.core.v1.ConfigMapProjection

|参数|参数类型|描述|
|--|--|--|
|items|Array of io.k8s.api.core.v1.KeyToPath objects|If unspecified, each key-value pair in the Data field of the referenced ConfigMap will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the ConfigMap, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'.|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|optional|Boolean|Specify whether the ConfigMap or it's keys must be defined|


**表 86**  io.k8s.api.core.v1.DownwardAPIProjection

|参数|参数类型|描述|
|--|--|--|
|items|Array of io.k8s.api.core.v1.DownwardAPIVolumeFile objects|Items is a list of DownwardAPIVolume file|


**表 87**  io.k8s.api.core.v1.DownwardAPIVolumeFile

|参数|参数类型|描述|
|--|--|--|
|fieldRef|io.k8s.api.core.v1.ObjectFieldSelector object|Required: Selects a field of the pod: only annotations, labels, name and namespace are supported.|
|mode|Integer|Optional: mode bits to use on this file, must be a value between 0 and 0777. If not specified, the volume defaultMode will be used. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set.|
|path|String|Required: Path is  the relative path name of the file to be created. Must not be absolute or contain the '..' path. Must be utf-8 encoded. The first item of the relative path must not start with '..'|
|resourceFieldRef|io.k8s.api.core.v1.ResourceFieldSelector object|Selects a resource of the container: only resources limits and requests (limits.cpu, limits.memory, requests.cpu and requests.memory) are currently supported.|


**表 88**  io.k8s.api.core.v1.ObjectFieldSelector

|参数|参数类型|描述|
|--|--|--|
|apiVersion|String|Version of the schema the FieldPath is written in terms of, defaults to "v1".|
|fieldPath|String|Path of the field to select in the specified API version.|


**表 89**  io.k8s.api.core.v1.ResourceFieldSelector

|参数|参数类型|描述|
|--|--|--|
|containerName|String|Container name: required for volumes, optional for env vars|
|divisor|String|Specifies the output format of the exposed resources, defaults to "1"|
|resource|String|Required: resource to select|


**表 90**  io.k8s.api.core.v1.SecretProjection

|参数|参数类型|描述|
|--|--|--|
|items|Array of io.k8s.api.core.v1.KeyToPath objects|If unspecified, each key-value pair in the Data field of the referenced Secret will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the Secret, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'.|
|name|String|Name of the referent. More info: https://kubernetes.io/docs/concepts/overview/working-with-objects/names/#names|
|optional|Boolean|Specify whether the Secret or its key must be defined|


**表 91**  io.k8s.api.core.v1.ServiceAccountTokenProjection

|参数|参数类型|描述|
|--|--|--|
|audience|String|Audience is the intended audience of the token. A recipient of a token must identify itself with an identifier specified in the audience of the token, and otherwise should reject the token. The audience defaults to the identifier of the apiserver.|
|expirationSeconds|Long|ExpirationSeconds is the requested duration of validity of the service account token. As the token approaches expiration, the kubelet volume plugin will proactively rotate the service account token. The kubelet will start trying to rotate the token if the token is older than 80 percent of its time to live or if the token is older than 24 hours.Defaults to 1 hour and must be at least 10 minutes.|
|path|String|Path is the path relative to the mount point of the file to project the token into.|


**表 92**  io.k8s.api.core.v1.QuobyteVolumeSource

|参数|参数类型|描述|
|--|--|--|
|group|String|Group to map volume access to Default is no group|
|readOnly|Boolean|ReadOnly here will force the Quobyte volume to be mounted with read-only permissions. Defaults to false.|
|registry|String|Registry represents a single or multiple Quobyte Registry services specified as a string as host:port pair (multiple entries are separated with commas) which acts as the central registry for volumes|
|user|String|User to map volume access to Defaults to serivceaccount user|
|volume|String|Volume is a string that references an already created Quobyte volume by name.|


**表 93**  io.k8s.api.core.v1.RBDVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|Filesystem type of the volume that you want to mount. Tip: Ensure that the filesystem type is supported by the host operating system. Examples: "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified. More info: https://kubernetes.io/docs/concepts/storage/volumes#rbd|
|image|String|The rados image name. More info: https://releases.k8s.io/HEAD/examples/volumes/rbd/README.md#how-to-use-it|
|keyring|String|Keyring is the path to key ring for RBDUser. Default is /etc/ceph/keyring. More info: https://releases.k8s.io/HEAD/examples/volumes/rbd/README.md#how-to-use-it|
|monitors|Array of strings|A collection of Ceph monitors. More info: https://releases.k8s.io/HEAD/examples/volumes/rbd/README.md#how-to-use-it|
|pool|String|The rados pool name. Default is rbd. More info: https://releases.k8s.io/HEAD/examples/volumes/rbd/README.md#how-to-use-it|
|readOnly|Boolean|ReadOnly here will force the ReadOnly setting in VolumeMounts. Defaults to false. More info: https://releases.k8s.io/HEAD/examples/volumes/rbd/README.md#how-to-use-it|
|secretRef|io.k8s.api.core.v1.LocalObjectReference object|SecretRef is name of the authentication secret for RBDUser. If provided overrides keyring. Default is nil. More info: https://releases.k8s.io/HEAD/examples/volumes/rbd/README.md#how-to-use-it|
|user|String|The rados user name. Default is admin. More info: https://releases.k8s.io/HEAD/examples/volumes/rbd/README.md#how-to-use-it|


**表 94**  io.k8s.api.core.v1.ScaleIOVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|Filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified.|
|gateway|String|The host address of the ScaleIO API Gateway.|
|protectionDomain|String|The name of the ScaleIO Protection Domain for the configured storage.|
|readOnly|Boolean|Defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts.|
|secretRef|io.k8s.api.core.v1.LocalObjectReference object|SecretRef references to the secret for ScaleIO user and other sensitive information. If this is not provided, Login operation will fail.|
|sslEnabled|Boolean|Flag to enable/disable SSL communication with Gateway, default false|
|storageMode|String|Indicates whether the storage for a volume should be ThickProvisioned or ThinProvisioned.|
|storagePool|String|The ScaleIO Storage Pool associated with the protection domain.|
|system|String|The name of the storage system as configured in ScaleIO.|
|volumeName|String|The name of a volume already created in the ScaleIO system that is associated with this volume source.|


**表 95**  io.k8s.api.core.v1.SecretVolumeSource

|参数|参数类型|描述|
|--|--|--|
|defaultMode|Integer|Optional: mode bits to use on created files by default. Must be a value between 0 and 0777. Defaults to 0644. Directories within the path are not affected by this setting. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set.|
|items|Array of io.k8s.api.core.v1.KeyToPath objects|If unspecified, each key-value pair in the Data field of the referenced Secret will be projected into the volume as a file whose name is the key and content is the value. If specified, the listed keys will be projected into the specified paths, and unlisted keys will not be present. If a key is specified which is not present in the Secret, the volume setup will error unless it is marked optional. Paths must be relative and may not contain the '..' path or start with '..'.|
|optional|Boolean|Specify whether the Secret or it's keys must be defined|
|secretName|String|Name of the secret in the pod's namespace to use. More info: https://kubernetes.io/docs/concepts/storage/volumes#secret|


**表 96**  io.k8s.api.core.v1.KeyToPath

|参数|参数类型|描述|
|--|--|--|
|key|String|The key to project.|
|mode|Integer|Optional: mode bits to use on this file, must be a value between 0 and 0777. If not specified, the volume defaultMode will be used. This might be in conflict with other options that affect the file mode, like fsGroup, and the result can be other mode bits set.|
|path|String|The relative path of the file to map the key to. May not be an absolute path. May not contain the path element '..'. May not start with the string '..'.|


**表 97**  io.k8s.api.core.v1.StorageOSVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|Filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified.|
|readOnly|Boolean|Defaults to false (read/write). ReadOnly here will force the ReadOnly setting in VolumeMounts.|
|secretRef|io.k8s.api.core.v1.LocalObjectReference object|SecretRef specifies the secret to use for obtaining the StorageOS API credentials. If not specified, default values will be attempted.|
|volumeName|String|VolumeName is the human-readable name of the StorageOS volume. Volume names are only unique within a namespace.|
|volumeNamespace|String|VolumeNamespace specifies the scope of the volume within StorageOS. If no namespace is specified then the Pod's namespace will be used. This allows the Kubernetes name scoping to be mirrored within StorageOS for tighter integration. Set VolumeName to any name to override the default behaviour. Set to "default" if you are not using namespaces within StorageOS. Namespaces that do not pre-exist within StorageOS will be created.|


**表 98**  io.k8s.api.core.v1.VsphereVirtualDiskVolumeSource

|参数|参数类型|描述|
|--|--|--|
|fsType|String|Filesystem type to mount. Must be a filesystem type supported by the host operating system. Ex. "ext4", "xfs", "ntfs". Implicitly inferred to be "ext4" if unspecified.|
|storagePolicyID|String|Storage Policy Based Management (SPBM) profile ID associated with the StoragePolicyName.|
|storagePolicyName|String|Storage Policy Based Management (SPBM) profile name.|
|volumePath|String|Path that identifies vSphere volume vmdk|


**表 99**  io.k8s.api.core.v1.PodStatus

|参数|参数类型|描述|
|--|--|--|
|conditions|Array of io.k8s.api.core.v1.PodCondition objects|Current service state of pod. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#pod-conditions|
|containerStatuses|Array of io.k8s.api.core.v1.ContainerStatus objects|The list has one entry per container in the manifest. Each entry is currently the output of *docker inspect*. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#pod-and-container-status|
|hostIP|String|IP address of the host to which the pod is assigned. Empty if not yet scheduled.|
|initContainerStatuses|Array of io.k8s.api.core.v1.ContainerStatus objects|The list has one entry per init container in the manifest. The most recent successful init container will have ready = true, the most recently started container will have startTime set. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#pod-and-container-status|
|managementIP|String|IP address of the nodeIP to which the pod is assigned. Empty if not yet scheduled.|
|message|String|A human readable message indicating details about why the pod is in this condition.|
|nominatedNodeName|String|nominatedNodeName is set only when this pod preempts other pods on the node, but it cannot be scheduled right away as preemption victims receive their graceful termination periods. This field does not guarantee that the pod will be scheduled on this node. Scheduler may decide to place the pod elsewhere if other nodes become available sooner. Scheduler may also decide to give the resources on this node to a higher priority pod that is created after preemption. As a result, this field may be different than PodSpec.nodeName when the pod is scheduled.|
|phase|String|The phase of a Pod is a simple, high-level summary of where the Pod is in its lifecycle. The conditions array, the reason and message fields, and the individual container status arrays contain more detail about the pod's status. There are five possible phase values:Pending: The pod has been accepted by the Kubernetes system, but one or more of the container images has not been created. This includes time before being scheduled as well as time spent downloading images over the network, which could take a while. Running: The pod has been bound to a node, and all of the containers have been created. At least one container is still running, or is in the process of starting or restarting. Succeeded: All containers in the pod have terminated in success, and will not be restarted. Failed: All containers in the pod have terminated, and at least one container has terminated in failure. The container either exited with non-zero status or was terminated by the system. Unknown: For some reason the state of the pod could not be obtained, typically due to an error in communicating with the host of the pod.More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#pod-phase|
|podIP|String|IP address allocated to the pod. Routable at least within the cluster. Empty if not yet allocated.|
|podNetworks|Array of io.k8s.api.core.v1.PodNetworkInterface objects|Complete list of Networks attached to this pod|
|processStatuses|Array of io.k8s.api.core.v1.ProcessStatus objects|Status list for processes|
|qosClass|String|The Quality of Service (QOS) classification assigned to the pod based on resource requirements See PodQOSClass type for available QOS classes More info: https://git.k8s.io/community/contributors/design-proposals/node/resource-qos.md|
|reason|String|A brief CamelCase message indicating details about why the pod is in this state. e.g. 'Evicted'|
|startTime|String|RFC 3339 date and time at which the object was acknowledged by the Kubelet. This is before the Kubelet pulled the container image(s) for the pod.|


**表 100**  io.k8s.api.core.v1.PodCondition

|参数|参数类型|描述|
|--|--|--|
|lastProbeTime|String|Last time we probed the condition.|
|lastTransitionTime|String|Last time the condition transitioned from one status to another.|
|message|String|Human-readable message indicating details about last transition.|
|reason|String|Unique, one-word, CamelCase reason for the condition's last transition.|
|status|String|Status is the status of the condition. Can be True, False, Unknown. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#pod-conditions|
|type|String|Type is the type of the condition. More info: https://kubernetes.io/docs/concepts/workloads/pods/pod-lifecycle#pod-conditions|


**表 101**  io.k8s.api.core.v1.ContainerStatus

|参数|参数类型|描述|
|--|--|--|
|containerID|String|Container's ID in the format 'docker://<container_id>'.|
|image|String|The image the container is running. More info: https://kubernetes.io/docs/concepts/containers/images|
|imageID|String|ImageID of the container's image.|
|lastState|io.k8s.api.core.v1.ContainerState object|Details about the container's last termination condition.|
|name|String|This must be a DNS_LABEL. Each container in a pod must have a unique name. Cannot be updated.|
|ready|Boolean|Specifies whether the container has passed its readiness probe.|
|restartCount|Integer|The number of times the container has been restarted, currently based on the number of dead containers that have not yet been removed. Note that this is calculated from dead containers. But those containers are subject to garbage collection. This value will get capped at 5 by GC.|
|state|io.k8s.api.core.v1.ContainerState object|Details about the container's current condition.|


**表 102**  io.k8s.api.core.v1.ContainerState

|参数|参数类型|描述|
|--|--|--|
|running|io.k8s.api.core.v1.ContainerStateRunning object|Details about a running container|
|terminated|io.k8s.api.core.v1.ContainerStateTerminated object|Details about a terminated container|
|waiting|io.k8s.api.core.v1.ContainerStateWaiting object|Details about a waiting container|


**表 103**  io.k8s.api.core.v1.ContainerStateRunning

|参数|参数类型|描述|
|--|--|--|
|startedAt|String|Time at which the container was last (re-)started|


**表 104**  io.k8s.api.core.v1.ContainerStateTerminated

|参数|参数类型|描述|
|--|--|--|
|containerID|String|Container's ID in the format 'docker://<container_id>'|
|exitCode|Integer|Exit status from the last termination of the container|
|finishedAt|String|Time at which the container last terminated|
|message|String|Message regarding the last termination of the container|
|reason|String|(brief) reason from the last termination of the container|
|signal|Integer|Signal from the last termination of the container|
|startedAt|String|Time at which previous execution of the container started|


**表 105**  io.k8s.api.core.v1.ContainerStateWaiting

|参数|参数类型|描述|
|--|--|--|
|message|String|Message regarding why the container is not yet running.|
|reason|String|(brief) reason the container is not yet running.|


**表 106**  io.k8s.api.core.v1.PodNetworkInterface

|参数|参数类型|描述|
|--|--|--|
|extraInfo|Map<String,String>|extra info of the interface|
|iP|Array of strings|IP address(both v4 and v6) of this interface|
|name|String|Name of the interface inside the pod|
|network|String|Name of the attached network|


**表 107**  io.k8s.api.core.v1.ProcessStatus

|参数|参数类型|描述|
|--|--|--|
|lastState|io.k8s.api.core.v1.ProcessState object|Details about the process's last termination condition.|
|name|String|This must be a DNS_LABEL. Each process in a pod must have a unique name. Cannot be updated.|
|package|String|The image the process is running.|
|packageID|String|ImageID of the process's image.|
|processID|String|process's ID in the format '<process_id>'.|
|ready|Boolean|Specifies whether the process has passed its readiness probe.|
|restartCount|Integer|The number of times the process has been restarted, currently based on the number of dead processes that have not yet been removed. Note that this is calculated from dead processes. But those processes are subject to garbage collection. This value will get capped at 5 by GC.|
|state|io.k8s.api.core.v1.ProcessState object|Details about the process's current condition.|


**表 108**  io.k8s.api.core.v1.ProcessState

|参数|参数类型|描述|
|--|--|--|
|running|io.k8s.api.core.v1.ProcessStateRunning object|Details about a running process|
|terminated|io.k8s.api.core.v1.ProcessStateTerminated object|Details about a terminated process|
|waiting|io.k8s.api.core.v1.ProcessStateWaiting object|Details about a waiting process|


**表 109**  io.k8s.api.core.v1.ProcessStateRunning

|参数|参数类型|描述|
|--|--|--|
|startedAt|String|Time at which the process was last (re-)started|


**表 110**  io.k8s.api.core.v1.ProcessStateTerminated

|参数|参数类型|描述|
|--|--|--|
|exitCode|Integer|Exit status from the last termination of the process|
|finishedAt|String|Time at which the process last terminated|
|message|String|Message regarding the last termination of the process|
|processID|String|Process's ID in the format 'docker://<process_id>'|
|reason|String|(brief) reason from the last termination of the process|
|signal|Integer|Signal from the last termination of the process|
|startedAt|String|Time at which previous execution of the process started|


**表 111**  io.k8s.api.core.v1.ProcessStateWaiting

|参数|参数类型|描述|
|--|--|--|
|message|String|Message regarding why the container is not yet running.|
|reason|String|(brief) reason the process is not yet running.|


**表 112**  io.k8s.apimachinery.pkg.apis.meta.v1.ListMeta\_v2

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
    "metadata" : {
      "annotations" : {
        "kubernetes.io/created-by" : "{\"kind\":\"SerializedReference\",\"apiVersion\":\"v1\",\"reference\":{\"kind\":\"ReplicationController\",\"namespace\":\"default\",\"name\":\"fdsfsd\",\"uid\":\"7539c329-57c4-11e7-afb7-fa163e218692\",\"apiVersion\":\"v1\",\"resourceVersion\":\"956153\"}}",
        "kubernetes.io/limit-ranger" : "LimitRanger plugin set: cpu request for container container01"
      },
      "creationTimestamp" : "2017-06-23T03:31:35Z",
      "generateName" : "fdsfsd-",
      "labels" : {
        "cce/appgroup" : "gfsad",
        "name" : "fdsfsd"
      },
      "name" : "fdsfsd-ddnft",
      "namespace" : "default",
      "ownerReferences" : [ {
        "apiVersion" : "v1",
        "controller" : true,
        "kind" : "ReplicationController",
        "name" : "fdsfsd",
        "uid" : "7539c329-57c4-11e7-afb7-fa163e218692"
      } ],
      "resourceVersion" : "1449034",
      "selfLink" : "/api/v1/namespaces/default/pods/fdsfsd-ddnft",
      "uid" : "753a45bc-57c4-11e7-afb7-fa163e218692"
    },
    "spec" : {
      "containers" : [ {
        "image" : "10.154.52.159:443/test/apache-php:latest",
        "imagePullPolicy" : "Always",
        "name" : "container01",
        "ports" : [ {
          "containerPort" : 80,
          "protocol" : "TCP"
        } ],
        "resources" : {
          "requests" : {
            "cpu" : "100m"
          }
        },
        "terminationMessagePath" : "/dev/termination-log",
        "volumeMounts" : [ {
          "mountPath" : "/var/run/secrets/kubernetes.io/serviceaccount",
          "name" : "default-token-863rh",
          "readOnly" : true
        } ]
      } ],
      "dnsPolicy" : "ClusterFirst",
      "imagePullSecrets" : [ {
        "name" : "myregistry"
      } ],
      "nodeName" : "192.168.12.187",
      "restartPolicy" : "Always",
      "securityContext" : { },
      "serviceAccount" : "default",
      "serviceAccountName" : "default",
      "volumes" : [ {
        "name" : "default-token-863rh",
        "secret" : {
          "defaultMode" : 420,
          "secretName" : "default-token-863rh"
        }
      } ]
    },
    "status" : {
      "conditions" : [ {
        "lastProbeTime" : null,
        "lastTransitionTime" : "2017-06-23T03:31:36Z",
        "status" : "True",
        "type" : "Initialized"
      }, {
        "lastProbeTime" : null,
        "lastTransitionTime" : "2017-06-28T06:34:51Z",
        "status" : "True",
        "type" : "Ready"
      }, {
        "lastProbeTime" : null,
        "lastTransitionTime" : "2017-06-23T03:31:35Z",
        "status" : "True",
        "type" : "PodScheduled"
      } ],
      "containerStatuses" : [ {
        "containerID" : "docker://f3daa802f753d123fe66b2cba2e917725702f8d446c17541822a68f9d2414c6d",
        "image" : "10.154.52.159:443/test/apache-php:latest",
        "imageID" : "docker://sha256:2e233ad9329bd7f65572dd6acb1a03e8839c36abfdb1d1f9012d84d13cecf9fc",
        "lastState" : { },
        "name" : "container01",
        "ready" : true,
        "restartCount" : 0,
        "state" : {
          "running" : {
            "startedAt" : "2017-06-28T06:34:46Z"
          }
        }
      } ],
      "hostIP" : "192.168.12.187",
      "phase" : "Running",
      "podIP" : "172.16.56.4",
      "startTime" : "2017-06-23T03:31:36Z"
    }
  } ],
  "kind" : "PodList",
  "metadata" : {
    "resourceVersion" : "1550321",
    "selfLink" : "/api/v1/pods"
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


