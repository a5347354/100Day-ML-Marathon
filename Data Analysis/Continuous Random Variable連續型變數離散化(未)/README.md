# Continuous Random Variable 連續型變數離散化
## 介紹
> 離散化主要減少 outlier 對 分析以及訓練模型的影響

## 主要方法Method
* 等寬劃分 bins based on values:按照相同寬度將資料分成幾等份。缺點是受到異異常值的影響比較⼤大（等距）
> 依照年齡10-20，20-30
> <br>pandas.cut(DATA, BINs)

* 等頻劃分 bins based on sample quantiles:將資料分成幾等份，每等份資料裡⾯面的個數是⼀一樣的（等份）
> 依照資料筆數年齡10-15有3人，15-18有3人
> <br>pandas.qcut(DATA, )

* 聚類劃分:使⽤用聚類演算法將資料聚成幾類，每⼀一個類為⼀一個劃分（特徵）

## Reference
[连续特征的离散化：在什么情况下将连续的特征离散化之后可以获得更好的效果？](https://www.zhihu.com/question/31989952)
