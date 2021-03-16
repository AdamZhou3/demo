#CUSP

## Question

-   *How has cycling-relevant street infrastructure changed in London and what might this suggest for future support for cycling in the city in future?** 
    
-   1.与自行车相关的街道基础设施在伦敦发生了怎样的变化，这对于将来对城市自行车的支持有何建议？ （地图上的可视化）
    
-   Can we create a map that incorporates all relevant cycling infrastructure at present? 

    -   2.我们是否可以创建包含当前所有相关自行车基础设施的地图？（可视化）官方提供：https://cycling.data.tfl.gov.uk/https://cycling.data.tfl.gov.uk/CyclingInfrastructure/data/points/cycle_parking.json

-   What is the potential for adding a network of secure bike (and e-bike) parking in London that can be accessed on-demand? 

    -   3.在伦敦增加可以按需访问的安全自行车（和电动自行车）停车网络的潜力是什么？()
    -   需求预测 贝叶斯不确定性预测

-   You may want to identify and map potential popular locations in London where cyclists, based on origin/destination and other data (e.g. retail and leisure spend, footfall, cycling count, Strava etc) may want to stop and secure their bike for 30 mins to 3 hours. With cycle theft increasing year-on-year, there is a case for more secure urban parking for bikes. 

    -   您可能想根据来源/目的地和其他数据（例如，零售和休闲支出，人流量，自行车计数，Strava等），确定并绘制伦敦可能流行的地点，骑自行车的人可能想要在30分钟内停车并保护自己的自行车， 3小时。
    
*The link between bike sharing and subway use during the COVID-19 pandemic: the case-study of New York's Citi Bike*
    
-   This is distinct to storage at home or in primary places of work (typically more than 3 hours) but instead intermediate journeys that cyclists would like to make on their bikes – e.g. stopping to meet friends for food or a drink, calling in at the gym, stopping to pick up some shopping etc. Research by CUSP London partner Active Things indicates that risk of theft puts off many cyclists making these intermediate journeys and has a negative impact on cycle use (i.e. they don’t use the electric bike if they plan to go to meet friends after work). 

    -   随着自行车盗窃逐年增加，有必要为自行车提供更安全的城市停车位。这与在家中或主要工作地点（通常超过3个小时）的存放方式不同，而骑车者想在自行车上进行的中间行程（例如，停下来见朋友吃喝玩乐，在健身房打电话，停下来买东西等等。
        CUSP伦敦合作伙伴Active Things的研究表明，盗窃的风险使许多骑自行车的人无法进行这些中间旅程，并且对自行车的使用产生负面影响（即，如果他们打算下班后与朋友见面，他们将不使用电动自行车）

-   Where should the first 100, 500 and 1000 lockers be installed to best cater to these intermediate journeys? 

    -   4.应该在哪里安装前100个，500个和1000个储物柜，以最好地适应这些中间旅程？ 

-   What kind of profile of use could be imagined in terms of daily usage patterns? --Do the current deployment on street and secure bike racks match the need for secure parking? 

    -   5.根据日常使用模式，可以想象出哪种使用情况？
    -   6.当前在街道和安全自行车架上的部署是否符合安全停车的需求?

## Data

