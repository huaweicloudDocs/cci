# 定时任务（CronJob）<a name="cci_01_0066"></a>

定时任务（CronJob）是基于时间控制的任务（Job），类似于Linux系统的crontab，在指定的时间周期运行指定的任务。

## 创建定时任务<a name="section145271625910"></a>

1.  登录云容器实例管理控制台，左侧导航栏中选择[工作负载 \> 定时任务（CronJob）](https://console.huaweicloud.com/cci/#/app/workload/cronjob/list)，在右侧页面单击“创建定时任务“。
2.  添加基本信息。
    -   **任务名称**

        请输入以小写字母或数字开头，小写字母、数字、中划线（-）、点（.）组成（其中两点不能相连，点不能与中划线相连），小写字母或数字结尾的1到63字符的字符串。任务名称不支持修改，如需修改名称，需要重新创建。

    -   **命名空间**

        选择命名空间，如果还未创建命名空间，请参考[命名空间](命名空间.md)创建。

    -   **任务描述**

        描述信息，少于等于250个字符。

    -   **Pod规格**

        您可以选择使用GPU（只能在GPU型命名空间下）或不使用GPU。

        当前提供3种类型的Pod，包括通用计算型（通用计算型命名空间下使用）、[RDMA](https://zh.wikipedia.org/wiki/%E8%BF%9C%E7%A8%8B%E7%9B%B4%E6%8E%A5%E5%86%85%E5%AD%98%E8%AE%BF%E9%97%AE)加速型和GPU加速型（GPU型命名空间下使用）。

        GPU加速型Pod提供NVIDIA Tesla V100 32G显卡和NVIDIA Tesla V100 16G显卡，具体的规格有如下所示。

        -   NVIDIA Tesla V100 32G显卡：
            -   NVIDIA Tesla V100 32G x 1，CPU 4核，内存32GB
            -   NVIDIA Tesla V100 32G x 2，CPU 8核，内存64GB
            -   NVIDIA Tesla V100 32G x 4，CPU 16核，内存128GB
            -   NVIDIA Tesla V100 32G x 8，CPU 32核，内存256GB

        -   NVIDIA Tesla V100 16G显卡：
            -   NVIDIA Tesla V100 16G x 1，CPU 4核，内存32GB
            -   NVIDIA Tesla V100 16G x 2，CPU 8核，内存64GB
            -   NVIDIA Tesla V100 16G x 4，CPU 16核，内存128GB
            -   NVIDIA Tesla V100 16G x 8，CPU 32核，内存256GB

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >“华北-北京四”区域，仅支持NVIDIA TeslaV100 32G显卡。

        云容器实例支持使用NVIDIA GPU的驱动版本为**410.104和418.126**，您应用程序中使用的CUDA需满足如[表1](#table153076178525)所示的配套关系。CUDA与驱动的配套关系来源于NVIDIA官网，详细信息请参见[CUDA Compatibility](https://docs.nvidia.com/deploy/cuda-compatibility/index.html)。

        **表 1**  NVIDIA GPU驱动与CUDA配套关系

        <a name="table153076178525"></a>
        <table><thead align="left"><tr id="row133073172525"><th class="cellrowborder" valign="top" width="30.620000000000005%" id="mcps1.2.3.1.1"><p id="p330781713521"><a name="p330781713521"></a><a name="p330781713521"></a>NVIDIA GPU驱动版本</p>
        </th>
        <th class="cellrowborder" valign="top" width="69.38%" id="mcps1.2.3.1.2"><p id="p1830741710523"><a name="p1830741710523"></a><a name="p1830741710523"></a>CUDA Toolkit版本</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row9786192115398"><td class="cellrowborder" valign="top" width="30.620000000000005%" headers="mcps1.2.3.1.1 "><p id="p1178672103912"><a name="p1178672103912"></a><a name="p1178672103912"></a>410.104</p>
        </td>
        <td class="cellrowborder" valign="top" width="69.38%" headers="mcps1.2.3.1.2 "><p id="p3628192518161"><a name="p3628192518161"></a><a name="p3628192518161"></a>CUDA 10.0 (10.0.130)及以下</p>
        </td>
        </tr>
        <tr id="row730851720527"><td class="cellrowborder" valign="top" width="30.620000000000005%" headers="mcps1.2.3.1.1 "><p id="p163080175524"><a name="p163080175524"></a><a name="p163080175524"></a>418.126</p>
        </td>
        <td class="cellrowborder" valign="top" width="69.38%" headers="mcps1.2.3.1.2 "><p id="p113083174523"><a name="p113083174523"></a><a name="p113083174523"></a>CUDA 10.1 (10.1.105)及以下</p>
        </td>
        </tr>
        </tbody>
        </table>

        当不使用GPU时，Pod规格需满足如下要求：

        -   Pod的CPU取值范围为0.25核-32核，或者自定义选择48核、64核，且单个容器的CPU必须为0.25核的整数倍
        -   Pod的内存取值范围为1GB-512GB，且内存必须为1GB的整数倍
        -   Pod的CPU/内存配比值必须在1:2到1:8之间
        -   一个Pod内最多支持5个容器，单个容器最小配置是0.25核、0.2GB，最大同容器实例的最大配置
        -   Pod中所有容器和InitContainer（启动容器）规格中的request和limit相等

    -   **容器配置**

        一个Pod可以包含一个或多个运行不同镜像的容器，通常情况下一个Pod中只有一个容器，若您的应用程序需要多个容器，请单击“添加容器“，然后选择镜像。

        >![](public_sys-resources/icon-notice.gif) **须知：** 
        >同一个Pod实例中的不同容器如果监听了相同的端口，则会导致端口冲突，Pod可能会启动失败。例如在Pod中添加了一个nginx镜像容器，启动了80端口，如果该Pod中另一个http服务的镜像也启动80端口，那么这个Pod就会出现端口冲突。

        -   我的镜像：展示了您上传到容器镜像服务的镜像。

            >![](public_sys-resources/icon-note.gif) **说明：** 
            >如您是IAM用户，您需要参考[（可选）上传镜像](环境设置.md#section1593133403517)进行权限设置后才可使用帐号的私有镜像。
            >CCI当前暂不支持对接第三方镜像仓库。

        -   开源镜像中心：展示了镜像中心的公共镜像。
        -   共享镜像：展示了容器镜像服务中他人共享的镜像。

        镜像选择完成后，需要选择镜像的版本、设置容器名称、设置容器占用的CPU和内存规格（**单个容器最小配置是0.25核、0.2GB**），并选择是否开启采集标准输出文件（开启后，应用运维管理AOM将根据实际使用量进行计费）。

        >![](public_sys-resources/icon-note.gif) **说明：** 
        >每个租户一个月有500M的免费日志存储空间，超过500M时AOM将根据实际使用量进行收费，计费规则请参见[产品价格详情](https://www.huaweicloud.com/pricing.html?tab=detail#/aom)。

        对于GPU加速型Pod（仅GPU型命名空间下才可以选择），Pod中只有一个容器能使用GPU，如果您的Pod中有多个容器，您可以通过**开启GPU**这个开关选择哪个容器使用GPU。

        您还可以为容器做如下高级设置：

        -   存储：支持挂载持久化卷到容器中，以实现数据文件的持久化存储，当前支持文件存储卷。单击“添加文件存储卷“，输入名称、容量、容器内挂载路径、挂载子路径，选择磁盘类型。定时任务创建完成后，可对存储卷进行管理，具体请参见[文件存储卷](文件存储卷.md)。
        -   日志采集：支持根据您配置的日志输出路径，采集应用日志，请自行防爆处理。单击添加日志存储，输入容器内日志路径，调整日志存储空间。负载创建完成后，可在AOM界面查看日志，具体请参见[日志管理](日志管理.md)。
        -   环境变量：在容器中设置环境变量，支持手动输入和引用变量。环境变量为应用提供极大的灵活性，您可以在应用程序中使用环境变量，在创建容器时为环境变量赋值，容器运行时读取环境变量的值，从而做到灵活的配置，而不是每次都重新编写应用程序制作镜像。

            手动输入只需要直接输入变量名称和变量值。

            变量引用支持引用PodIP（Pod的IP地址）、PodName（Pod的名称）以及Secret，输入变量名称，选择引用类型、引用值。其中Secret引用的创建请参见[使用Secret](使用Secret.md)。

        -   存活探针：用于容器的自定义监控检查，如果检查失败，云容器实例将关闭该容器，然后根据默认重启策略来决定是否重启容器。详细步骤请参见[健康检查](健康检查.md)。
        -   生命周期：生命周期脚本定义，在容器的生命周期的特定阶段执行调用。详细步骤请参见[容器生命周期](容器生命周期.md)。
        -   启动命令：输入容器启动命令，容器启动后会立即执行。启动命令对应于容器引擎的ENTRYPOINT启动命令，详细内容请参见[容器启动命令](容器启动命令.md)。
        -   配置管理：容器支持挂载ConfigMap和Secret。ConfigMap和Secret的创建请参见[使用ConfigMap](使用ConfigMap.md)和[使用Secret](使用Secret.md)。

3.  单击“下一步：定时规则”，进行任务高级配置。
    -   并发策略
        -   Forbid：在前一个任务未完成时，不创建新任务。
        -   Allow：定时任务不断新建Job。
        -   Replace：已到新任务创建时间点，但前一个任务还未完成，新的任务会取代前一个任务。

    -   定时规则：设置任务在何时执行。
    -   任务记录：设置保留执行成功任务的个数和保留执行失败任务的个数。

4.  单击“下一步：规格确认“，单击“提交”，单击“返回任务列表”。

    在任务列表中，待任务状态为“已启动“，任务创建成功。您可以单击负载名进入任务详情界面，按F5查看任务实时状态。


## 使用kubectl创建定时任务<a name="section1127114384291"></a>

使用kubectl创建定时任务请参见[创建CronJob](https://support.huaweicloud.com/devg-cci/cci_05_0022.html)。

