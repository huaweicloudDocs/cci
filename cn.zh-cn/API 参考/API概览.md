# API概览<a name="cci_02_0002"></a>

云容器实例所提供的接口为CCI接口和Kubernetes原生接口。通过使用云容器实例提供的接口，您可以完整的使用云容器实例的所有功能，包括创建无状态负载、有状态负载等。

<a name="table1577981717153"></a>
<table><thead align="left"><tr id="row16810121712155"><th class="cellrowborder" valign="top" width="19%" id="mcps1.1.4.1.1"><p id="p13731217121512"><a name="p13731217121512"></a><a name="p13731217121512"></a>大类</p>
</th>
<th class="cellrowborder" valign="top" width="20.979999999999997%" id="mcps1.1.4.1.2"><p id="p13834717131516"><a name="p13834717131516"></a><a name="p13834717131516"></a>类型</p>
</th>
<th class="cellrowborder" valign="top" width="60.019999999999996%" id="mcps1.1.4.1.3"><p id="p3883151714159"><a name="p3883151714159"></a><a name="p3883151714159"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2054614267164"><td class="cellrowborder" rowspan="2" valign="top" width="19%" headers="mcps1.1.4.1.1 "><p id="p154009311259"><a name="p154009311259"></a><a name="p154009311259"></a>API</p>
</td>
<td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.1.4.1.2 "><p id="p14546162641618"><a name="p14546162641618"></a><a name="p14546162641618"></a><a href="#section13159414572">Network</a></p>
</td>
<td class="cellrowborder" valign="top" width="60.019999999999996%" headers="mcps1.1.4.1.3 "><p id="p565181993120"><a name="p565181993120"></a><a name="p565181993120"></a>Network对象管理接口，包括Network对象的创建、查询、修改、删除等接口。</p>
<p id="p854542223216"><a name="p854542223216"></a><a name="p854542223216"></a>Network对象是华为云CCI 新增对象，用于定义kubernetes中一个namespace内的网络与华为云虚拟私有云服务的子网和VPC的映射关系。</p>
</td>
</tr>
<tr id="row1739710274275"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p19398427102710"><a name="p19398427102710"></a><a name="p19398427102710"></a><a href="#section743818217318">Extended PersistentVolumeClaim</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p14398132752718"><a name="p14398132752718"></a><a name="p14398132752718"></a>Extended PersistentVolumeClaim对象管理接口，包括导入存储、查询导入的PVC、解绑存储接口。</p>
</td>
</tr>
<tr id="row24301411136"><td class="cellrowborder" rowspan="19" valign="top" width="19%" headers="mcps1.1.4.1.1 "><p id="p1565011115165"><a name="p1565011115165"></a><a name="p1565011115165"></a>Kubernetes API</p>
</td>
<td class="cellrowborder" valign="top" width="20.979999999999997%" headers="mcps1.1.4.1.2 "><p id="p1243017413139"><a name="p1243017413139"></a><a name="p1243017413139"></a><a href="#section115511242677">Namespace</a></p>
</td>
<td class="cellrowborder" valign="top" width="60.019999999999996%" headers="mcps1.1.4.1.3 "><p id="p87892038224"><a name="p87892038224"></a><a name="p87892038224"></a>Namespace对象管理接口，包括Namespace对象的创建、查询、修改、删除等接口。</p>
<p id="p10513122920328"><a name="p10513122920328"></a><a name="p10513122920328"></a><span>命名空间（namespace）是一种在多个用户之间划分资源的方法。当你的项目和人员众多的时候可以考虑根据项目属性，例如生产、测试、开发划分不同的namespace。</span></p>
</td>
</tr>
<tr id="row9338112161"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p17348113165"><a name="p17348113165"></a><a name="p17348113165"></a><a href="#section2458101711812">Pod</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p195231610101919"><a name="p195231610101919"></a><a name="p195231610101919"></a>Pod对象管理接口，包括Pod对象的查询接口。</p>
<p id="p177481415123215"><a name="p177481415123215"></a><a name="p177481415123215"></a><span>Pod是Kubernetes创建或部署的最小单位。一个Pod封装一个或多个容器、存储资源、一个独立的网络IP以及管理控制容器运行方式的策略选项。</span></p>
</td>
</tr>
<tr id="row119982597157"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1998185911517"><a name="p1998185911517"></a><a name="p1998185911517"></a><a href="#section731718191482">Deployment</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p470917181199"><a name="p470917181199"></a><a name="p470917181199"></a>Deployment对象管理接口，包括Deployment对象的创建、查询、修改、删除等接口。</p>
<p id="p1425134810321"><a name="p1425134810321"></a><a name="p1425134810321"></a>Deployment是Pod Controller的一种。一个Deployment可以包含一个或多个Pod副本，每个Pod副本的角色相同，所以系统会自动为Deployment的多个Pod副本分发请求。Deployment中的所有Pod副本共享存储卷。</p>
</td>
</tr>
<tr id="row13781759181516"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1778165917158"><a name="p1778165917158"></a><a name="p1778165917158"></a><a href="#section43641211885">StatefulSet</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p08101223181910"><a name="p08101223181910"></a><a name="p08101223181910"></a>Statefulset对象管理接口，包括Statefulset对象的创建、查询、修改、删除等接口。</p>
<p id="p1036081163320"><a name="p1036081163320"></a><a name="p1036081163320"></a>StatefulSet同样是Pod的Controller的一种。一个StatefulSet可以包含一个或多个Pod副本，不同的Pod副本的角色有区别，且每个Pod副本都有独立的访问域名，所以用户可以手动指定请求在Pod副本之间的分发路径。StatefulSet的Pod副本间不共享数据，因此每个Pod副本都会被分配独立的专属存储卷。</p>
</td>
</tr>
<tr id="row12496159161520"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1049610591151"><a name="p1049610591151"></a><a name="p1049610591151"></a><a href="#section1822314261185">Job</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p134393081919"><a name="p134393081919"></a><a name="p134393081919"></a>Job对象管理接口，包括Job对象的创建、查询、修改、删除等接口。</p>
<p id="p2026631573310"><a name="p2026631573310"></a><a name="p2026631573310"></a>Job是用来控制批处理型任务的资源对象。批处理业务与长期伺服业务（Deployment、Statefulset）的主要区别是批处理业务的运行有头有尾，而长期伺服业务在用户不停止的情况下永远运行。Job管理的Pod根据用户的设置把任务成功完成就自动退出了。</p>
</td>
</tr>
<tr id="row2027518598155"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p10276185916155"><a name="p10276185916155"></a><a name="p10276185916155"></a><a href="#section477116311381">Service</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p2027675910153"><a name="p2027675910153"></a><a name="p2027675910153"></a>Service对象管理接口，包括Service对象的创建、查询、修改、删除等接口。</p>
<p id="p19321836113313"><a name="p19321836113313"></a><a name="p19321836113313"></a><span>Service定义了这样一种抽象：一个Pod的逻辑分组，一种可以访问它们的策略（通常称为微服务）。</span></p>
</td>
</tr>
<tr id="row146566588151"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p17656155831518"><a name="p17656155831518"></a><a name="p17656155831518"></a><a href="#section10848153414818">Ingress</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p12656958151511"><a name="p12656958151511"></a><a name="p12656958151511"></a>Ingress对象管理接口，包括Ingress对象的创建、查询、修改、删除等接口。</p>
<p id="p188313373419"><a name="p188313373419"></a><a name="p188313373419"></a>Ingress是授权入站连接到达集群服务的规则集合。您可以给Ingress配置外部可访问的URL、负载均衡、SSL、基于名称的虚拟主机等。</p>
</td>
</tr>
<tr id="row31738719148"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p6749143431511"><a name="p6749143431511"></a><a name="p6749143431511"></a><a href="#section96612351882">ConfigMap</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p4572811102018"><a name="p4572811102018"></a><a name="p4572811102018"></a>Configmap对象管理接口，包括Configmap对象的创建、查询、修改、删除等接口。</p>
</td>
</tr>
<tr id="row7758330161810"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p07581530131819"><a name="p07581530131819"></a><a name="p07581530131819"></a><a href="#section95518361180">Secret</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p67475169203"><a name="p67475169203"></a><a name="p67475169203"></a>Secret对象管理接口，包括Secret对象的创建、查询、修改、删除等接口。</p>
</td>
</tr>
<tr id="row32428295185"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p1024212971820"><a name="p1024212971820"></a><a name="p1024212971820"></a><a href="#section114573714816">PersistentVolumeClaim</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p19478111614219"><a name="p19478111614219"></a><a name="p19478111614219"></a>PersistentVolumeClaim对象管理接口，包括PersistentVolumeClaim对象的创建、查询、修改、删除等接口。</p>
<p id="p8862152223419"><a name="p8862152223419"></a><a name="p8862152223419"></a>PersistentVolumeClaim（PVC）是用户存储的请求。 它类似于Pod，Pod申请CPU和内存，PVC申请存储资源。</p>
</td>
</tr>
<tr id="row1136183761816"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p413663714186"><a name="p413663714186"></a><a name="p413663714186"></a><a href="#section7210115621412">Event</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1444115556191"><a name="p1444115556191"></a><a name="p1444115556191"></a>Event对象管理接口，包括Event对象的查询接口。</p>
</td>
</tr>
<tr id="row156962284558"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p136974289555"><a name="p136974289555"></a><a name="p136974289555"></a><a href="#section1583211914508">API Groups</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1369722811556"><a name="p1369722811556"></a><a name="p1369722811556"></a>API GroupS查询接口，可以查询各个Group下的API资源。</p>
</td>
</tr>
<tr id="row1344152911558"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p934442916559"><a name="p934442916559"></a><a name="p934442916559"></a><a href="#section282871018505">Endpoint</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p113391713300"><a name="p113391713300"></a><a name="p113391713300"></a>Endpoint对象管理接口，包括Endpoint对象的查询接口。</p>
</td>
</tr>
<tr id="row02754303552"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p6275143085513"><a name="p6275143085513"></a><a name="p6275143085513"></a><a href="#section195241411145011">ReplicaSet</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p2027512305555"><a name="p2027512305555"></a><a name="p2027512305555"></a>ReplicaSet对象管理接口，包括ReplicaSet对象的查询接口。</p>
</td>
</tr>
<tr id="row15775163011573"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p147764306577"><a name="p147764306577"></a><a name="p147764306577"></a><a href="#section833512127540">VolcanoJob</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p2776183035714"><a name="p2776183035714"></a><a name="p2776183035714"></a>VolcanoJob对象管理接口，包括VolcanoJob对象的创建、查询、修改、删除接口。</p>
</td>
</tr>
<tr id="row118591324511"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p8860635451"><a name="p8860635451"></a><a name="p8860635451"></a><a href="TFJob.md">TFJob</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p1586043104519"><a name="p1586043104519"></a><a name="p1586043104519"></a>TFJob即Tensorflow任务，是基于Tensorflow开源框架的kubernetes自定义资源类型，有多种角色可以配置，能够帮助我们更简单地实现Tensorflow的单机或分布式训练。</p>
</td>
</tr>
<tr id="row1157711310452"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p165771813154517"><a name="p165771813154517"></a><a name="p165771813154517"></a><a href="MXJob.md">MXJob</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p18577513134517"><a name="p18577513134517"></a><a name="p18577513134517"></a>MXJob即MXNet任务，是基于MXNet开源框架的kubernetes自定义资源类型，有多种角色可以配置，能够帮助我们更简单地实现MXNet的训练。</p>
</td>
</tr>
<tr id="row2380510124513"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p638191015458"><a name="p638191015458"></a><a name="p638191015458"></a><a href="PyTorchJob.md">PyTorchJob</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p538111101458"><a name="p538111101458"></a><a name="p538111101458"></a>PyTorchJob即PyTorch任务，是基于PyTorch开源框架的kubernetes自定义资源类型，有多种角色可以配置，能够帮助我们更简单地实现PyTorch的训练。</p>
</td>
</tr>
<tr id="row117781617154410"><td class="cellrowborder" valign="top" headers="mcps1.1.4.1.1 "><p id="p87781817154410"><a name="p87781817154410"></a><a name="p87781817154410"></a><a href="#section187328377322">RBAC</a></p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.1.4.1.2 "><p id="p6778201744419"><a name="p6778201744419"></a><a name="p6778201744419"></a>通过权限设置可以让不同的用户或用户组拥有操作不同Kubernetes资源的权限。</p>
</td>
</tr>
</tbody>
</table>

