### 数据总述

在本次挑战中，将提供给你一个用户列表以及他们的人口统计信息、网页会话记录和一些汇总统计信息。你需要预测新用户的第一个预订目的地是哪个国家。该数据集中的所有用户都来自美国。 

目的地国有12种可能的结果，包含为:“US”、“FR”、“CA”、“GB”、“ES”、“IT”、“PT”、“NL”、“DE”、“AU”、“NDF”(没有找到目的地)和“other”。请注意，“NDF”与“other”不同，因为“other”表示有预订，但指的是未被列入名单的国家，而“NDF”表示没有预订。 

![1538635917098](https://github.com/vichry/Airbnb-New-User-Bookings/blob/master/Data_Description_1.png)

训练集和测试集按日期划分。在测试集中，你需要预测2014年7月1日之后所有新用户的首次活动(注意:这是在12月5日比赛重新开始时更新的)。在sessions数据集中，数据只能追溯到1/1/2014，而users数据集可以追溯到2010年。 

### 文件说明

1.![Data Description_2](https://github.com/vichry/Airbnb-New-User-Bookings/blob/master/Data_Description_2.png)**train_users.csv** ——用户训练数据（标签大致同下）

2.![Data Description_2](https://github.com/vichry/Airbnb-New-User-Bookings/blob/master/Data_Description_2.png)**test_users.csv** ——用户测试数据

数据包含特征如下：

| id                      | 用户id                   |
| :---------------------- | :----------------------- |
| date_account_created    | 账号注册时间             |
| timestamp_first_active  | 首次活跃时间             |
| date_first_booking      | 首次订房时间             |
| gender                  | 性别                     |
| age                     | 年龄                     |
| signup_method           | 注册方式                 |
| signup_flow             | 注册页面                 |
| language                | 语言                     |
| affiliate_channel       | 付费渠道                 |
| affiliate_provider      | 付费渠道提供方           |
| first_affiliate_tracked | 注册前首次接触的市场渠道 |
| signup_app              | 注册app                  |
| first_device_type       | 首次使用的设备类型       |
| first_browser           | 首次使用的浏览器类型     |
| **country_destination** | **预定国家（需要预测）** |

**注意，timestamp_first_active 可以早于date_account_created或date_first_booking，因为用户可以在注册之前进行搜索** 

3.![Data Description_2](https://github.com/vichry/Airbnb-New-User-Bookings/blob/master/Data_Description_2.png)**sessions.csv** ——网页浏览数据 

数据包含特征如下：

| user_id       | 用户id   |
| ------------- | -------- |
| action        | 用户行为 |
| action_type   | 行为类型 |
| action_detail | 具体细节 |
| device_type   | 设备类型 |
| secs_elapsed  | 停留时长 |

**sessions中的id与users中的id相对应**

4.![Data Description_2](https://github.com/vichry/Airbnb-New-User-Bookings/blob/master/Data_Description_2.png)**countries .csv** ——该数据集为目标国家及其位置的汇总统计数据 

5.![Data Description_2](https://github.com/vichry/Airbnb-New-User-Bookings/blob/master/Data_Description_2.png)**age_gender_bkts.csv** ——用户年龄、性别、目的地国家汇总统计 

6.![Data Description_2](https://github.com/vichry/Airbnb-New-User-Bookings/blob/master/Data_Description_2.png)**sample_submission.csv** ——提交预测的正确格式示例 

***

相关参考：

[[1] Airbnb New User Bookings#Data](https://www.kaggle.com/c/airbnb-recruiting-new-user-bookings/data)
