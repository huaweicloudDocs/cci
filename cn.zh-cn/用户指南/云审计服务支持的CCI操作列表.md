# 云审计服务支持的CCI操作列表<a name="cci_01_0084"></a>

CCI通过云审计服务（Cloud Trace Service，简称CTS）为您提供云服务资源的操作记录，记录内容包括您从云管理控制台或者开放API发起的的云服务资源操作请求以及每次请求的结果，供您查询、审计和回溯使用。

**表 1**  云审计服务支持的CCI操作列表

<a name="table10122133613599"></a>
<table><thead align="left"><tr id="row1612243618593"><th class="cellrowborder" valign="top" width="51.35999999999999%" id="mcps1.2.3.1.1"><p id="p5122153665915"><a name="p5122153665915"></a><a name="p5122153665915"></a>操作名称</p>
</th>
<th class="cellrowborder" valign="top" width="48.64%" id="mcps1.2.3.1.2"><p id="p712203655914"><a name="p712203655914"></a><a name="p712203655914"></a>事件名称</p>
</th>
</tr>
</thead>
<tbody><tr id="row14122193635917"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p135461825104216"><a name="p135461825104216"></a><a name="p135461825104216"></a>创建一个Service对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p45457255423"><a name="p45457255423"></a><a name="p45457255423"></a>createService</p>
</td>
</tr>
<tr id="row1512383615911"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p6546125164216"><a name="p6546125164216"></a><a name="p6546125164216"></a>删除一个Service对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p185463250429"><a name="p185463250429"></a><a name="p185463250429"></a>deleteService</p>
</td>
</tr>
<tr id="row2123103625916"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p13546025164210"><a name="p13546025164210"></a><a name="p13546025164210"></a>删除指定Namespace下的所有Service对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p2546172514427"><a name="p2546172514427"></a><a name="p2546172514427"></a>deleteServicesByNamespace</p>
</td>
</tr>
<tr id="row5816121312386"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p954612574214"><a name="p954612574214"></a><a name="p954612574214"></a>替换指定的Service对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p3546162519428"><a name="p3546162519428"></a><a name="p3546162519428"></a>replaceService</p>
</td>
</tr>
<tr id="row546661415383"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p454611251428"><a name="p454611251428"></a><a name="p454611251428"></a>更新指定的Service对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p85461325144212"><a name="p85461325144212"></a><a name="p85461325144212"></a>updateService</p>
</td>
</tr>
<tr id="row168015145382"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p354682513426"><a name="p354682513426"></a><a name="p354682513426"></a>删除一个Endpoint对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p954612514424"><a name="p954612514424"></a><a name="p954612514424"></a>deleteEndpoint</p>
</td>
</tr>
<tr id="row066512346381"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p85461925164216"><a name="p85461925164216"></a><a name="p85461925164216"></a>删除指定Namespace下的所有Endpoint对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p754632513428"><a name="p754632513428"></a><a name="p754632513428"></a>deleteEndpointsByNamespace</p>
</td>
</tr>
<tr id="row39231134123816"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p18547725194219"><a name="p18547725194219"></a><a name="p18547725194219"></a>替换指定Namespace下的Endpoint对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p17546142554212"><a name="p17546142554212"></a><a name="p17546142554212"></a>replaceEndpoint</p>
</td>
</tr>
<tr id="row11185193513816"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p165479257422"><a name="p165479257422"></a><a name="p165479257422"></a>更新指定Namespace下的Endpoint对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p654718257426"><a name="p654718257426"></a><a name="p654718257426"></a>updateEndpoint</p>
</td>
</tr>
<tr id="row16450535103817"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1754712564219"><a name="p1754712564219"></a><a name="p1754712564219"></a>创建一个Deployment对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p19547525164219"><a name="p19547525164219"></a><a name="p19547525164219"></a>createDeployment</p>
</td>
</tr>
<tr id="row107342035123814"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p354710251425"><a name="p354710251425"></a><a name="p354710251425"></a>删除一个Deployment对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1354782524214"><a name="p1354782524214"></a><a name="p1354782524214"></a>deleteDeployment</p>
</td>
</tr>
<tr id="row189915354383"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p85471525184210"><a name="p85471525184210"></a><a name="p85471525184210"></a>删除指定Namespace下的所有Deployment对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p35471325154215"><a name="p35471325154215"></a><a name="p35471325154215"></a>deleteDeploymentsByNamespace</p>
</td>
</tr>
<tr id="row11247123618381"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p55478251422"><a name="p55478251422"></a><a name="p55478251422"></a>替换指定Namespace下的Deployment对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p205474255427"><a name="p205474255427"></a><a name="p205474255427"></a>replaceDeployment</p>
</td>
</tr>
<tr id="row13528183623818"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p10547102534213"><a name="p10547102534213"></a><a name="p10547102534213"></a>更新指定Namespace下的Deployment对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p14547192517426"><a name="p14547192517426"></a><a name="p14547192517426"></a>updateDeployment</p>
</td>
</tr>
<tr id="row138443361388"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p354762511422"><a name="p354762511422"></a><a name="p354762511422"></a>创建一个Statefulset对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p85479254427"><a name="p85479254427"></a><a name="p85479254427"></a>createStatefulset</p>
</td>
</tr>
<tr id="row11196173713381"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p17547525104214"><a name="p17547525104214"></a><a name="p17547525104214"></a>删除一个Statefulset对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p5547192574218"><a name="p5547192574218"></a><a name="p5547192574218"></a>deleteStatefulset</p>
</td>
</tr>
<tr id="row1547923713817"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p18547425144219"><a name="p18547425144219"></a><a name="p18547425144219"></a>删除指定Namespace下的所有Statefulset对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p9547132518423"><a name="p9547132518423"></a><a name="p9547132518423"></a>deleteStatefulsetsByNamespace</p>
</td>
</tr>
<tr id="row1806137163818"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p6548172584212"><a name="p6548172584212"></a><a name="p6548172584212"></a>替换指定Namespace下的Statefulset对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p95486253428"><a name="p95486253428"></a><a name="p95486253428"></a>replaceStatefulset</p>
</td>
</tr>
<tr id="row15143838133818"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p14548325154214"><a name="p14548325154214"></a><a name="p14548325154214"></a>更新指定Namespace下的Statefulset对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p654832510422"><a name="p654832510422"></a><a name="p654832510422"></a>updateStatefulset</p>
</td>
</tr>
<tr id="row14502038193811"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p3548225174218"><a name="p3548225174218"></a><a name="p3548225174218"></a>创建一个Job对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p7548825194211"><a name="p7548825194211"></a><a name="p7548825194211"></a>createJob</p>
</td>
</tr>
<tr id="row1980053883816"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p16548192574214"><a name="p16548192574214"></a><a name="p16548192574214"></a>删除一个Job对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1854818252428"><a name="p1854818252428"></a><a name="p1854818252428"></a>deleteJob</p>
</td>
</tr>
<tr id="row11151173923816"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p15548112564213"><a name="p15548112564213"></a><a name="p15548112564213"></a>删除指定Namespace下的所有Job对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p195481825194215"><a name="p195481825194215"></a><a name="p195481825194215"></a>deleteJobsByNamespace</p>
</td>
</tr>
<tr id="row1950073943815"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p115487258426"><a name="p115487258426"></a><a name="p115487258426"></a>替换指定Namespace下的某个Job对象的状态</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p454862554218"><a name="p454862554218"></a><a name="p454862554218"></a>replaceJob</p>
</td>
</tr>
<tr id="row118871714163811"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1548112534212"><a name="p1548112534212"></a><a name="p1548112534212"></a>更新指定Namespace下的某个Job对象的状态</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p165489257424"><a name="p165489257424"></a><a name="p165489257424"></a>updateJob</p>
</td>
</tr>
<tr id="row11704159385"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p354817252424"><a name="p354817252424"></a><a name="p354817252424"></a>创建一个Cronjob对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p55487252421"><a name="p55487252421"></a><a name="p55487252421"></a>createCronjob</p>
</td>
</tr>
<tr id="row91481731204115"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p155489258421"><a name="p155489258421"></a><a name="p155489258421"></a>删除一个Cronjob对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1548625174216"><a name="p1548625174216"></a><a name="p1548625174216"></a>deleteCronjob</p>
</td>
</tr>
<tr id="row191501231144119"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p175481925194212"><a name="p175481925194212"></a><a name="p175481925194212"></a>删除指定Namespace下的所有Cronjob对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p7548122518429"><a name="p7548122518429"></a><a name="p7548122518429"></a>deleteCronjobsByNamespace</p>
</td>
</tr>
<tr id="row91501313418"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p25481525104218"><a name="p25481525104218"></a><a name="p25481525104218"></a>替换指定Namespace下的某个Cronjob对象的状态</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1654852516423"><a name="p1654852516423"></a><a name="p1654852516423"></a>replaceCronjob</p>
</td>
</tr>
<tr id="row21502031194113"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p20548112544212"><a name="p20548112544212"></a><a name="p20548112544212"></a>更新指定Namespace下的某个Cronjob对象的状态</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1548125154213"><a name="p1548125154213"></a><a name="p1548125154213"></a>updateCronjob</p>
</td>
</tr>
<tr id="row10150131164119"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p15549172517428"><a name="p15549172517428"></a><a name="p15549172517428"></a>创建一个Ingress对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p254922518425"><a name="p254922518425"></a><a name="p254922518425"></a>createIngress</p>
</td>
</tr>
<tr id="row14151183184119"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p754972574215"><a name="p754972574215"></a><a name="p754972574215"></a>删除一个Ingress对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p7549162519427"><a name="p7549162519427"></a><a name="p7549162519427"></a>deleteIngress</p>
</td>
</tr>
<tr id="row18151103194115"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1754962544212"><a name="p1754962544212"></a><a name="p1754962544212"></a>删除指定Namespace下的所有Ingress对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p4549825144217"><a name="p4549825144217"></a><a name="p4549825144217"></a>deleteIngressesByNamespace</p>
</td>
</tr>
<tr id="row71511731184113"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p13549525104210"><a name="p13549525104210"></a><a name="p13549525104210"></a>替换指定Namespace下的特定Ingress对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1554916251424"><a name="p1554916251424"></a><a name="p1554916251424"></a>replaceIngress</p>
</td>
</tr>
<tr id="row71516312419"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p154920253423"><a name="p154920253423"></a><a name="p154920253423"></a>更新指定Namespace下的某个Ingress对象的状态</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p115498257425"><a name="p115498257425"></a><a name="p115498257425"></a>updateIngress</p>
</td>
</tr>
<tr id="row21513312411"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1154932534212"><a name="p1154932534212"></a><a name="p1154932534212"></a>创建一个Namespace</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1354972504215"><a name="p1354972504215"></a><a name="p1354972504215"></a>createNamespace</p>
</td>
</tr>
<tr id="row515213174111"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p95491225154210"><a name="p95491225154210"></a><a name="p95491225154210"></a>删除一个Namespace</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p16549172518424"><a name="p16549172518424"></a><a name="p16549172518424"></a>deleteNamespace</p>
</td>
</tr>
<tr id="row8152331204111"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p16549122594213"><a name="p16549122594213"></a><a name="p16549122594213"></a>创建一个Pod</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p9549172574213"><a name="p9549172574213"></a><a name="p9549172574213"></a>createPod</p>
</td>
</tr>
<tr id="row015213111419"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p95491525154210"><a name="p95491525154210"></a><a name="p95491525154210"></a>更新指定Pod</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p25491825184210"><a name="p25491825184210"></a><a name="p25491825184210"></a>updatePod</p>
</td>
</tr>
<tr id="row1915233114413"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1554916256421"><a name="p1554916256421"></a><a name="p1554916256421"></a>替换指定Pod</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p654982594217"><a name="p654982594217"></a><a name="p654982594217"></a>replacePod</p>
</td>
</tr>
<tr id="row1215223116410"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p9549192574218"><a name="p9549192574218"></a><a name="p9549192574218"></a>删除一个Pod</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p55491257427"><a name="p55491257427"></a><a name="p55491257427"></a>deletePod</p>
</td>
</tr>
<tr id="row6152163110410"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p954932514218"><a name="p954932514218"></a><a name="p954932514218"></a>删除Namespace下所有的Pod</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p554911250426"><a name="p554911250426"></a><a name="p554911250426"></a>deletePodsByNamespace</p>
</td>
</tr>
<tr id="row191534313411"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p155501025114219"><a name="p155501025114219"></a><a name="p155501025114219"></a>删除指定Event</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p11550112574214"><a name="p11550112574214"></a><a name="p11550112574214"></a>deleteEvent</p>
</td>
</tr>
<tr id="row5153153154110"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1255092518424"><a name="p1255092518424"></a><a name="p1255092518424"></a>创建一个Configmap</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1055072554210"><a name="p1055072554210"></a><a name="p1055072554210"></a>createConfigmap</p>
</td>
</tr>
<tr id="row101536313419"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p20550102515420"><a name="p20550102515420"></a><a name="p20550102515420"></a>更新指定Configmap</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p115501225164214"><a name="p115501225164214"></a><a name="p115501225164214"></a>updateConfigmap</p>
</td>
</tr>
<tr id="row1315343111415"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p17550182534217"><a name="p17550182534217"></a><a name="p17550182534217"></a>替换指定Configmap</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1555012254428"><a name="p1555012254428"></a><a name="p1555012254428"></a>replaceConfigmap</p>
</td>
</tr>
<tr id="row5153103124111"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p35503255423"><a name="p35503255423"></a><a name="p35503255423"></a>删除一个Configmap</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p175501725134218"><a name="p175501725134218"></a><a name="p175501725134218"></a>deleteConfigmap</p>
</td>
</tr>
<tr id="row315323144110"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p455015257424"><a name="p455015257424"></a><a name="p455015257424"></a>删除指定Namespace下所有的Configmap</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1555072512420"><a name="p1555072512420"></a><a name="p1555072512420"></a>deleteConfigmapsByNamespace</p>
</td>
</tr>
<tr id="row15153133134113"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p11550142554213"><a name="p11550142554213"></a><a name="p11550142554213"></a>创建一个Secret</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p155012512424"><a name="p155012512424"></a><a name="p155012512424"></a>createSecret</p>
</td>
</tr>
<tr id="row191531431174111"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p8550925114216"><a name="p8550925114216"></a><a name="p8550925114216"></a>更新指定Secret</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1555011258426"><a name="p1555011258426"></a><a name="p1555011258426"></a>updateSecret</p>
</td>
</tr>
<tr id="row115418318416"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p4550172554216"><a name="p4550172554216"></a><a name="p4550172554216"></a>替换指定Secret</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p755022584214"><a name="p755022584214"></a><a name="p755022584214"></a>replaceSecret</p>
</td>
</tr>
<tr id="row6236161516385"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p2055022513425"><a name="p2055022513425"></a><a name="p2055022513425"></a>删除指定Secret</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1455072520423"><a name="p1455072520423"></a><a name="p1455072520423"></a>deleteSecret</p>
</td>
</tr>
<tr id="row64003156383"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p8550122520425"><a name="p8550122520425"></a><a name="p8550122520425"></a>删除指定Namespace下所有的Secret</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p45503257429"><a name="p45503257429"></a><a name="p45503257429"></a>deleteSecretsByNamespace</p>
</td>
</tr>
<tr id="row976691573816"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1455182515422"><a name="p1455182515422"></a><a name="p1455182515422"></a>删除指定Network</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p0551142574211"><a name="p0551142574211"></a><a name="p0551142574211"></a>deleteNetwork</p>
</td>
</tr>
<tr id="row1093116152383"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p16551132514422"><a name="p16551132514422"></a><a name="p16551132514422"></a>创建一个Network</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p15512257423"><a name="p15512257423"></a><a name="p15512257423"></a>createNetwork</p>
</td>
</tr>
<tr id="row8952162389"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p19551125124218"><a name="p19551125124218"></a><a name="p19551125124218"></a>删除指定Namespace下所有的Network</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1555122514423"><a name="p1555122514423"></a><a name="p1555122514423"></a>deleteNetworksByNamespace</p>
</td>
</tr>
<tr id="row627551663812"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p0551025104217"><a name="p0551025104217"></a><a name="p0551025104217"></a>更新指定Network</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p5551162518422"><a name="p5551162518422"></a><a name="p5551162518422"></a>updateNetwork</p>
</td>
</tr>
<tr id="row24561416203810"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p155182524220"><a name="p155182524220"></a><a name="p155182524220"></a>替换指定Network</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p155511925144219"><a name="p155511925144219"></a><a name="p155511925144219"></a>replaceNetwork</p>
</td>
</tr>
<tr id="row86221816163818"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1155110254422"><a name="p1155110254422"></a><a name="p1155110254422"></a>创建network-attachment-definition</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1355119259427"><a name="p1355119259427"></a><a name="p1355119259427"></a>createNetworkAttachmentDefinition</p>
</td>
</tr>
<tr id="row1779151617386"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p75517256423"><a name="p75517256423"></a><a name="p75517256423"></a>删除指定Namespace下所有的network-attachment-definitions</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p655162554219"><a name="p655162554219"></a><a name="p655162554219"></a>deleteNetworkAttachmentDefinitionsByNamespace</p>
</td>
</tr>
<tr id="row1995721663817"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p125521625164210"><a name="p125521625164210"></a><a name="p125521625164210"></a>删除指定network-attachment-definition</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p255292511429"><a name="p255292511429"></a><a name="p255292511429"></a>deleteNetworkAttachmentDefinition</p>
</td>
</tr>
<tr id="row1412191773811"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p135521525174214"><a name="p135521525174214"></a><a name="p135521525174214"></a>创建PV</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p6552152512422"><a name="p6552152512422"></a><a name="p6552152512422"></a>createPersistentvolume</p>
</td>
</tr>
<tr id="row7664121717383"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p455242524217"><a name="p455242524217"></a><a name="p455242524217"></a>删除指定Namespace下所有的PV</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1855213252421"><a name="p1855213252421"></a><a name="p1855213252421"></a>deletePersistentvolumesByNamespace</p>
</td>
</tr>
<tr id="row1079231717386"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p11552192514429"><a name="p11552192514429"></a><a name="p11552192514429"></a>替换指定PV</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p555292524220"><a name="p555292524220"></a><a name="p555292524220"></a>replacePersistentvolume</p>
</td>
</tr>
<tr id="row69931317173813"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1552182564214"><a name="p1552182564214"></a><a name="p1552182564214"></a>更新指定PV</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p155521825144212"><a name="p155521825144212"></a><a name="p155521825144212"></a>updatePersistentvolume</p>
</td>
</tr>
<tr id="row18139518193810"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1255292514217"><a name="p1255292514217"></a><a name="p1255292514217"></a>删除指定PV</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1055282584211"><a name="p1055282584211"></a><a name="p1055282584211"></a>deletePersistentvolume</p>
</td>
</tr>
<tr id="row20277111853814"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p115521925134216"><a name="p115521925134216"></a><a name="p115521925134216"></a>创建PVC</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p10552122513424"><a name="p10552122513424"></a><a name="p10552122513424"></a>createPersistentvolumeclaim</p>
</td>
</tr>
<tr id="row54522018183815"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1055217257425"><a name="p1055217257425"></a><a name="p1055217257425"></a>导入已有PVC</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p16552112564214"><a name="p16552112564214"></a><a name="p16552112564214"></a>createPersistentvolumeclaimByStorageInfo</p>
</td>
</tr>
<tr id="row360941815385"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p195531725124217"><a name="p195531725124217"></a><a name="p195531725124217"></a>删除指定Namespace下所有的PVC</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p155531725104217"><a name="p155531725104217"></a><a name="p155531725104217"></a>deletePersistentvolumeclaimsByNamespace</p>
</td>
</tr>
<tr id="row16763111843812"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p2553162564218"><a name="p2553162564218"></a><a name="p2553162564218"></a>替换指定PVC</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1255310259422"><a name="p1255310259422"></a><a name="p1255310259422"></a>replacePersistentvolumeclaim</p>
</td>
</tr>
<tr id="row1992131833810"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p455362511425"><a name="p455362511425"></a><a name="p455362511425"></a>更新指定PVC</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p185531425124216"><a name="p185531425124216"></a><a name="p185531425124216"></a>updatePersistentvolumeclaim</p>
</td>
</tr>
<tr id="row1892121915386"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1055322544218"><a name="p1055322544218"></a><a name="p1055322544218"></a>删除指定PVC</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p155319258420"><a name="p155319258420"></a><a name="p155319258420"></a>deletePersistentvolumeclaim</p>
</td>
</tr>
<tr id="row12598191387"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p11553102517421"><a name="p11553102517421"></a><a name="p11553102517421"></a>购买一个套餐包</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p195531925154212"><a name="p195531925154212"></a><a name="p195531925154212"></a>createPackageproduct</p>
</td>
</tr>
<tr id="row245716197383"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p15553225114214"><a name="p15553225114214"></a><a name="p15553225114214"></a>购买活动套餐包</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1655302517425"><a name="p1655302517425"></a><a name="p1655302517425"></a>createActiveproduct</p>
</td>
</tr>
<tr id="row1464391963816"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p555382534210"><a name="p555382534210"></a><a name="p555382534210"></a>创建Kubeflow job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p85531725194217"><a name="p85531725194217"></a><a name="p85531725194217"></a>createKubeflowJob</p>
</td>
</tr>
<tr id="row2840101919381"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p2554102574216"><a name="p2554102574216"></a><a name="p2554102574216"></a>删除指定Namespace下所有的Kubeflow job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p17553112518429"><a name="p17553112518429"></a><a name="p17553112518429"></a>deleteKubeflowJobsByNamespace</p>
</td>
</tr>
<tr id="row644102018385"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p14554152516426"><a name="p14554152516426"></a><a name="p14554152516426"></a>替换指定Kubeflow job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1255462516421"><a name="p1255462516421"></a><a name="p1255462516421"></a>replaceKubeflowJob</p>
</td>
</tr>
<tr id="row1324482019385"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p165545255428"><a name="p165545255428"></a><a name="p165545255428"></a>更新指定Kubeflow job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p4554425134218"><a name="p4554425134218"></a><a name="p4554425134218"></a>updateKubeflowJob</p>
</td>
</tr>
<tr id="row1244119202386"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p13554325184211"><a name="p13554325184211"></a><a name="p13554325184211"></a>删除指定Kubeflow job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p15554122514428"><a name="p15554122514428"></a><a name="p15554122514428"></a>deleteKubeflowJob</p>
</td>
</tr>
<tr id="row564613201384"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p555517252423"><a name="p555517252423"></a><a name="p555517252423"></a>创建Volcano job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p055582514424"><a name="p055582514424"></a><a name="p055582514424"></a>createVolcanoJob</p>
</td>
</tr>
<tr id="row0883172013813"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1755512574219"><a name="p1755512574219"></a><a name="p1755512574219"></a>删除指定Namespace下所有的Volcano job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p655562519428"><a name="p655562519428"></a><a name="p655562519428"></a>deleteVolcanoJobsByNamespace</p>
</td>
</tr>
<tr id="row10923218388"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p20555122544210"><a name="p20555122544210"></a><a name="p20555122544210"></a>替换指定Volcano job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p95551258426"><a name="p95551258426"></a><a name="p95551258426"></a>replaceVolcanoJob</p>
</td>
</tr>
<tr id="row16310621113819"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p15555192534217"><a name="p15555192534217"></a><a name="p15555192534217"></a>更新指定Volcano job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p155510254423"><a name="p155510254423"></a><a name="p155510254423"></a>updateVolcanoJob</p>
</td>
</tr>
<tr id="row1540921183816"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p4555152524213"><a name="p4555152524213"></a><a name="p4555152524213"></a>删除指定Volcano job</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1755532517424"><a name="p1755532517424"></a><a name="p1755532517424"></a>deleteVolcanoJob</p>
</td>
</tr>
<tr id="row912313616599"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p855616250427"><a name="p855616250427"></a><a name="p855616250427"></a>创建Agency</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p4556202564216"><a name="p4556202564216"></a><a name="p4556202564216"></a>createAgency</p>
</td>
</tr>
<tr id="row161231136185917"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1755622511421"><a name="p1755622511421"></a><a name="p1755622511421"></a>更新配额</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p35561625134215"><a name="p35561625134215"></a><a name="p35561625134215"></a>modifyQuota</p>
</td>
</tr>
<tr id="row13263193712499"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p626313734916"><a name="p626313734916"></a><a name="p626313734916"></a>创建一个imagecache对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1926314376494"><a name="p1926314376494"></a><a name="p1926314376494"></a>createImagecache</p>
</td>
</tr>
<tr id="row112901635204914"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p829118356493"><a name="p829118356493"></a><a name="p829118356493"></a>删除一个imagecache对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p17291635124917"><a name="p17291635124917"></a><a name="p17291635124917"></a>deleteImagecache</p>
</td>
</tr>
<tr id="row103171332496"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p15317193384916"><a name="p15317193384916"></a><a name="p15317193384916"></a>替换指定的imagecache对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p18317123364913"><a name="p18317123364913"></a><a name="p18317123364913"></a>replaceImagecache</p>
</td>
</tr>
<tr id="row17438153120491"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p19439173119493"><a name="p19439173119493"></a><a name="p19439173119493"></a>更新指定的imagecache对象</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p20439153115498"><a name="p20439153115498"></a><a name="p20439153115498"></a>updateImagecache</p>
</td>
</tr>
<tr id="row1712319575414"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p16556102504212"><a name="p16556102504212"></a><a name="p16556102504212"></a>上传模板</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p95565259427"><a name="p95565259427"></a><a name="p95565259427"></a>createChart</p>
</td>
</tr>
<tr id="row11124195724120"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p17556122554219"><a name="p17556122554219"></a><a name="p17556122554219"></a>更新指定模板</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p85561251428"><a name="p85561251428"></a><a name="p85561251428"></a>updateChart</p>
</td>
</tr>
<tr id="row61245570415"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p85561425204217"><a name="p85561425204217"></a><a name="p85561425204217"></a>删除指定模板</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p1955642534214"><a name="p1955642534214"></a><a name="p1955642534214"></a>deleteChart</p>
</td>
</tr>
<tr id="row9124657144114"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p14556182534218"><a name="p14556182534218"></a><a name="p14556182534218"></a>上传插件</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p18556525134210"><a name="p18556525134210"></a><a name="p18556525134210"></a>createAddon</p>
</td>
</tr>
<tr id="row1912414578413"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p16557625144216"><a name="p16557625144216"></a><a name="p16557625144216"></a>更新指定插件</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p14557725144219"><a name="p14557725144219"></a><a name="p14557725144219"></a>updateAddon</p>
</td>
</tr>
<tr id="row51241957164116"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1255792524219"><a name="p1255792524219"></a><a name="p1255792524219"></a>删除指定插件</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p165571325154212"><a name="p165571325154212"></a><a name="p165571325154212"></a>deleteAddon</p>
</td>
</tr>
<tr id="row1043010168426"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p655762515427"><a name="p655762515427"></a><a name="p655762515427"></a>创建模板实例</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p135571025164215"><a name="p135571025164215"></a><a name="p135571025164215"></a>createRelease</p>
</td>
</tr>
<tr id="row143111664212"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p455752515428"><a name="p455752515428"></a><a name="p455752515428"></a>更新模板实例</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p19557122504219"><a name="p19557122504219"></a><a name="p19557122504219"></a>updateRelease</p>
</td>
</tr>
<tr id="row5431161616429"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p255712252428"><a name="p255712252428"></a><a name="p255712252428"></a>删除模板实例</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p9557122524219"><a name="p9557122524219"></a><a name="p9557122524219"></a>deleteRelease</p>
</td>
</tr>
<tr id="row2431716134216"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p1955718254424"><a name="p1955718254424"></a><a name="p1955718254424"></a>创建插件实例</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p955712594211"><a name="p955712594211"></a><a name="p955712594211"></a>createAddonInstance</p>
</td>
</tr>
<tr id="row174311916174217"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p105571025154220"><a name="p105571025154220"></a><a name="p105571025154220"></a>更新插件实例</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p20557182515428"><a name="p20557182515428"></a><a name="p20557182515428"></a>updateAddonInstance</p>
</td>
</tr>
<tr id="row141241957104115"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p2055872511422"><a name="p2055872511422"></a><a name="p2055872511422"></a>删除插件实例</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p15558102515429"><a name="p15558102515429"></a><a name="p15558102515429"></a>deleteAddonInstance</p>
</td>
</tr>
<tr id="row19783947115012"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p97831547195016"><a name="p97831547195016"></a><a name="p97831547195016"></a>创建插件readme</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p078334755014"><a name="p078334755014"></a><a name="p078334755014"></a>createAddonReadme</p>
</td>
</tr>
<tr id="row177291053175010"><td class="cellrowborder" valign="top" width="51.35999999999999%" headers="mcps1.2.3.1.1 "><p id="p573075315013"><a name="p573075315013"></a><a name="p573075315013"></a>删除插件Readme</p>
</td>
<td class="cellrowborder" valign="top" width="48.64%" headers="mcps1.2.3.1.2 "><p id="p13730105305010"><a name="p13730105305010"></a><a name="p13730105305010"></a>deleteAddonReadme</p>
</td>
</tr>
</tbody>
</table>

