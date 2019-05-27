# Categorical Variables 類別變數
##介紹
> 此變數代表著某一個狀態、屬性，像是性別、膚色等，又可分為有序 oridnal及無序 nominal，而我們常將文字的訊息轉化成電腦較好處理的訊息．

<br><img src="Categorical Variables.png">

## 類別變數分為哪幾類？
* 有序變數 Oridnal Variables
> 有序變數代表其資料是有順序之分的，如成績分為A++、A+、A、B++、B+、B或著小學、國中、高中、大學，較適合用***Label Encoding***處理
* 無序變數 Non-ordinal/Nominal Variables
> 無序變數代表資料並無順序，像是髮色、人種等，適合用***One Hot Encoding***處理

## 該如何處理呢？
* 標籤編碼 Label Encoding
> 類似流水號，將類別依序填上代碼

<br><img src="Label Encoding.png">

```python
from sklearn.preprocessing import LabelEncode
import numpy as np
taipei = [ ['信義區', 1],
           ['南港區', 2],
           ['大安區', 3],
           ['南港區', 2],
           ['信義區', 0],
           ['文山區', 2]]
taipei = np.array(taipei)
# -----------LabelEncoder-----------
taipei[:, 0] = LabelEncoder().fit_transform(taipei[:, 0])
"""output
       行政區
array([['0', '1'],
       ['1', '2'],
       ['2', '3'],
       ['1', '2'],
       ['0', '0']],
       ['3', '2']],
      dtype='<U4')
"""
```
* 獨熱編碼 One Hot Encoding
> 將不同類別獨立一欄，並以0和1代表
> <br>缺點：浪費記憶體空間與計算時間

<br><img src="One Hot Encoding.png">

```python
# 第一種做法
import pandas as pd
pd.get_dummies(taipei['行政區'])
```

```python
# 第二種做法
from sklearn.preprocessing import OneHotEncoder
taipei = [ ['信義區', 1],
           ['南港區', 2],
           ['大安區', 3],
           ['南港區', 2],
           ['信義區', 0],
           ['文山區', 2]]
taipei = np.array(taipei)
# -----------One Hot Encoder-----------
enc = preprocessing.OneHotEncoder()
enc.fit(taipei)
"""output
        信義  | 南港 | 大安 | 文山 | 0 | 1 | 2 | 3
array([[ 1.,    0.,    0.,   0.,  0., 1., 0., 0.,],
       [ 0.,    1.,    0.,   0.,  0., 0., 1., 0.,],
       [ 0.,    0.,    1.,   0.,  0., 0., 0., 1.,],
       [ 0.,    1.,    0.,   0.,  0., 0., 1., 0.,],
       [ 1.,    0.,    0.,   0.,  1., 0., 0., 0.,],
       [ 0.,    0.,    0.,   1.,  0., 0., 1., 0.,]])
"""
```


##### Conclusion
處理方式         |記憶體空間／計算時間 |適用模型
----------------|----------------:|-------:
Label Encoding  |小/小             |樹狀模型
One Hot Encoding|較大/較長          |非樹狀模型
sparse

## Reference
[Python机器学习中的实用小操作(一)：数据清理篇](https://zhuanlan.zhihu.com/p/29893734)
<br>[数据预处理：独热编码（One-Hot Encoding）和 LabelEncoder标签编码](https://www.twblogs.net/a/5baab6e32b7177781a0e6859/zh-cn/)
<br>[Sklearn 的 OneHotEncoder 說明與簡單範例](https://tree.rocks/python/sklearn-explain-onehotencoder-use/)
