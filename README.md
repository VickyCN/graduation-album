# 毕业纪念册APP
## 加值宣言：
目前市面上的毕业纪念册多为纸质版，有少数电子版的毕业纪念册APP，但多为校园内部使用。因此，我们设计一款可以在市面上使用的毕业纪念册APP，我们设置了小学、初中、高中、大学的同校范围毕业交际圈，用户通过添加个人信息后加入同校的交友圈中，在毕业后，用户选择显示同城设置来展现自己的地理位置，其中的用户通过一键发起同城聚会邀请进行聚会。基于APP能满足信息多元化且使用便捷性的优势，我们将调用静态地图API来显示聚会的位置定点显示，和路径规划API来选取最合适的路线，同时我们将加入图片信息，语音信息，视频信息等是区别于市场同类产品的一大特点。
## 核心价值：（最小可行性产品）
用户可以了解同城的校友位置，一键发送同城聚会定位，用户点击目的地即可从定位规划前往路线。

 - **静态地图** ：获取和显示位置标签信息。
 - **路径规划** ：提供步行、公交、驾车查询及行驶距离计算接口选择合适路径。
## 背景：
人们一毕业就各奔东西，但是在大家心中都有和同学聚餐的想法，但有时候想约出来聚餐总不是那么容易地事情，要么就是没有联系方式，要么就是距离太远无法约见。所以我们设计一款毕业纪念册，一款在自己圈的社交软件，用户通过显示同城展示地理位置，在静态地图页面上看见同城的校友位置信息，通过点击目的同时选择前行方式获得相应的前进路线。同时我们增加了传统的毕业纪念册的模式，即用户通过点击通讯录的头像，即可查看班级合照，同时用户可以在留言区下留下文字信息，相较于传统模式，我们增加在留言区语音留言的方式来保留我们的语言记忆。
## 目的：
相比传统添加好友方式，毕业纪念册APP可以通过注册填写详细信息就可以获得同样注册信息的校园圈的联系方式，同时用户可以自行选择是否展示自己的信息，方便用户寻找同学。
## 用户：
在校生、毕业生、任课老师
## 用户痛点：
- 场景一：想联系同学聚会，却没有联系方式。
- 场景二：想浏览曾经的同班同学的明言明语。
- 场景三：想联系一下没有联系方式的同学（没有微信、QQ、手机号联系方式）

## 人工智能概率性：
- **静态地图** ：室内环境位置定位可能会存在一定的偏差。
- **路径规划** ：由于道路、数据、算法的变更，很可能存在间隔一段时间后请求相同起终点的经纬度返回不同结果。

## 需求列表与人工智能API加值 ：

|  用户需求   | 对应API|  重要程度|
| --- | --- | --- |
|   用户想知道这所城市同学的位置分布  |  静态地图    |    重要 |
|   用户想去聚会的目的地  |  路径规划   |   重要  |

## API使用比较分析
- 高德地图API

|          | 个人开发        |                 | 认证个人开发    |                 | 企业开发        |                 |
| -------- | --------------- | --------------- | --------------- | --------------- | --------------- | --------------- |
|          | 调用量（次/日） | 并发量（次/秒） | 调用量（次/日） | 并发量（次/秒） | 调用量（次/日） | 并发量（次/秒） |
| 静态地图 | 100,000         | 400             | 3,000,000       | 500             | 6,000,000       | 1000            |
| 路径规划 | 2,000           | 20              | 3,000           | 50              | 300,000         | 200             |

- 百度地图API

|          | 未认证用户    |                 | 认证用户      |                 |               |                 |
| -------- | ------------- | --------------- | ------------- | --------------- | ------------- | --------------- |
|          |               |                 | 个人          |                 | 企业          |                 |
|          | 配额（次/日） | 并发量（次/秒） | 配额（次/日） | 并发量（次/秒） | 配额（次/日） | 并发量（次/秒） |
| 静态地图 | 100,000       | 400             | 3,000,000     | 500             | 6,000,000     | 500             |
| 路径规划 | 2000          | 20              | 30,000        | 50              | 300,000       | 200             |

这款毕业纪念册处于起步阶段，通过价比和成熟度的综合考量，在前期阶段我们将选择百度地图API个人认证用户的静态地图和路径规划的API调用，如若后期使用人数上调API的调用将视情况选择。
## 使用后风险报告：
目前国内的静态地图和路径规划的API调用平台，比较成熟的就是百度地图API和高德地图API。目前短期内使用百度地图的个人用户使用配合是比较划算的，当这款软件有一定成熟度、知名度和一定的使用基数时，可以考虑使用高德地图API的企业开发使用额度。

## 原型：
- [交互及界面设计：（HTML文档](http://nfunm026.gitee.io/graduation-album)）
- [原型文档下载区：] （https://github.com/VickyCN/graduation-album）
-毕业纪念册原型架构图

![原型界面的架构图]（https://images.gitee.com/uploads/images/2019/1207/124745_9c1f907a_1648228.jpeg“毕业纪念册架构图.JPG”）架构图