## Network<a name="section13159414572"></a>

<a name="table177341359552"></a>
<table><thead align="left"><tr id="row973425919514"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p87342591555"><a name="p87342591555"></a><a name="p87342591555"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p157341859858"><a name="p157341859858"></a><a name="p157341859858"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row16734959259"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1373445920518"><a name="p1373445920518"></a><a name="p1373445920518"></a><a href="创建Network.md">创建Network</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p673416596519"><a name="p673416596519"></a><a name="p673416596519"></a>创建一个Network对象。</p>
<p id="p1071653911206"><a name="p1071653911206"></a><a name="p1071653911206"></a>Network对象是华为云CCI 新增对象，用于定义kubernetes中一个namespace内的网络与华为云虚拟私有云服务的子网和VPC的映射关系。</p>
</td>
</tr>
<tr id="row273411591512"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p87341059754"><a name="p87341059754"></a><a name="p87341059754"></a><a href="查询Network.md">查询Network</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p4734145920510"><a name="p4734145920510"></a><a name="p4734145920510"></a>查询Network信息。</p>
</td>
</tr>
<tr id="row12734559159"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1873418591652"><a name="p1873418591652"></a><a name="p1873418591652"></a><a href="查询所有Network.md">查询所有Network</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p117346596516"><a name="p117346596516"></a><a name="p117346596516"></a>查询指定namespace下的所有Network对象。</p>
</td>
</tr>
<tr id="row57349591520"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p9734195917511"><a name="p9734195917511"></a><a name="p9734195917511"></a><a href="查询Network状态.md">查询Network状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p173412591512"><a name="p173412591512"></a><a name="p173412591512"></a>查询一个指定Network对象的状态。</p>
</td>
</tr>
<tr id="row1473418590511"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1873418594515"><a name="p1873418594515"></a><a name="p1873418594515"></a><a href="删除Network.md">删除Network</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p27349591518"><a name="p27349591518"></a><a name="p27349591518"></a>删除一个指定Network对象。</p>
</td>
</tr>
<tr id="row1873495910510"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p373419591456"><a name="p373419591456"></a><a name="p373419591456"></a><a href="删除所有Network.md">删除所有Network</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p4734135911510"><a name="p4734135911510"></a><a name="p4734135911510"></a>删除指定namespace下的所有Network对象。</p>
</td>
</tr>
</tbody>
</table>

## Extended PersistentVolumeClaim<a name="section743818217318"></a>

<a name="table13439202119314"></a>
<table><thead align="left"><tr id="row9439102193117"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p34391821113113"><a name="p34391821113113"></a><a name="p34391821113113"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p54391821183110"><a name="p54391821183110"></a><a name="p54391821183110"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row9439132123114"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p14398216319"><a name="p14398216319"></a><a name="p14398216319"></a><a href="导入存储.md">导入存储</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p8439152103111"><a name="p8439152103111"></a><a name="p8439152103111"></a>导入已有存储到指定的命名空间。</p>
</td>
</tr>
<tr id="row2440102115319"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p944017213312"><a name="p944017213312"></a><a name="p944017213312"></a><a href="查询导入的PVC.md">查询导入的PVC</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p19440102143119"><a name="p19440102143119"></a><a name="p19440102143119"></a>查询指定命名空间下的PVC。</p>
</td>
</tr>
<tr id="row744092118317"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p9440152114316"><a name="p9440152114316"></a><a name="p9440152114316"></a><a href="解绑存储.md">解绑存储</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p3908185"><a name="p3908185"></a><a name="p3908185"></a>从指定命名空间解绑存储的接口。该接口扩展了原生的删除存储接口，增加了是否删除volume和存储类型的参数。</p>
</td>
</tr>
</tbody>
</table>

## Namespace<a name="section115511242677"></a>

