# PATCH请求方法操作说明<a name="cci_02_0070"></a>

对于PATCH请求方法的操作，Kubernetes API通过相应的HTTP头域“Content-Type”对其进行识别。

## 操作说明<a name="zh-cn_topic_0083857408_s8aafd6c4a7764494b1ed22d2e4a178bf"></a>

目前支持两种类型的PATCH请求方法的操作。

1.  **Merge Patch, Content-Type: application/merge-patch+json**

    在RFC7386协议的定义中，Merge Patch必须包含对一个资源对象的部分描述，即为JSON对象。该JSON对象被提交到服务端后与服务端的当前对象合并，即替换当前资源对象中的列表域，从而创建一个新的对象。

2.  **Strategic Merge Patch, Content-Type: application/strategic-merge-patch+json**

    Strategic Merge Patch是添加合法的元数据到API对象中，并通过这些新的元数据来决定哪个列表被合并，哪个列表不该被合并。当前这些元数据则作为结构标签。


“Merge Patch“与“Strategic Merge Patch“的操作区别请参见[PATCH请求方法操作示例](PATCH请求方法操作示例.md)。

