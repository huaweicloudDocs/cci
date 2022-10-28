# 使用ConfigMap<a name="cci_01_0034"></a>

ConfigMap是一种用于存储应用所需配置信息的资源类型。资源创建完成后，可在容器应用中作为文件使用。

## 创建ConfigMap<a name="section18512531861"></a>

1.  登录云容器实例控制台，单击左侧导航栏的“配置中心 \> 配置项（ConfigMap）”，在右侧页面中选择命名空间，单击“创建配置项“。

    CCI控制台上也支持直接使用YAML方式创建配置项，在右上角单击YAML创建，输入ConfigMap的YAML定义内容，单击“确定“即可，YAML定义可以参考[yaml格式](#li5976173124010)。

2.  云容器实例支持“手工输入”和“文件上传”两种方式来创建ConfigMap。
    -   方式一：手工输入。参照[表1](#table16321825732)设置新增配置参数，其中带“\*”标志的参数为必填参数。

        **表 1**  新建配置参数说明

|参数|参数说明|
|--|--|
|**基本信息**|
|*配置项名称|新建的ConfigMap名称。请输入以小写字母或数字开头，小写字母、数字、中划线（-）、点（.）组成（其中两点不能相连，点不能与中划线相连），小写字母或数字结尾的1到253字符的字符串|
|描述|ConfigMap的描述信息。|
|**配置项数据**|ConfigMap存储的配置数据。其中，“键”代表文件名；“值”代表文件中的内容。单击“添加数据” 。输入键、值。|
|**配置项标签**|标签以Key/value键值对的形式附加到各种对象上（如负载、服务等）。标签定义了这些对象的可识别属性，用来对它们进行管理和选择。单击“添加标签” 。输入键、值。|


    -   方式二：文件上传。

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >云容器实例支持json或yaml格式，且文件大小需要小于1MB，详细请参见[ConfigMap文件格式要求](#section18975165217385)。

        单击“添加文件“，选择已创建的ConfigMap类型资源文件后，单击“打开”。

3.  配置完成后，单击“创建“。

## ConfigMap的使用<a name="section152761334151217"></a>

配置项创建完成后，可以在创建负载的过程中挂载到容器指定路径下，如下图所示，将名为cci-configmap01的配置项挂载到“/tmp/configmap1“路径下。

**图 1**  使用ConfigMap<a name="fig4539158113314"></a>  
![](figures/使用ConfigMap.png "使用ConfigMap")

负载创建后，在“/tmp/configmap1“路径下将创建配置文件，配置项的“键”代表文件名；“值”代表文件中的内容。

## ConfigMap文件格式要求<a name="section18975165217385"></a>

ConfigMap资源文件支持json和yaml两种格式，且数据值大小不得超过1MB。

-   json格式

    文件名称为configmap.json，配置示例如下：

    ```
    {
      "kind": "ConfigMap",
      "apiVersion": "v1",
      "metadata": {
        "name": "nginxconf",
        "namespace": "cci-namespace-demo"
      },
      "data": {
        "nginx.conf": "server {\n    listen       80;\n    server_name  localhost;\n\n    location / {\n        root   html;\n        index  index.html index.htm;\n    }\n}"
      }
    }
    ```

-   <a name="li5976173124010"></a>yaml格式

    文件名称为configmap.yaml，配置示例如下：

    ```
    kind: ConfigMap
    apiVersion: v1
    metadata:
      name: nginxconf
      namespace: cci-namespace-demo
    data:
      nginx.conf: |-
        server {
            listen       80;
            server_name  localhost;
    
            location / {
                root   html;
                index  index.html index.htm;
            }
        }
    ```


## 使用kubectl创建ConfigMap<a name="section25041341338"></a>

使用kubectl创建ConfigMap请参见[ConfigMap](https://support.huaweicloud.com/devg-cci/cci_05_0019.html)。

