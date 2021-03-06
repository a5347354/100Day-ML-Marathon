# Cross Validation 交叉驗證
## 介紹
交叉驗證是一種統計學上將樣本切割成多個小子集的做測試與訓練，若將所有資料拿來建立模型，就無其他資料評估模型的好壞，為避免***overfitting***的情形發生，需透過驗證/測試集來評估模型．

<br><img src="Cross Validation.png" width="600">
<br>如上圖，將資料分成十等分，並做十次
* 第一次(Round 1)拿第1份當作驗證，其他9份當作測試
* 第二次(Round 2)拿第2份當作驗證，其他9份當作測試
* ....
* 將十次的準確性Accuracy平均，*越高代表越好*．

## 分為以下幾類
* k-folder cross-vailation
* kk folder cross-vaildation
* least-one-out cross-validation
* 10-fold corss validation




#### Example 1
```python
from sklearn.cross_validation import cross_val_score
from sklearn import datasets
from sklearn.cross_validation import train_test_split
from sklearn.neighbors import KNeighborsClassifier
import numpy as np

# 資料
iris = datasets.load_iris()
x = iris.data
y = iris.target


#分成十組資料，找十個鄰居
knn = KNeighborsClassifier(n_neighbors=10)
#-----------------cross_val_score-------------------
#accuracy是一種方法，越高越好，cv=5分成五組（上述圖是十組）
scores = cross_val_score(knn,x,y,cv=5,scoring='accuracy')
print(scores)
print(scores.mean())

## [ 0.96666667 1. 1. 0.93333333 1. ]
## 0.98
```



## Reference
[Day29 機器學習：交叉驗證！](https://ithelp.ithome.com.tw/articles/10197461)