<a name="table107701356677"></a>
<table><thead align="left"><tr id="row10770175615712"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p47701561470"><a name="p47701561470"></a><a name="p47701561470"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p10770656176"><a name="p10770656176"></a><a name="p10770656176"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row13770135620716"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p877017569716"><a name="p877017569716"></a><a name="p877017569716"></a><a href="创建Namespace.md">创建Namespace</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p127700561777"><a name="p127700561777"></a><a name="p127700561777"></a>创建一个Namespace。</p>
</td>
</tr>
<tr id="row177701056871"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p7770185617719"><a name="p7770185617719"></a><a name="p7770185617719"></a><a href="查询Namespace.md">查询Namespace</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p3770195611714"><a name="p3770195611714"></a><a name="p3770195611714"></a>查询Namespace的详细信息。</p>
</td>
</tr>
<tr id="row6535849114119"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1653513491417"><a name="p1653513491417"></a><a name="p1653513491417"></a><a href="列出Namespace.md">列出Namespace</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p16535154918414"><a name="p16535154918414"></a><a name="p16535154918414"></a>列出用户所有Namespace。</p>
</td>
</tr>
<tr id="row147701556973"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p177075613713"><a name="p177075613713"></a><a name="p177075613713"></a><a href="删除Namespace.md">删除Namespace</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p277012561717"><a name="p277012561717"></a><a name="p277012561717"></a>删除一个Namespace。</p>
</td>
</tr>
</tbody>
</table>

## Pod<a name="section2458101711812"></a>

<a name="table1147318177810"></a>
<table><thead align="left"><tr id="row54731717286"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p648961718811"><a name="p648961718811"></a><a name="p648961718811"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p16489201713819"><a name="p16489201713819"></a><a name="p16489201713819"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1248918173818"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p4489151716815"><a name="p4489151716815"></a><a name="p4489151716815"></a><a href="创建Pod.md">创建Pod</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p114896171184"><a name="p114896171184"></a><a name="p114896171184"></a>创建一个Pod。</p>
</td>
</tr>
<tr id="row54891817387"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1548971714814"><a name="p1548971714814"></a><a name="p1548971714814"></a><a href="查询Pod.md">查询Pod</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p9504111718813"><a name="p9504111718813"></a><a name="p9504111718813"></a>查询Pod的详细信息。</p>
</td>
</tr>
<tr id="row15504171714817"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p550471719811"><a name="p550471719811"></a><a name="p550471719811"></a><a href="查询指定Namespace下所有Pod.md">查询指定Namespace下所有Pod</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p950416177819"><a name="p950416177819"></a><a name="p950416177819"></a>查询所有Pod的详细信息。</p>
</td>
</tr>
<tr id="row15504151718818"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p150412175815"><a name="p150412175815"></a><a name="p150412175815"></a><a href="查询Pod状态.md">查询Pod状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p552017171810"><a name="p552017171810"></a><a name="p552017171810"></a>查询Pod对象的状态。</p>
</td>
</tr>
<tr id="row652021713814"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p145201617687"><a name="p145201617687"></a><a name="p145201617687"></a><a href="查询Pod日志.md">查询Pod日志</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1452081719812"><a name="p1452081719812"></a><a name="p1452081719812"></a>查询Pod的日志。</p>
</td>
</tr>
<tr id="row3701817184211"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p67013175425"><a name="p67013175425"></a><a name="p67013175425"></a><a href="列出用户所有的Pod.md">列出用户所有的Pod</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p207011017144216"><a name="p207011017144216"></a><a name="p207011017144216"></a>列出用户所有的Pod。</p>
</td>
</tr>
<tr id="row185209171683"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p185201174817"><a name="p185201174817"></a><a name="p185201174817"></a><a href="替换Pod.md">替换Pod</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1252013179811"><a name="p1252013179811"></a><a name="p1252013179811"></a>替换指定Pod。</p>
</td>
</tr>
<tr id="row8475035999"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p104757352918"><a name="p104757352918"></a><a name="p104757352918"></a><a href="更新Pod.md">更新Pod</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p144751635198"><a name="p144751635198"></a><a name="p144751635198"></a>更新Pod。</p>
</td>
</tr>
<tr id="row1883418363917"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p38348361693"><a name="p38348361693"></a><a name="p38348361693"></a><a href="删除Pod.md">删除Pod</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p10834103615917"><a name="p10834103615917"></a><a name="p10834103615917"></a>删除Pod。</p>
</td>
</tr>
<tr id="row17319123714910"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p131918373918"><a name="p131918373918"></a><a name="p131918373918"></a><a href="删除所有Pod.md">删除所有Pod</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p431917372911"><a name="p431917372911"></a><a name="p431917372911"></a>删除Namespace下所有Pod。</p>
</td>
</tr>
</tbody>
</table>

## Deployment<a name="section731718191482"></a>

<a name="table1433210191285"></a>
<table><thead align="left"><tr id="row7332161910816"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p133219191386"><a name="p133219191386"></a><a name="p133219191386"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p2332161918815"><a name="p2332161918815"></a><a name="p2332161918815"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row6349919386"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p734919192089"><a name="p734919192089"></a><a name="p734919192089"></a><a href="创建Deployment.md">创建Deployment</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p63491191289"><a name="p63491191289"></a><a name="p63491191289"></a>创建一个Deployment。</p>
</td>
</tr>
<tr id="row23493198814"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p234915191385"><a name="p234915191385"></a><a name="p234915191385"></a><a href="查询Deployment.md">查询Deployment</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p53491819382"><a name="p53491819382"></a><a name="p53491819382"></a>查询Deployment的详细信息。</p>
</td>
</tr>
<tr id="row16349161911810"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p203649193814"><a name="p203649193814"></a><a name="p203649193814"></a><a href="查询Namespace下所有Deployment.md">查询Namespace下所有Deployment</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p23641719984"><a name="p23641719984"></a><a name="p23641719984"></a>查询Namespace下所有Deployment的详细信息。</p>
</td>
</tr>
<tr id="row2036410191982"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p173643195819"><a name="p173643195819"></a><a name="p173643195819"></a><a href="查询Deployment状态.md">查询Deployment状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1436414191886"><a name="p1436414191886"></a><a name="p1436414191886"></a>查询Deployment的状态。</p>
</td>
</tr>
<tr id="row208889346424"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p18898342423"><a name="p18898342423"></a><a name="p18898342423"></a><a href="查询Deployment的伸缩操作.md">查询Deployment的伸缩操作</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p8889103415428"><a name="p8889103415428"></a><a name="p8889103415428"></a>查询Deployment伸缩操作。</p>
</td>
</tr>
<tr id="row1750353514215"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p0503035104211"><a name="p0503035104211"></a><a name="p0503035104211"></a><a href="列出用户所有Deployment.md">列出用户所有Deployment</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p750393516424"><a name="p750393516424"></a><a name="p750393516424"></a>列出用户所有的Deployment。</p>
</td>
</tr>
<tr id="row33644191284"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1036491915817"><a name="p1036491915817"></a><a name="p1036491915817"></a><a href="替换Deployment.md">替换Deployment</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1637913191981"><a name="p1637913191981"></a><a name="p1637913191981"></a>替换Deployment。</p>
</td>
</tr>
<tr id="row121918394423"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p22198391429"><a name="p22198391429"></a><a name="p22198391429"></a><a href="替换Deployment的伸缩操作.md">替换Deployment的伸缩操作</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p9219339124219"><a name="p9219339124219"></a><a name="p9219339124219"></a>替换Deployment伸缩操作。</p>
</td>
</tr>
<tr id="row437951918819"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1637991913811"><a name="p1637991913811"></a><a name="p1637991913811"></a><a href="更新Deployment.md">更新Deployment</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p73799192815"><a name="p73799192815"></a><a name="p73799192815"></a>更新Deployment。</p>
</td>
</tr>
<tr id="row5556843204217"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p255604354217"><a name="p255604354217"></a><a name="p255604354217"></a><a href="更新Deployment的伸缩操作.md">更新Deployment的伸缩操作</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p355624314216"><a name="p355624314216"></a><a name="p355624314216"></a>更新Deployment伸缩操作。</p>
</td>
</tr>
<tr id="row3830018141013"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p138301518141012"><a name="p138301518141012"></a><a name="p138301518141012"></a><a href="删除Deployment.md">删除Deployment</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p15830518141011"><a name="p15830518141011"></a><a name="p15830518141011"></a>删除Deployment。</p>
</td>
</tr>
<tr id="row1315141915103"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p231591991013"><a name="p231591991013"></a><a name="p231591991013"></a><a href="删除所有Deployment.md">删除所有Deployment</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p631515194108"><a name="p631515194108"></a><a name="p631515194108"></a>删除Namespace下所有Deployment。</p>
</td>
</tr>
</tbody>
</table>

