# Missing Value
## 介紹
資料中常常會因人為輸入或某些因素造成部分資料未填入．
<br><img src="Missing Values 01.png" width="600">
<br>
<br><img src="Missing Values 02.png" width="600">
## How to deal with missing datas

### 填補
＊ [填補統計值](#-填補統計值)
<br>＊ [填補指定值](#-填補指定值)
<br>＊ [填補預測值](#-填補預測值)

#### ＊ 填補統計值
* 填補平均值 Mean：數值型欄欄位，偏態不明顯

```python
import numpy as np
mean_value = df['屋齡'].mean()
df['屋齡'] = df['屋齡'].fillna(mean_value)
```
* 填補中位數 Median：數值型欄欄位，偏態很明顯

```python
import numpy as np
median_value = df['屋齡'].median()
df['屋齡'] = df['屋齡'].fillna(median_value)
```
* 填補眾數 Mode：類別型欄位

```python
# 方法一 - 推薦
import pandas as pd
mode_value = df['行政區'].mode()[0]
df['行政區'] = df['行政區'].fillna(mode_value)
```

```python
# 方法二
from scipy import status
mode_value = stats.mode(df['行政區'])[0][0]
df['行政區'] = df['行政區'].fillna(mode_value)
```

```python
# 方法三 - 僅適用數值型類別
import numpy as np
counts = np.bincount(df['行政區'])
mode_value = np.argmax(counts)
df['行政區'] = df['行政區'].fillna(mode_value)
```


#### ＊ 填補指定值
需對欄位領域知識已有了解
* 補不可能出現的數值：類別型欄位，且不適合眾數時
* 補 0：某些欄位，0本身就有含意

```python
import numpy as np
df['房間數'] = df['房間數'].fillna(0)
```



#### ＊ 填補預測值
速度慢但精確，若填補範圍廣，且是重要特徵欄位可用此方式



## Reference
其他缺失值處理參考
<img src="數據缺失值處理.png" width="600">
<br>[Missing Value Treatment | 遺失值處理 | 統計 R語言](https://www.jamleecute.com/missing-value-treatment-遺失值處理/)
