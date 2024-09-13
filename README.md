# [首页查询更多项目](https://github.com/GraduationProject-ssm) 包安装运行


# 10938ssm二手交易平台网站

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1Sh44eDEx6?p=39)


# 系统概述
进过系统的分析后，就开始记性系统的设计，系统设计包含总体设计和详细设计。总体设计只是一个大体的设计，经过了总体设计，我们能够划分出系统的一些东西，例如文件、文档、数据等。而且我们通过总体设计，大致可以划分出了程序的模块，以及功能。但是只是一个初步的分类，并没有真正的实现。

整体设计，只是一个初步设计，而且，对于一个项目，我们可以进行多个整体设计，通过对比，包括性能的对比、成本的对比、效益的对比，来最终确定一个最优的设计方案，选择优秀的整体设计可以降低开发成本，增加公司效益，从这一点来讲，整体设计还是非常重要的。

` `二手交易平台网站工作原理图如图4-1所示：

![](/md/blog.012.png)

图4-1 系统工作原理图
## 4.2 系统结构设计
系统架构图属于系统设计阶段，系统架构图只是这个阶段一个产物，系统的总体架构决定了整个系统的模式，是系统的基础。二手交易平台的整体结构设计如图4-2所示。

![](/md/blog.013.png)

图4-2 系统结构图
## 4.3数据库设计
数据库是计算机信息系统的基础。目前，电脑系统的关键与核心部分就是数据库。数据库开发的优劣对整个系统的质量和速度有着直接影响。
### 4.3.1 数据库设计原则
数据库的概念结构设计采用实体—联系（E-R）模型设计方法。E-R模型法的组成元素有：实体、属性、联系，E-R模型用E-R图表示，是提示用户工作环境中所涉及的事物，属性则是对实体特性的描述。在系统设计当中数据库起着决定性的因素。下面设计出这几个关键实体的实体—关系图。
### 4.3.2 数据库实体
数据模型中的实体（Entity），也称为实例，对应现实世界中可区别于其他对象的“事件”或“事物”。例如，公司中的每个员工，家里中的每个家具。

本系统的E-R图如下图所示：

1、用户管理实体图如图4-3所示：

![](/md/blog.014.png)

图4-3用户管理实体图

2、商家管理实体图如图4-4所示：

![](/md/blog.015.png)

`                               `图4-4商家管理实体图

3、订单配送管理实体图如图4-5所示：

![](/md/blog.016.png)

`                              `图4-5订单配送管理实体图

#########

### 4.3.3 数据库表设计
数据库的表信息属于设计的一部分，下面介绍数据库中的各个表的详细信息。

表4-1 dingdanpeisong表

|列名|数据类型|长度|约束|
| :- | :- | :- | :- |
|id|int|11|NOT NULL|
|dingdanbianhao|varchar|50|` `default NULL|
|shangpinmingcheng|varchar|50|` `default NULL|
|shuliang|varchar|50|` `default NULL|
|yonghuming|varchar|50|` `default NULL|
|yonghuxingming|varchar|50|` `default NULL|
|shoujihaoma|varchar|50|` `default NULL|
|shouhuodizhi|varchar|50|` `default NULL|
|fahuoriqi|varchar|50|` `default NULL|
|shangjiahao|varchar|50|` `default NULL|
|shangjiamingcheng|varchar|50|` `default NULL|


表4-2dingdanxinx表

|列名|数据类型|长度|约束|
| :- | :- | :- | :- |
|id|int|11|NOT NULL|
|addtime|varchar|50|default NULL|
|dingdanbianhao|varchar|50|default NULL|
|shangpinmingcheng|varchar|50|default NULL|
|chengse|varchar|50|default NULL|
|jiage|varchar|50|default NULL|
|shuliang|varchar|50|default NULL|
|zongjine|varchar|50|default NULL|
|shangjiahao|varchar|50|default NULL|
|xiadanriqi|varchar|50|default NULL|
|beizhu|varchar|50|default NULL|
|yonghuming|varchar|50|default NULL|
|yonghuxingming|varchar|50|default NULL|
|shoujihaoma|varchar|50|default NULL|
|shouhuodizhi|varchar|50|default NULL|

表4-3：shangjia表

|列名|数据类型|长度|约束|
| :- | :- | :- | :- |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|shangjiahao|varchar|50|default NULL|
|mima|varchar|50|default NULL|
|shangjiamingcheng|varchar|50|default NULL|
|tupian|varchar|50|default NULL|
|lianxiren|varchar|50|default NULL|
|lianxidianhua|varchar|50|default NULL|
|dizhi|varchar|50|default NULL|