## StatefulSet<a name="section43641211885"></a>

<a name="table43641216818"></a>
<table><thead align="left"><tr id="row193643215818"><th class="cellrowborder" valign="top" width="32.12%" id="mcps1.1.3.1.1"><p id="p53641521981"><a name="p53641521981"></a><a name="p53641521981"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.88%" id="mcps1.1.3.1.2"><p id="p1038013211987"><a name="p1038013211987"></a><a name="p1038013211987"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row18380721186"><td class="cellrowborder" valign="top" width="32.12%" headers="mcps1.1.3.1.1 "><p id="p238042115810"><a name="p238042115810"></a><a name="p238042115810"></a><a href="创建StatefulSet.md">创建StatefulSet</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.88%" headers="mcps1.1.3.1.2 "><p id="p238018210814"><a name="p238018210814"></a><a name="p238018210814"></a>创建StatefulSet。</p>
</td>
</tr>
<tr id="row338002118818"><td class="cellrowborder" valign="top" width="32.12%" headers="mcps1.1.3.1.1 "><p id="p133801121488"><a name="p133801121488"></a><a name="p133801121488"></a><a href="查询StatefulSet.md">查询StatefulSet</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.88%" headers="mcps1.1.3.1.2 "><p id="p9395321088"><a name="p9395321088"></a><a name="p9395321088"></a>查询StatefulSet的详细信息。</p>
</td>
</tr>
<tr id="row133951921089"><td class="cellrowborder" valign="top" width="32.12%" headers="mcps1.1.3.1.1 "><p id="p13395112110816"><a name="p13395112110816"></a><a name="p13395112110816"></a><a href="查询指定namespace下所有StatefulSet.md">查询指定namespace下所有StatefulSet</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.88%" headers="mcps1.1.3.1.2 "><p id="p1739514211082"><a name="p1739514211082"></a><a name="p1739514211082"></a>查询Namespace下所有StatefulSet的详细信息。</p>
</td>
</tr>
<tr id="row9395132117814"><td class="cellrowborder" valign="top" width="32.12%" headers="mcps1.1.3.1.1 "><p id="p113957213819"><a name="p113957213819"></a><a name="p113957213819"></a><a href="查询StatefulSet状态.md">查询StatefulSet状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.88%" headers="mcps1.1.3.1.2 "><p id="p04119211784"><a name="p04119211784"></a><a name="p04119211784"></a>查询StatefulSet状态。</p>
</td>
</tr>
<tr id="row6726113134316"><td class="cellrowborder" valign="top" width="32.12%" headers="mcps1.1.3.1.1 "><p id="p1272681394316"><a name="p1272681394316"></a><a name="p1272681394316"></a><a href="列出用户所有的StatefulSet.md">列出用户所有的StatefulSet</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.88%" headers="mcps1.1.3.1.2 "><p id="p27261913204314"><a name="p27261913204314"></a><a name="p27261913204314"></a>列出用户所有的Statefulset。</p>
</td>
</tr>
<tr id="row741111218811"><td class="cellrowborder" valign="top" width="32.12%" headers="mcps1.1.3.1.1 "><p id="p11411621587"><a name="p11411621587"></a><a name="p11411621587"></a><a href="替换StatefulSet.md">替换StatefulSet</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.88%" headers="mcps1.1.3.1.2 "><p id="p74113211584"><a name="p74113211584"></a><a name="p74113211584"></a>替换StatefulSet。</p>
</td>
</tr>
<tr id="row134113219810"><td class="cellrowborder" valign="top" width="32.12%" headers="mcps1.1.3.1.1 "><p id="p104112211587"><a name="p104112211587"></a><a name="p104112211587"></a><a href="更新StatefulSet.md">更新StatefulSet</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.88%" headers="mcps1.1.3.1.2 "><p id="p17427162119818"><a name="p17427162119818"></a><a name="p17427162119818"></a>更新StatefulSet。</p>
</td>
</tr>
<tr id="row16661132141111"><td class="cellrowborder" valign="top" width="32.12%" headers="mcps1.1.3.1.1 "><p id="p86611326110"><a name="p86611326110"></a><a name="p86611326110"></a><a href="删除StatefulSet.md">删除StatefulSet</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.88%" headers="mcps1.1.3.1.2 "><p id="p666192131111"><a name="p666192131111"></a><a name="p666192131111"></a>删除StatefulSet。</p>
</td>
</tr>
<tr id="row1214618351112"><td class="cellrowborder" valign="top" width="32.12%" headers="mcps1.1.3.1.1 "><p id="p1514619316111"><a name="p1514619316111"></a><a name="p1514619316111"></a><a href="删除所有StatefulSet.md">删除所有StatefulSet</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.88%" headers="mcps1.1.3.1.2 "><p id="p51468310117"><a name="p51468310117"></a><a name="p51468310117"></a>删除Namespace下所有StatefulSet。</p>
</td>
</tr>
</tbody>
</table>

## Job<a name="section1822314261185"></a>

<a name="table162232263813"></a>
<table><thead align="left"><tr id="row112232261382"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p4239152619816"><a name="p4239152619816"></a><a name="p4239152619816"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p152391926385"><a name="p152391926385"></a><a name="p152391926385"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1223913261080"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p7239126384"><a name="p7239126384"></a><a name="p7239126384"></a><a href="创建Job.md">创建Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p72541526489"><a name="p72541526489"></a><a name="p72541526489"></a>创建Job。</p>
</td>
</tr>
<tr id="row02549261588"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p182546263813"><a name="p182546263813"></a><a name="p182546263813"></a><a href="查询Job.md">查询Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1625411261812"><a name="p1625411261812"></a><a name="p1625411261812"></a>查询Job的详细信息。</p>
</td>
</tr>
<tr id="row162547261389"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p025416267816"><a name="p025416267816"></a><a name="p025416267816"></a><a href="查询指定namespace下所有Job.md">查询指定namespace下所有Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p16254172611811"><a name="p16254172611811"></a><a name="p16254172611811"></a>查询Namespace下所有Job的详细信息。</p>
</td>
</tr>
<tr id="row3270226485"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p627012261584"><a name="p627012261584"></a><a name="p627012261584"></a><a href="查询Job状态.md">查询Job状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p6270126282"><a name="p6270126282"></a><a name="p6270126282"></a>查询Job状态。</p>
</td>
</tr>
<tr id="row1455182624318"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p95642612432"><a name="p95642612432"></a><a name="p95642612432"></a><a href="列出用户所有Job.md">列出用户所有Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1756132684315"><a name="p1756132684315"></a><a name="p1756132684315"></a>列出用户所有Job。</p>
</td>
</tr>
<tr id="row327014261787"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1527082615814"><a name="p1527082615814"></a><a name="p1527082615814"></a><a href="替换Job.md">替换Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p8270426687"><a name="p8270426687"></a><a name="p8270426687"></a>替换Job。</p>
</td>
</tr>
<tr id="row13270192610815"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p22862266818"><a name="p22862266818"></a><a name="p22862266818"></a><a href="更新Job.md">更新Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p11286326386"><a name="p11286326386"></a><a name="p11286326386"></a>更新Job。</p>
</td>
</tr>
<tr id="row02173451114"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p62117346118"><a name="p62117346118"></a><a name="p62117346118"></a><a href="删除Job.md">删除Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p102193401114"><a name="p102193401114"></a><a name="p102193401114"></a>删除Job。</p>
</td>
</tr>
<tr id="row1272593417119"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p8725183420112"><a name="p8725183420112"></a><a name="p8725183420112"></a><a href="删除所有Job.md">删除所有Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p16725234141116"><a name="p16725234141116"></a><a name="p16725234141116"></a>删除Namespace下所有Job。</p>
</td>
</tr>
</tbody>
</table>

## Service<a name="section477116311381"></a>

