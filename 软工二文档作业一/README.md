#用例文档
##1.引言
    本报告详细地部分完成对影院管理系统的概要设计，
    达到指导详细设计和开发的目的，同时实现和用户的沟通。
    本报告面向开发人员，及最终用户而编写，是了解系统的导航。
##2.用例图
[use cases diagram][1]
[1]:https://github.com/jiangxizhanzhi/resource/blob/master/usecaseDiagram2.PNG
##3.用例列表
- 热映电影信息调整
- 即将上映电影信息调整
- 电影信息查询
##4.详细用例描述
###4.1上架电影信息调整
- 用例编号：01
- 名称：上架电影信息调整
- 创建者：happy_SE
- 最后一次更新者：happy_SE
- 更新日期：2019/3/19
- 参与者：影院 目标是上架电影，开展电影宣传 观众 目标是标记想看的电影
- 触发条件：有新影片上映
- 前置条件：获得新影片发行商的宣传许可
- 后置条件：存储影片名称，宣传片，简介，图片剧照，演职人员，上映时间，影片类型
- 正常流程：  
    1. 影院开始新一次上架电影  
    2. 影院向系统输入影片名称宣传片，简介，图片剧照，演职人员，上映时间，影片类型   
    3. 影院向系统确认信息  
    4. 影院重复2-3步，直到完成所有新影片上架  
    5. 影院输入结束，系统显示当前上架所有影片信息  
- 拓展流程：
    * 2a.影院发现有信息输入错误

    * 3-5a.影院发现有个别信息输入错误：  
        1.  影院输入影片标识搜索  
        2.  影院修改该影片信息冲，并确认  
        3.  系统重新显示当前上架的所有影片信息  
- 特殊需求：无

###4.2预售电影想看人数信息调整
- 用例编号：02
- 名称： 预售电影想看人数收集
- 创建者：happy_SE
- 最后一次更新者：happy_SE
- 更新日期：2019/3/19
- 参与者：影院 目标是收集预售想看人数来进行后期排片调整 观众 目标是支持所喜爱的电影，标记想看
- 触发条件：有新影片上架变成预售状态
- 前置条件：影院获得发行商影片放映许可，给预售电影进行排片
- 后置条件：存储影片名称及其对应想看人数
- 正常流程：  
    1. 影院开启预售电影  
    2. 影院确认预售电影信息  
    3. 影院重复1-2直到所有预售电影信息得到输入  
    4. 系统收集观众对各个预售电影的想看标记次数  
    5. 系统显示预售电影想看人数的排名及具体人次信息  
- 拓展流程：  
    * 1-4a.预售电影突发下架，或信息有误：  
        1. 影院在预售电影信息中输入影片标识  
        2. 影院删除该预售电影信息，或改正信息  
        3. 系统重新正确显示当前所有影片信息  
        
    * 3b.系统收集的某个电影想看次数在一小时内的增长速度突然同比加快200%以上：  
        1. 系统更改该影片想看的状态至无法更改状态  
        2. 系统删除该小时段所有预售电影的想看标记次数  
        
-    特殊需求：无
##5.需求分析模型
###5.1 系统顺序图

[sequendce diagram][2]
[2]:https://github.com/jiangxizhanzhi/resource/blob/master/系统顺序图1.PNG

[sequence diagram][3]
[3]:https://github.com/jiangxizhanzhi/resource/blob/master/系统顺序图2.PNG
      
###5.2 概念类图
[concenptual class diagram][4]
[4]:https://github.com/FNhaha/resouce/blob/master/软工二文档作业一/上架电影.png
[concenptual class diagram][5]
[5]:https://github.com/FNhaha/resouce/blob/master/软工二文档作业一/获取电影标记人数.png
[concenptual class diagram][6]
[6]:https://github.com/FNhaha/resouce/blob/master/软工二文档作业一/查看电影详情.png
[concenptual class diagram][7]
[7]:https://github.com/FNhaha/resouce/blob/master/软工二文档作业一/标记电影.png
[concenptual class diagram][8]
[8]:https://github.com/FNhaha/resouce/blob/master/软工二文档作业一/搜索.png