表4-4：shangpinxinxi表

|列名|数据类型|长度|约束|
| :- | :- | :- | :- |
|id|` `int|11|NOT NULL |
|addtime|varchar|50|default NULL|
|shangpinmingcheng|varchar|50|default NULL|
|tupian|varchar|50|default NULL|
|guige|varchar|50|default NULL|
|pinpai|varchar|50|default NULL|
|chengse|varchar|50|default NULL|
|jiage|varchar|50|default NULL|
|shuliang|varchar|50|default NULL|
|shangpinxiangqing|varchar|50|default NULL|
|shangjiahao|varchar|50|default NULL|
|shangjiamingcheng|varchar|50|default NULL|
|dizhi|varchar|50|default NULL|

# 5统详细设计
## 5.1商家能模块
`  `商家首页，在商家首页页面可以查看个人中心、商品分类管理、商品信息管理、订单信息管理、订单配送管理信息，如图5-1所示。

![](/md/blog.017.png)

图5-1商家首页界面图



`     `个人中心，用户通过个人中心可以查看用户名、用户姓名、头像、性别、手机号码、邮箱等信息操作，如图5-2所示。

![](/md/blog.018.png)

图5-2 个人中心界面图

商品分类管理，用户通过商品分类管理可以查看商品分类、操作等信息进行查看、修改或删除，如图5-3所示。

![](/md/blog.019.png)

图5-3个人中心界面图

商品信息管理，用户通过商品信息管理可以查看商品名称、图片、规格、品牌、成色、价格、数量、商品详情、商家号、商家名称、地址等信息进行查看、修改或删除，如图5-4所示。


![](/md/blog.020.png)

图5-4商品信息管理界面图

## 5.2管理员功能模块
管理员登录，通过填写注册时输入的用户名、密码进行登录，如图5-5所示。

![](/md/blog.021.png)

图5-5管理员登录界面图

管理员首页：管理员通过在管理员首页进入页面可以查看个人中心、用户管理、商家管理、商品信息管理、论坛管理、系统管理等功能模块，进行相对应操作，如图5-6所示。

![](/md/blog.022.png)

图5-6管理员首页界面图







用户管理：管理员通过在用户管理进入页面可以查看用户名、用户姓名、头像、性别、手机号码、邮箱等并进行查看、删除、修改操作，如图5-7所示。


![](/md/blog.023.png)

图5-7用户管理界面图

商家管理：管理员在通过商家管理进入页面可以查看商家号、商品名称、图片、联系人、联系电话、地址等信息，并进行查看、删除、修改操作，如图5-8所示。

![](/md/blog.024.png)

图5-8 商家管理面图


商品信息管理：管理员在通过商品信息管理进入页面可以查看商品名称、图片、规格、品牌、成色、价格、数量、商品详情、商家号、商家名称、地址等信息，并进行查看、删除、修改操作，如图5-9所示。

![](/md/blog.025.png)

图5-9商品信息管理界面图

论坛管理：管理员在通过论坛管理进入页面可以查看商品名称、图片、规格、品牌、成色、价格、数量、商品详情、商家号、商家名称、地址等信息，并进行查询、删除、添加操作，如图5-10所示。

![](/md/blog.026.png)

图5-10论坛管理界面图

轮播图管理管理，该页面为轮播图管理界面。管理员可以在此页面进行首页轮播图的管理，通过新建操作可在轮播图中加入新的图片，还可以对以上传的图片进行修改操作，以及图片的删除操作，如图5-11所示。

![](/md/blog.027.png)

图5-11轮播图管理管理界面图

## 5.3用户功能模块
用户首页，在用户首页页面可以查看个人中心、订单信息管理、订单配送管理、我的收藏管理等信息，如图5-12所示。

![](/md/blog.028.png)

图5-12用户首页界面图

订单信息管理，用户通过订单信息管理可以查看订单编号、商品名称、成色、价格、数量、总金额、商家号、下单日期、备注、用户名、用户姓名、手机号码、收货地址、是否支付等信息查看、支付操作，如图5-13所示。

![](/md/blog.029.png)

图5-13订单信息管理界面图

订单配送管理，用户通过订单配送管理可以查看订单编号、商品名称、数量、用户名、用户姓名、手机号码、收货地址、发货日期、商家号、商品名称等信息查看操作，如图5-14所示。

![](/md/blog.030.png)

图5-14订单配送管理界面图