<a name="table17786133118816"></a>
<table><thead align="left"><tr id="row127861531383"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p37861311588"><a name="p37861311588"></a><a name="p37861311588"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p1786631784"><a name="p1786631784"></a><a name="p1786631784"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row480120315819"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p148011131681"><a name="p148011131681"></a><a name="p148011131681"></a><a href="创建Service.md">创建Service</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1180114312818"><a name="p1180114312818"></a><a name="p1180114312818"></a>创建一个Service。</p>
</td>
</tr>
<tr id="row780193111820"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1080123116820"><a name="p1080123116820"></a><a name="p1080123116820"></a><a href="查询Service.md">查询Service</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p48011313813"><a name="p48011313813"></a><a name="p48011313813"></a>查询Service的详细信息。</p>
</td>
</tr>
<tr id="row1980119317812"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p18178311488"><a name="p18178311488"></a><a name="p18178311488"></a><a href="查询所有Service.md">查询所有Service</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p7817831788"><a name="p7817831788"></a><a name="p7817831788"></a>查询Namespace下所有Service的详细信息。</p>
</td>
</tr>
<tr id="row1381715310817"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1781718311387"><a name="p1781718311387"></a><a name="p1781718311387"></a><a href="查询service状态.md">查询service状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p12817331287"><a name="p12817331287"></a><a name="p12817331287"></a>查询指定的Service的状态。</p>
</td>
</tr>
<tr id="row73831819124"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p193816186127"><a name="p193816186127"></a><a name="p193816186127"></a><a href="删除Service.md">删除Service</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1438618181219"><a name="p1438618181219"></a><a name="p1438618181219"></a>删除Service。</p>
</td>
</tr>
</tbody>
</table>

## Ingress<a name="section10848153414818"></a>

<a name="table08641134984"></a>
<table><thead align="left"><tr id="row388019344810"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p58807341882"><a name="p58807341882"></a><a name="p58807341882"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p9895334588"><a name="p9895334588"></a><a name="p9895334588"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row15895834389"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p29123345810"><a name="p29123345810"></a><a name="p29123345810"></a><a href="创建Ingress.md">创建Ingress</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1691214345816"><a name="p1691214345816"></a><a name="p1691214345816"></a>创建Ingress。</p>
</td>
</tr>
<tr id="row092693413811"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p179265340818"><a name="p179265340818"></a><a name="p179265340818"></a><a href="查询Ingress.md">查询Ingress</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p59422034289"><a name="p59422034289"></a><a name="p59422034289"></a>查询Ingress的详细信息。</p>
</td>
</tr>
<tr id="row39424342084"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p15942153412817"><a name="p15942153412817"></a><a name="p15942153412817"></a><a href="查询所有Ingress.md">查询所有Ingress</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p11958234281"><a name="p11958234281"></a><a name="p11958234281"></a>查询Namespace下所有Ingress的详细信息。</p>
</td>
</tr>
<tr id="row189589341289"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p179731834389"><a name="p179731834389"></a><a name="p179731834389"></a><a href="查询Ingress状态.md">查询Ingress状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p159737342813"><a name="p159737342813"></a><a name="p159737342813"></a>查询Ingress状态。</p>
</td>
</tr>
<tr id="row139731434380"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p99895342815"><a name="p99895342815"></a><a name="p99895342815"></a><a href="替换Ingress.md">替换Ingress</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p18989163412820"><a name="p18989163412820"></a><a name="p18989163412820"></a>替换Ingress。</p>
</td>
</tr>
<tr id="row10411356811"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1544351820"><a name="p1544351820"></a><a name="p1544351820"></a><a href="更新Ingress.md">更新Ingress</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p920935187"><a name="p920935187"></a><a name="p920935187"></a>更新Ingress。</p>
</td>
</tr>
<tr id="row1261925181219"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p561913512126"><a name="p561913512126"></a><a name="p561913512126"></a><a href="删除Ingress.md">删除Ingress</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p861915119120"><a name="p861915119120"></a><a name="p861915119120"></a>删除Ingress。</p>
</td>
</tr>
<tr id="row7104185241211"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p19104105216128"><a name="p19104105216128"></a><a name="p19104105216128"></a><a href="删除所有ingress.md">删除所有ingress</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1104252141217"><a name="p1104252141217"></a><a name="p1104252141217"></a>删除Namespace下所有Ingress。</p>
</td>
</tr>
</tbody>
</table>

## ConfigMap<a name="section96612351882"></a>

<a name="table1267616358814"></a>
<table><thead align="left"><tr id="row1367617351683"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p16676203516811"><a name="p16676203516811"></a><a name="p16676203516811"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p1969263513819"><a name="p1969263513819"></a><a name="p1969263513819"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row16692113513813"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p86923351387"><a name="p86923351387"></a><a name="p86923351387"></a><a href="创建ConfigMap.md">创建ConfigMap</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p76921635787"><a name="p76921635787"></a><a name="p76921635787"></a>创建ConfigMap。</p>
</td>
</tr>
<tr id="row2692935683"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p7707113516811"><a name="p7707113516811"></a><a name="p7707113516811"></a><a href="查询ConfigMap.md">查询ConfigMap</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p16707335682"><a name="p16707335682"></a><a name="p16707335682"></a>查询ConfigMap详细信息。</p>
</td>
</tr>
<tr id="row5707153512812"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p127239351488"><a name="p127239351488"></a><a name="p127239351488"></a><a href="查询所有ConfigMap.md">查询所有ConfigMap</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1972319351987"><a name="p1972319351987"></a><a name="p1972319351987"></a>查询Namespace下所有ConfigMap的详细信息。</p>
</td>
</tr>
<tr id="row14723535585"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p172310351484"><a name="p172310351484"></a><a name="p172310351484"></a><a href="替换ConfigMap.md">替换ConfigMap</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p57233354812"><a name="p57233354812"></a><a name="p57233354812"></a>替换ConfigMap。</p>
</td>
</tr>
<tr id="row67393351884"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p27392351481"><a name="p27392351481"></a><a name="p27392351481"></a><a href="更新ConfigMap.md">更新ConfigMap</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1973933513814"><a name="p1973933513814"></a><a name="p1973933513814"></a>更新ConfigMap。</p>
</td>
</tr>
<tr id="row18739103520813"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p5739163510815"><a name="p5739163510815"></a><a name="p5739163510815"></a><a href="删除ConfigMap.md">删除ConfigMap</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p207546351989"><a name="p207546351989"></a><a name="p207546351989"></a>删除ConfigMap。</p>
</td>
</tr>
<tr id="row4726311134"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p127293181310"><a name="p127293181310"></a><a name="p127293181310"></a><a href="删除所有ConfigMap.md">删除所有ConfigMap</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p172183115135"><a name="p172183115135"></a><a name="p172183115135"></a>删除Namespace下所有ConfigMap。</p>
</td>
</tr>
</tbody>
</table>

## Secret<a name="section95518361180"></a>

<a name="table855113366814"></a>
<table><thead align="left"><tr id="row135671336782"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p135672361183"><a name="p135672361183"></a><a name="p135672361183"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p1456714366815"><a name="p1456714366815"></a><a name="p1456714366815"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row05833361686"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p15583173610816"><a name="p15583173610816"></a><a name="p15583173610816"></a><a href="创建Secret.md">创建Secret</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p185831836282"><a name="p185831836282"></a><a name="p185831836282"></a>创建Secret。</p>
</td>
</tr>
<tr id="row175837362814"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p759920361983"><a name="p759920361983"></a><a name="p759920361983"></a><a href="替换Secret.md">替换Secret</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1359943611819"><a name="p1359943611819"></a><a name="p1359943611819"></a>替换Secret。</p>
</td>
</tr>
<tr id="row159916361882"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1459917366820"><a name="p1459917366820"></a><a name="p1459917366820"></a><a href="更新Secret.md">更新Secret</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p66143361782"><a name="p66143361782"></a><a name="p66143361782"></a>更新Secret中部分信息。</p>
</td>
</tr>
<tr id="row66142361889"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p106140361488"><a name="p106140361488"></a><a name="p106140361488"></a><a href="删除Secret.md">删除Secret</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1261420367818"><a name="p1261420367818"></a><a name="p1261420367818"></a>删除Secret。</p>
</td>
</tr>
<tr id="row1614103619816"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1629036286"><a name="p1629036286"></a><a name="p1629036286"></a><a href="删除所有Secret.md">删除所有Secret</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p156291036582"><a name="p156291036582"></a><a name="p156291036582"></a>删除Namespace下所有Secret。</p>
</td>
</tr>
</tbody>
</table>