*   ‘requested locations’ is a stronger signal, those are locations where people have requested a secure bike parking location
*   ‘searches’ is a weaker signal, those are locations where people searched for on activethings.app or** [**app.runfriendly.com**](http://app.runfriendly.com/) **(as stated in one of the columns).** 
*   Most columns will speak for themselves, but more explanation could be provided whenever needed.
*   **基本思路**政策背景：[Encouraging cycling and walking - Transport for London (tfl.gov.uk)](https://tfl.gov.uk/corporate/about-tfl/how-we-work/planning-for-the-future/encouraging-cycling-and-walking#:~:text=The overarching goal of the,the London-wide cycle network) （来自Data Dive Programme Mar 2021 Final.pdf第三页）*(**Transport for London | Every Journey Matters (2021). Encouraging cycling and walking. [online] Transport for London. Available at: https://tfl.gov.uk/corporate/about-tfl/how-we-work/planning-for-the-future/encouraging-cycling-and-walking#:~:text=The%20overarching%20goal%20of%20the,the%20London-wide%20cycle%20network [Accessed 16 Mar. 2021].*)
*   合作公司背景：**RunFriendly** build digital tools to make it friendlier to ride bikes, run and do active things outdoors. As seen in Men’s Health as a ‘Top App to Change Your Life in 2020’ and as an ‘Eco Hero’ by Runner’s World. Our customers include Nike and HSBC. RunFriendly is a solution from Active Things. We are building the digital infrastructure & network to **make it friendlier to ride bikes, run & walk in cities.** Right now, we’re trying to help us do Active Things during the coronavirus. This includes a volunteer service whereby we help runners (and bike riders) **‘run-an-errand’** for those most at-risk of COVID-19. （来自Data Dive Programme Mar 2021 Final.pdf第四页）



## **思路1（完全按照topic的流程）**
问题1 & 2，对伦敦自行车基建设施的可视化，整体的展现变化和分布。
问题3：-首先，说明自行车盗窃的背景；-其次，引入Runfriendly的搜索记录数据，展示搜索的热门点的分布，观察和已有基建设施分布的差距。
-（*如果感到时间充裕，可以尝试使用tfl的共享单车使用记录数据来观察单车使用频率的分布，但是估计这个要花不少时间*）
-阐明建设安全的自行车停放网络的潜力，即locker设置的必要性。
由此引出问题4，在哪装。问题4：

**Methdology**![img](https://lh5.googleusercontent.com/p4cSKhfDijbm_enSm5r5tY8fitgL-rTZw5EP62WUQ24gZ_FxBWn8o0H-YHURUCSDrF95micxfXM-Agy2RDBO_e_pmVCEn4B4deh3aig4bcGhVydjKNC674lvLe8UbUFh1p1Si-dT)(From I2P Jon Reades Assessment#2 Feedback)
**Q&A**确认dataset的使用方法。Request.csv的获取方法？
停一整天的
清理不正常的搜索记录（比如5min内多次搜索同一地点），有没有用户信息帮助我们筛选？
searches.csv What does “type” means?How can I do with “columns”?![img](https://lh3.googleusercontent.com/Bn3vAIrotbyvY70mM5-yLwgpctlCEzGNjZrlh8s-eT73yOJp_s1mDglnXjnd88-J3ebesgnKM9HDgA_SGFjrU62If-MB-6muMui6c3wSGS2mINpZGDqnMF9egpoRSv2A7rjNP84r)
request.csv
In duration column, there are some request like “multiple days”, does that means there are some users want to put bike in the secure box for many days?
Besides, can we have a dictionary about the attributes in the csv files, for we are not sure about the meaning of them.

## Day2 **关于第三问：交通网络的潜力**

https://www.sciencedirect.com/science/article/pii/S2590198220300774

概要：疫情下公共交通系统下降，但地铁下降甚于自行车，且可能有部分需求从地铁转移到自行车如何比对疫情和非疫情期间的自行车使用量变化？

https://cycling.data.tfl.gov.uk/的自行车租赁数据（搜索“usage-stats/”获取月份租赁数据，包括起始站点和结束站点，可使用疫情前和疫情期间的某个月份进行比对，比如2019年11月和2020年11月，后者为疫情相当严重的一个月）。假设：自行车使用量减少，但减少量有限。对自行车租赁数据进行分析，发现租赁者的行为模式变化，说明其使用目的或人群发生了变化。（比如之前使用时间中位数是15min，路线长是大概4km；疫情之后是30min和10km，可以说明有更多的上班族骑着它上班了，或许通过结束站点分析目的地也会有帮助）

对比：地铁数据的变化[ https://data.london.gov.uk/dataset/public-transport-journeys-type-transport](https://data.london.gov.uk/dataset/public-transport-journeys-type-transport) （只有个使用人数的话不太容易做地图） 假设：自行车受到的冲击小于地铁，自行车对应对后疫情时代有帮助。（英国真的后疫情了吗）结论：在新冠流行期间，自行车收到冲击较小且发生了用户的转移。（劣势或许是长时间骑行需要休息，以及可能存在的结束骑行后需要重新打理仪容的问题，幸运的是咱们的Runfriendly正好是做这个的）其他自行车网络的潜力：环保，价格低廉，避免疫情。这些可以参考那篇论文的结论部分。其他思路：找一下比如伦敦某大型卖场的销售数据，分析其几个月来自行车销售情况，是否有更多的人想要自行车了？ps. 还是刚才的自行车数据，可以筛选“短期骑行”（30min-3hrs），分析其路线，画在地图上观察其特征比如从某站前往某站。感觉这个和我们有门网络分析课上的东西比较像，或许可以先做个简单的图或者表格找一下哪几个站之间比较“热门”，再结合交通网络图对两点间路线进行分析？

**另：**[**https://cycling.data.tfl.gov.uk/**](https://cycling.data.tfl.gov.uk/) **文档简单整理**

CycleCounters**：我怀疑是车子的销售/登记数据，按地区和日期分类，里边有很多车子的数据比如长宽高轴距？之类的。**

CycleCountsProgramme**：某个按区域统计自行车数量的项目的数据。按站点统计的某天某几个小时内有多少自行车被站点观测到。**

CycleParking**：一个来自2015年的压缩文件包，看格式可能是MapInfo的文件，没用过所以不知道这里边有什么，可能是停车场区域之类的。（The file "cycle-parking-map-info.zip" is used to load the cycle parking points in the api.These are then displayed on the map pages.The zip file should be updated when we want to add new cycle parking points.）**CycleRoutes**：一个JSON文件，应该是自行车路线？**

CyclingInfrastructure**：一系列JSON文件，目测是描述基础设施地理位置的**

CyclingInfrastructure**/**documentation**/：包含一份图片免责声明，一份对各种公共设施的详细定义（应该是吧），还有一份应该是那些JSON的字典，告诉你每个字段的意思（[cid_database_schema.xlsx](https://cycling.data.tfl.gov.uk/CyclingInfrastructure/documentation/cid_database_schema.xlsx)）**usage-stats**：从2012年起的每月租赁数据，包括自行车租赁起始点和归还点，以及租赁起止时间和持续秒数。



## 资料

London Cycling Design Standards (LCDS) https://tfl.gov.uk/corporate/publications-and-reports/streets-toolkit

https://cycling.data.tfl.gov.uk/



https://tfl.gov.uk/corporate/publications-and-reports/cycling

https://docs.google.com/document/d/1K8AZMt8LOapOn1DIzzurzIWgOptX_fg_34R3gk3HBRc/edit#



http://planning.data.tfl.gov.uk/

## CID

https://blog.tfl.gov.uk/2019/08/13/data-drop-cycling-infrastructure-database/

https://data.london.gov.uk/dataset/cycling-infrastructure-database

-   自行车道和赛道-包括它们是隔离的还是涂漆的车道
-   自行车停车，包括停车的类型和容量

-   Cycle lanes and tracks – including whether they are segregated or painted lanes
-   Cycle parking, including the type and capacity of parking

-   信号交叉口循环
-   受限路线–允许通过周期但限制车辆通行的模态过滤器和交通闸
-   交通平静，包括大伦敦所有减速带的位置
-   先进的停车线–交叉口处的供人骑行的箱子
-   信号–交界处的早期释放信号
-   标牌–签署的自行车路线和其他寻路
-   限制点–骑自行车的人必须下车的路径，这些路径可以穿过公园和其他可以或不能在其上骑行的绿色空间



*   现有数据
    *   Parking数据 属性包括是否lock, 每个parking的容积
    *   路网数据
    *   路网节点数据 （反应道路密度）
    *   自行车道数据 lane
    *   POI数据
    *   基础数据
        *   LSOA
        *   Boroughs

*   自行车道路的密度 与道路长度的对比 lane
    *   密度对比与长度对比
    *   分区统计

-   parking的容积分区统计
    -   根据parking的属性统计每个lsoa内的总数
    -   parking 多大比例是lock的  
    -   路网节点与parking的比例
        -   反映设施完善程度
-   潜力评估 potential for  <u>secure bike (and e-bike) parking</u> that can be accessed on-demand? 
    -   那些地区比较缺乏lock的parking
    -   多大比例的 缺乏locking    直接引用报告
        -   8.2 million short journeys by car that could potentially be cycled 
        -   参考 P12 引用数据 Analysis of Cycling Potential http://content.tfl.gov.uk/analysis-of-cycling-potential.pdf 
-   需求预测 
    -   选一个小区域做
    -   API计算流量分布 流量图
    -   

