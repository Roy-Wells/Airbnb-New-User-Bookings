# Airbnb 新用户的民宿预定结果

![Airbnb](https://github.com/vichry/Airbnb-New-User-Bookings/Img/Airbnb.jpg)



### 写在前面

Airbnb的旅客会发现他们自己和鸟儿一起呆在奇妙的书屋中，享受着他们的早晨。或者在游艇甲板上喝着咖啡，又或者和主人一起做当地早餐，而不是睁眼便看到冷冰冰的标志——“请勿打扰”。

Airbnb的新用户可以在190多个国家的3.4万多个城市预订住宿。它能准确预测到新用户将在哪里预订他们的首次旅行体验。Airbnb还可以与他们的民宿提供更个性化的内容，减少首次预订的平均时间，并更好地预测需求。

在这场招聘竞争中，Airbnb将向你发出预测一个新用户会在哪个国家进行首次预订的挑战。凡是能够提供令人印象深刻的答案(和解释他们是如何到达那里的)的kaggler，将有机会获得采访并加入Airbnb的数据科学和分析团队。

![](C:\Users\vich\Desktop\A.I\Airbnb New User Bookings\Img\airbnb_banner.png)

### 评估方法

本次比赛的评价标准为NDCG@k，其中k=5。NDCG的计算公式为: 

![Evaluation_1](C:\Users\vich\Desktop\A.I\Airbnb New User Bookings\Img\Evaluation_1.png)

![1538634703543](C:\Users\vich\Desktop\A.I\Airbnb New User Bookings\Img\Evaluation_2.png)

对于每个新用户，你最多可以对第一次预订的国家做出5个预测。 其中正确预测到的国家，其相关性为1。其余相关性标记为0。

例如：如果一个特定用户的目标是FR，那么预测就变成了 

![1538634646162](C:\Users\vich\Desktop\A.I\Airbnb New User Bookings\Img\Evaluation_3.png)

### 提交文件说明

对于数据集中的每个用户，提交文件应该包含两列:id和country。目的地国家的预测必须按照最可能的目的地国家先行的顺序进行。 

该文件应包含表头，并具有以下格式: 

```
id,country
000am9932b,NDF
000am9932b,US
000am9932b,IT
01wi37r0hw,FR
etc.
```



****

相关参考：

【1】[Airbnb New User Bookings#description](https://www.kaggle.com/c/airbnb-recruiting-new-user-bookings#description)