## PersistentVolumeClaim<a name="section114573714816"></a>

<a name="table181452371281"></a>
<table><thead align="left"><tr id="row1016111377816"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p71614371884"><a name="p71614371884"></a><a name="p71614371884"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p131611371283"><a name="p131611371283"></a><a name="p131611371283"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row217793711811"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p151771737284"><a name="p151771737284"></a><a name="p151771737284"></a><a href="创建PersistentVolumeClaim.md">创建PersistentVolumeClaim</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p217720371283"><a name="p217720371283"></a><a name="p217720371283"></a>创建PersistentVolumeClaim。</p>
</td>
</tr>
<tr id="row819223719817"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1819218375811"><a name="p1819218375811"></a><a name="p1819218375811"></a><a href="查询PersistentVolumeClaim.md">查询PersistentVolumeClaim</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p11928371982"><a name="p11928371982"></a><a name="p11928371982"></a>查询PersistentVolumeClaim。</p>
</td>
</tr>
<tr id="row5192937489"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p119253720815"><a name="p119253720815"></a><a name="p119253720815"></a><a href="查询所有PersistentVolumeClaim.md">查询所有PersistentVolumeClaim</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p1120716371186"><a name="p1120716371186"></a><a name="p1120716371186"></a>查询Namespace下的所有PersistentVolumeClaim。</p>
</td>
</tr>
<tr id="row10207837189"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p142072037882"><a name="p142072037882"></a><a name="p142072037882"></a><a href="删除PersistentVolumeClaim.md">删除PersistentVolumeClaim</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p8207173713818"><a name="p8207173713818"></a><a name="p8207173713818"></a>删除PersistentVolumeClaim。</p>
</td>
</tr>
</tbody>
</table>

## Event<a name="section7210115621412"></a>

<a name="table152101556181410"></a>
<table><thead align="left"><tr id="row8226195611414"><th class="cellrowborder" valign="top" width="32.11%" id="mcps1.1.3.1.1"><p id="p1022665619148"><a name="p1022665619148"></a><a name="p1022665619148"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.89%" id="mcps1.1.3.1.2"><p id="p18226856141410"><a name="p18226856141410"></a><a name="p18226856141410"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2242115681418"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p20757377157"><a name="p20757377157"></a><a name="p20757377157"></a><a href="查询Event.md">查询Event</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p4257115661410"><a name="p4257115661410"></a><a name="p4257115661410"></a>查询Event详细信息。</p>
</td>
</tr>
<tr id="row19257155615145"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p1775714781515"><a name="p1775714781515"></a><a name="p1775714781515"></a><a href="查询所有Event.md">查询所有Event</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p19273155691411"><a name="p19273155691411"></a><a name="p19273155691411"></a>查询Namespace下所有Event的详细信息。</p>
</td>
</tr>
<tr id="row628975615141"><td class="cellrowborder" valign="top" width="32.11%" headers="mcps1.1.3.1.1 "><p id="p475717711510"><a name="p475717711510"></a><a name="p475717711510"></a><a href="删除Event.md">删除Event</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.89%" headers="mcps1.1.3.1.2 "><p id="p83048568146"><a name="p83048568146"></a><a name="p83048568146"></a>删除Event。</p>
</td>
</tr>
</tbody>
</table>

## API Groups<a name="section1583211914508"></a>

<a name="table627374417502"></a>
<table><thead align="left"><tr id="row9274204412509"><th class="cellrowborder" valign="top" width="32.1%" id="mcps1.1.3.1.1"><p id="p42740442509"><a name="p42740442509"></a><a name="p42740442509"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.9%" id="mcps1.1.3.1.2"><p id="p7274134405019"><a name="p7274134405019"></a><a name="p7274134405019"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row72746447502"><td class="cellrowborder" valign="top" width="32.1%" headers="mcps1.1.3.1.1 "><p id="p1327454415020"><a name="p1327454415020"></a><a name="p1327454415020"></a><a href="列出APIVersions.md">列出APIVersions</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.9%" headers="mcps1.1.3.1.2 "><p id="p0274944135015"><a name="p0274944135015"></a><a name="p0274944135015"></a>列出所有API Version。</p>
</td>
</tr>
<tr id="row12274134415506"><td class="cellrowborder" valign="top" width="32.1%" headers="mcps1.1.3.1.1 "><p id="p16274204415509"><a name="p16274204415509"></a><a name="p16274204415509"></a><a href="列出APIGroups.md">列出APIGroups</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.9%" headers="mcps1.1.3.1.2 "><p id="p17274124435015"><a name="p17274124435015"></a><a name="p17274124435015"></a>列出所有API Group。</p>
</td>
</tr>
<tr id="row3274184413505"><td class="cellrowborder" valign="top" width="32.1%" headers="mcps1.1.3.1.1 "><p id="p32745444502"><a name="p32745444502"></a><a name="p32745444502"></a><a href="列出所有extensions-v1beta1版本的API.md">列出所有extensions/v1beta1版本的API</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.9%" headers="mcps1.1.3.1.2 "><p id="p1027484435017"><a name="p1027484435017"></a><a name="p1027484435017"></a>列出所有extensions/v1beata1版本的API。</p>
</td>
</tr>
<tr id="row12274144411500"><td class="cellrowborder" valign="top" width="32.1%" headers="mcps1.1.3.1.1 "><p id="p5274844145015"><a name="p5274844145015"></a><a name="p5274844145015"></a><a href="列出所有apps-v1版本的API.md">列出所有apps/v1版本的API</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.9%" headers="mcps1.1.3.1.2 "><p id="p55051913123214"><a name="p55051913123214"></a><a name="p55051913123214"></a>列出所有apps/v1版本的API。</p>
</td>
</tr>
<tr id="row427464416504"><td class="cellrowborder" valign="top" width="32.1%" headers="mcps1.1.3.1.1 "><p id="p327419447507"><a name="p327419447507"></a><a name="p327419447507"></a><a href="列出所有apps-v1beta1版本的API.md">列出所有apps/v1beta1版本的API</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.9%" headers="mcps1.1.3.1.2 "><p id="p651571333212"><a name="p651571333212"></a><a name="p651571333212"></a>列出所有apps/v1beata1版本的API。</p>
</td>
</tr>
<tr id="row102741441501"><td class="cellrowborder" valign="top" width="32.1%" headers="mcps1.1.3.1.1 "><p id="p8274194475014"><a name="p8274194475014"></a><a name="p8274194475014"></a><a href="列出所有batch-v1版本的API.md">列出所有batch/v1版本的API</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.9%" headers="mcps1.1.3.1.2 "><p id="p6528141317328"><a name="p6528141317328"></a><a name="p6528141317328"></a>列出所有batch/v1版本的API。</p>
</td>
</tr>
<tr id="row2027464413501"><td class="cellrowborder" valign="top" width="32.1%" headers="mcps1.1.3.1.1 "><p id="p327418448503"><a name="p327418448503"></a><a name="p327418448503"></a><a href="列出所有networking-cci-io-v1beta1版本的API.md">列出所有networking.cci.io/v1beta1版本的API</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.9%" headers="mcps1.1.3.1.2 "><p id="p1053811136320"><a name="p1053811136320"></a><a name="p1053811136320"></a>列出所有networwking.cci.io/v1beata1版本的API。</p>
</td>
</tr>
<tr id="row9590428165113"><td class="cellrowborder" valign="top" width="32.1%" headers="mcps1.1.3.1.1 "><p id="p11591192815515"><a name="p11591192815515"></a><a name="p11591192815515"></a><a href="列出所有v1版本的API.md">列出所有v1版本的API</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.9%" headers="mcps1.1.3.1.2 "><p id="p185479133329"><a name="p185479133329"></a><a name="p185479133329"></a>列出所有v1版本的API。</p>
</td>
</tr>
</tbody>
</table>

## Endpoint<a name="section282871018505"></a>

