# Cross Validation 交叉驗證
## 介紹
> 交叉驗證是一種統計學上將樣本切割成多個小子集的做測試與訓練

<br><img src="Cross Validation.png">
如上圖，將資料分成十等分，並做十次
* 第一次(Round 1)拿第1份當作驗證，其他9份當作測試
* 第二次(Round 2)拿第2份當作驗證，其他9份當作測試
* ....
* 將十次的準確性Accuracy平均，越高代表越好．

#### 分為以下幾類
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
X = iris.data
y = iris.target

#------------------Knn分類法------------------
#分成十組資料，找十個鄰居
knn = KNeighborsClassifier(n_neighbors=10)

#accuracy是一種方法，越高越好
scores = cross_val_score(knn,X,y,cv=5,scoring='accuracy')
print(scores)
print(scores.mean())

## [ 0.96666667 1. 1. 0.93333333 1. ]
## 0.98
```



## Reference
[Day29 機器學習：交叉驗證！](https://ithelp.ithome.com.tw/articles/10197461)