<a name="table6621151319527"></a>
<table><thead align="left"><tr id="row16622151305214"><th class="cellrowborder" valign="top" width="32.23%" id="mcps1.1.3.1.1"><p id="p1062241325211"><a name="p1062241325211"></a><a name="p1062241325211"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.77%" id="mcps1.1.3.1.2"><p id="p562291319525"><a name="p562291319525"></a><a name="p562291319525"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1662281335216"><td class="cellrowborder" valign="top" width="32.23%" headers="mcps1.1.3.1.1 "><p id="p116221813165219"><a name="p116221813165219"></a><a name="p116221813165219"></a><a href="查询Endpoint.md">查询Endpoint</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.77%" headers="mcps1.1.3.1.2 "><p id="p1962211136520"><a name="p1962211136520"></a><a name="p1962211136520"></a>查询Endpoint。</p>
</td>
</tr>
<tr id="row8622613145215"><td class="cellrowborder" valign="top" width="32.23%" headers="mcps1.1.3.1.1 "><p id="p162221310525"><a name="p162221310525"></a><a name="p162221310525"></a><a href="查询所有Endpoints.md">查询所有Endpoints</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.77%" headers="mcps1.1.3.1.2 "><p id="p71108357543"><a name="p71108357543"></a><a name="p71108357543"></a>查询所有Endpoints。</p>
</td>
</tr>
</tbody>
</table>

## ReplicaSet<a name="section195241411145011"></a>

<a name="table48581059115212"></a>
<table><thead align="left"><tr id="row178584599520"><th class="cellrowborder" valign="top" width="32.43%" id="mcps1.1.3.1.1"><p id="p954214712532"><a name="p954214712532"></a><a name="p954214712532"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="67.57%" id="mcps1.1.3.1.2"><p id="p145488795315"><a name="p145488795315"></a><a name="p145488795315"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row7858559135210"><td class="cellrowborder" valign="top" width="32.43%" headers="mcps1.1.3.1.1 "><p id="p3858159165215"><a name="p3858159165215"></a><a name="p3858159165215"></a><a href="查询所有ReplicaSets.md">查询所有ReplicaSets</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.57%" headers="mcps1.1.3.1.2 "><p id="p12858359155214"><a name="p12858359155214"></a><a name="p12858359155214"></a>查询所有ReplicaSets。</p>
</td>
</tr>
</tbody>
</table>

## VolcanoJob<a name="section833512127540"></a>

<a name="table5335512155419"></a>
<table><thead align="left"><tr id="row15336191213548"><th class="cellrowborder" valign="top" width="31.869999999999997%" id="mcps1.1.3.1.1"><p id="p1336112125410"><a name="p1336112125410"></a><a name="p1336112125410"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="68.13%" id="mcps1.1.3.1.2"><p id="p3336512145419"><a name="p3336512145419"></a><a name="p3336512145419"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row055383310547"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p8554133205414"><a name="p8554133205414"></a><a name="p8554133205414"></a><a href="获取namespace下的所有Volcano-Job.md">获取namespace下的所有Volcano Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p19555103355413"><a name="p19555103355413"></a><a name="p19555103355413"></a>查询命名空间下所有的Volcano Job。</p>
</td>
</tr>
<tr id="row119410385549"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p619403855410"><a name="p619403855410"></a><a name="p619403855410"></a><a href="创建Volcano-Job.md">创建Volcano Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p81941238115414"><a name="p81941238115414"></a><a name="p81941238115414"></a>创建Volcano Job。</p>
</td>
</tr>
<tr id="row16194838175417"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p51941386541"><a name="p51941386541"></a><a name="p51941386541"></a><a href="删除namespace下的所有Volcano-Job.md">删除namespace下的所有Volcano Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p1194138145416"><a name="p1194138145416"></a><a name="p1194138145416"></a>删除命名空间下的所有Volcano Job。</p>
</td>
</tr>
<tr id="row09611445542"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p9961644185410"><a name="p9961644185410"></a><a name="p9961644185410"></a><a href="查询Volcano-Job详情.md">查询Volcano Job详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p79618449548"><a name="p79618449548"></a><a name="p79618449548"></a>查询Volcano Job的详细信息。</p>
</td>
</tr>
<tr id="row189618445543"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p1096113441546"><a name="p1096113441546"></a><a name="p1096113441546"></a><a href="替换Volcano-Job.md">替换Volcano Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p139615447546"><a name="p139615447546"></a><a name="p139615447546"></a>替换Volcano Job。</p>
</td>
</tr>
<tr id="row6961104455417"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p496174445411"><a name="p496174445411"></a><a name="p496174445411"></a><a href="删除Volcano-Job.md">删除Volcano Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p1496114414545"><a name="p1496114414545"></a><a name="p1496114414545"></a>删除Volcano Job。</p>
</td>
</tr>
<tr id="row79614446547"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p8961174475419"><a name="p8961174475419"></a><a name="p8961174475419"></a><a href="更新Volcano-Job.md">更新Volcano Job</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p15961174415410"><a name="p15961174415410"></a><a name="p15961174415410"></a>更新Volcano Job。</p>
</td>
</tr>
</tbody>
</table>

## TFJob<a name="section185645171614"></a>

<a name="table5856655165"></a>
<table><thead align="left"><tr id="row138571559167"><th class="cellrowborder" valign="top" width="31.869999999999997%" id="mcps1.1.3.1.1"><p id="p168571057164"><a name="p168571057164"></a><a name="p168571057164"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="68.13%" id="mcps1.1.3.1.2"><p id="p5857195191618"><a name="p5857195191618"></a><a name="p5857195191618"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row13857155151616"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p4857857166"><a name="p4857857166"></a><a name="p4857857166"></a><a href="创建TFJob.md">创建TFJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p1126719141184"><a name="p1126719141184"></a><a name="p1126719141184"></a>创建TFJob。</p>
</td>
</tr>
<tr id="row1885785161617"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p108580516167"><a name="p108580516167"></a><a name="p108580516167"></a><a href="查询TFJob.md">查询TFJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p16264141401814"><a name="p16264141401814"></a><a name="p16264141401814"></a><span>查询TFJob的详细信息。</span></p>
</td>
</tr>
<tr id="row38581859164"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p2858175101612"><a name="p2858175101612"></a><a name="p2858175101612"></a><a href="查询指定namespace下的所有TFJob.md">查询指定namespace下的所有TFJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p1385895131611"><a name="p1385895131611"></a><a name="p1385895131611"></a>查询Namespace下所有TFJob的详细信息。</p>
</td>
</tr>
<tr id="row1985985131615"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p185916511167"><a name="p185916511167"></a><a name="p185916511167"></a><a href="删除namespace下的所有TFJob.md">删除namespace下的所有TFJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p48597561616"><a name="p48597561616"></a><a name="p48597561616"></a>删除命名空间下的所有TFJob。</p>
</td>
</tr>
<tr id="row1785915151610"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p98591358163"><a name="p98591358163"></a><a name="p98591358163"></a><a href="删除TFJob.md">删除TFJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p16860105111613"><a name="p16860105111613"></a><a name="p16860105111613"></a>删除TFJob。</p>
</td>
</tr>
<tr id="row3860051168"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p38601251168"><a name="p38601251168"></a><a name="p38601251168"></a><a href="更新TFJob.md">更新TFJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p188602054167"><a name="p188602054167"></a><a name="p188602054167"></a>更新TFJob。</p>
</td>
</tr>
<tr id="row18601958160"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p19861859163"><a name="p19861859163"></a><a name="p19861859163"></a><a href="替换TFJob.md">替换TFJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p1186114531618"><a name="p1186114531618"></a><a name="p1186114531618"></a>替换TFJob。</p>
</td>
</tr>
</tbody>
</table>

## MXJob<a name="section8941628191918"></a>

<a name="table794192831918"></a>
<table><thead align="left"><tr id="row16942122891911"><th class="cellrowborder" valign="top" width="31.869999999999997%" id="mcps1.1.3.1.1"><p id="p4942728201916"><a name="p4942728201916"></a><a name="p4942728201916"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="68.13%" id="mcps1.1.3.1.2"><p id="p1494252831914"><a name="p1494252831914"></a><a name="p1494252831914"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row10942192816190"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p7943628191916"><a name="p7943628191916"></a><a name="p7943628191916"></a><a href="创建MXJob.md">创建MXJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p194362810192"><a name="p194362810192"></a><a name="p194362810192"></a>创建MXJob。</p>
</td>
</tr>
<tr id="row5943122841918"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p159431428151919"><a name="p159431428151919"></a><a name="p159431428151919"></a><a href="查询MXJob.md">查询MXJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p594314286198"><a name="p594314286198"></a><a name="p594314286198"></a><span>查询MXJob的详细信息。</span></p>
</td>
</tr>
<tr id="row1943128151917"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p12943628111913"><a name="p12943628111913"></a><a name="p12943628111913"></a><a href="查询指定namespace下的所有MXJob.md">查询指定namespace下的所有MXJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p1194442891918"><a name="p1194442891918"></a><a name="p1194442891918"></a>查询Namespace下所有MXJob的详细信息。</p>
</td>
</tr>
<tr id="row694417281191"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p19446282196"><a name="p19446282196"></a><a name="p19446282196"></a><a href="删除namespace下的所有MXJob.md">删除namespace下的所有MXJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p149441428141917"><a name="p149441428141917"></a><a name="p149441428141917"></a>删除命名空间下的所有MXJob。</p>
</td>
</tr>
<tr id="row17944202811195"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p1494462813190"><a name="p1494462813190"></a><a name="p1494462813190"></a><a href="删除MXJob.md">删除MXJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p10944628201911"><a name="p10944628201911"></a><a name="p10944628201911"></a>删除MXJob。</p>
</td>
</tr>
<tr id="row109450283196"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p2094532861913"><a name="p2094532861913"></a><a name="p2094532861913"></a><a href="更新MXJob.md">更新MXJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p29454287192"><a name="p29454287192"></a><a name="p29454287192"></a>更新MXJob。</p>
</td>
</tr>
<tr id="row12945202841919"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p1194512282192"><a name="p1194512282192"></a><a name="p1194512282192"></a><a href="替换MXJob.md">替换MXJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p149451528121911"><a name="p149451528121911"></a><a name="p149451528121911"></a>替换MXJob。</p>
</td>
</tr>
</tbody>
</table>

## PyTorchJob<a name="section1582883081918"></a>

<a name="table108281230161917"></a>
<table><thead align="left"><tr id="row4828133031912"><th class="cellrowborder" valign="top" width="31.869999999999997%" id="mcps1.1.3.1.1"><p id="p118287306198"><a name="p118287306198"></a><a name="p118287306198"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="68.13%" id="mcps1.1.3.1.2"><p id="p28294303198"><a name="p28294303198"></a><a name="p28294303198"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2829163016193"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p88291530111912"><a name="p88291530111912"></a><a name="p88291530111912"></a><a href="创建PyTorchJob.md">创建PyTorchJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p18829113011192"><a name="p18829113011192"></a><a name="p18829113011192"></a>创建PyTorchJob。</p>
</td>
</tr>
<tr id="row18829730141917"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p1282919306195"><a name="p1282919306195"></a><a name="p1282919306195"></a><a href="查询PyTorchJob.md">查询PyTorchJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p882916302192"><a name="p882916302192"></a><a name="p882916302192"></a><span>查询PyTorchJob的详细信息。</span></p>
</td>
</tr>
<tr id="row108293308193"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p198291430121913"><a name="p198291430121913"></a><a name="p198291430121913"></a><a href="查询指定namespace下的所有PyTorchJob.md">查询指定namespace下的所有PyTorchJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p4829133031914"><a name="p4829133031914"></a><a name="p4829133031914"></a>查询Namespace下所有PyTorchJob的详细信息。</p>
</td>
</tr>
<tr id="row108292030171910"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p683013309198"><a name="p683013309198"></a><a name="p683013309198"></a><a href="删除namespace下的所有PyTorchJob.md">删除namespace下的所有PyTorchJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p7830113014195"><a name="p7830113014195"></a><a name="p7830113014195"></a>删除命名空间下的所有PyTorchJob。</p>
</td>
</tr>
<tr id="row14830530131913"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p1183013021912"><a name="p1183013021912"></a><a name="p1183013021912"></a><a href="删除PyTorchJob.md">删除PyTorchJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p38301730141911"><a name="p38301730141911"></a><a name="p38301730141911"></a>删除PyTorchJob。</p>
</td>
</tr>
<tr id="row15830123015197"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p1483018309195"><a name="p1483018309195"></a><a name="p1483018309195"></a><a href="更新PyTorchJob.md">更新PyTorchJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p5830193061915"><a name="p5830193061915"></a><a name="p5830193061915"></a>更新PyTorchJob。</p>
</td>
</tr>
<tr id="row6830730201914"><td class="cellrowborder" valign="top" width="31.869999999999997%" headers="mcps1.1.3.1.1 "><p id="p1383043091920"><a name="p1383043091920"></a><a name="p1383043091920"></a><a href="替换PyTorchJob.md">替换PyTorchJob</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.13%" headers="mcps1.1.3.1.2 "><p id="p1383083081911"><a name="p1383083081911"></a><a name="p1383083081911"></a>替换PyTorchJob。</p>
</td>
</tr>
</tbody>
</table>

## RBAC<a name="section187328377322"></a>

**表 1**  RBAC

<a name="table9795194911260"></a>
<table><thead align="left"><tr id="row5796549112610"><th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.1"><p id="p102791555192715"><a name="p102791555192715"></a><a name="p102791555192715"></a>API</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.3.1.2"><p id="p92808553276"><a name="p92808553276"></a><a name="p92808553276"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row3796749172618"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p197971649162614"><a name="p197971649162614"></a><a name="p197971649162614"></a><a href="获取指定的ClusterRole.md">获取指定的ClusterRole</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p14449814192918"><a name="p14449814192918"></a><a name="p14449814192918"></a>获取指定的ClusterRole。</p>
</td>
</tr>
<tr id="row1879714496265"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p17974494267"><a name="p17974494267"></a><a name="p17974494267"></a><a href="获取ClusterRole列表.md">获取ClusterRole列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p1644931416297"><a name="p1644931416297"></a><a name="p1644931416297"></a>获取ClusterRole列表。</p>
</td>
</tr>
<tr id="row9850164414386"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p12850104493811"><a name="p12850104493811"></a><a name="p12850104493811"></a><a href="创建RoleBinding.md">创建RoleBinding</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p14790163819435"><a name="p14790163819435"></a><a name="p14790163819435"></a>创建RoleBinding。</p>
</td>
</tr>
<tr id="row12422184518384"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p7422645113819"><a name="p7422645113819"></a><a name="p7422645113819"></a><a href="更新指定的RoleBinding.md">更新指定的RoleBinding</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p11790163814431"><a name="p11790163814431"></a><a name="p11790163814431"></a>部分更新指定的RoleBinding。</p>
</td>
</tr>
<tr id="row1299824517389"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p13998144533811"><a name="p13998144533811"></a><a name="p13998144533811"></a><a href="替换指定的RoleBinding.md">替换指定的RoleBinding</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p187901538164315"><a name="p187901538164315"></a><a name="p187901538164315"></a>替换指定的RoleBinding。</p>
</td>
</tr>
<tr id="row553474623820"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p12534144643816"><a name="p12534144643816"></a><a name="p12534144643816"></a><a href="删除指定的RoleBinding.md">删除指定的RoleBinding</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p8791113884313"><a name="p8791113884313"></a><a name="p8791113884313"></a>删除指定的RoleBinding。</p>
</td>
</tr>
<tr id="row96408470383"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p15640194712381"><a name="p15640194712381"></a><a name="p15640194712381"></a><a href="获取指定的RoleBinding.md">获取指定的RoleBinding</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p8792138144316"><a name="p8792138144316"></a><a name="p8792138144316"></a>获取指定的RoleBinding。</p>
</td>
</tr>
<tr id="row4230124883810"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p323110487381"><a name="p323110487381"></a><a name="p323110487381"></a><a href="获取指定namespace下RoleBinding列表.md">获取指定namespace下RoleBinding列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p7792938134311"><a name="p7792938134311"></a><a name="p7792938134311"></a>列出指定namespace下的RoleBinding列表。</p>
</td>
</tr>
<tr id="row895614819382"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.1 "><p id="p1956748153814"><a name="p1956748153814"></a><a name="p1956748153814"></a><a href="获取RoleBinding列表.md">获取RoleBinding列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.3.1.2 "><p id="p20793938164315"><a name="p20793938164315"></a><a name="p20793938164315"></a>获取RoleBinding列表。</p>
</td>
</tr>
</tbody>
</table>

