# ROC Curve
## 介紹
ROC 是在觀察，不同的閾值對於 Ture Positive rate / False Positive rate 的影響程度，線越往左上方靠近，模型的預測準確率會好，中間那條斜直線代表亂猜的 baseline，如果模型表現得與亂猜差不多，就等於這個模型沒什麼預測價值
。
* 完美 AUC = 1
<br>線趨近於左上角

<br><img src="ROC Curve High Performance.png" width="500">

* 沒預測價值的模型 AUC = 0.5
<br>線趨近於中線

<br><img src="ROC Curve Low Performance.png" width="500">

```python
import sklearn.metrics as metrics
from sklearn.metrics import roc_curve, auc

fpr, tpr, threshold = roc_curve(test_Y, pred_X)
# 面積值 auc
roc_auc = auc(fpr,tpr)



# ----------------畫圖----------------
import matplotlib.pyplot as plt
# 畫中間那條線
plt.plot([0, 1], [0, 1], 'k--')
# 繪製曲線
plt.plot(fpr, tpr, label='MODEL NAME (area = %0.3f)' % roc_auc)
plt.xlabel('False positive rate')
plt.ylabel('True positive rate')
plt.title('ROC curve')
plt.legend(loc='best')
plt.show()
```
Output：
<br><img src="ROC Curve.png" width="600">


## Reference
[Python 機器學習筆記 - 使用 ROC 曲線 (receiver operating characteristic curve) 評估分析成果](http://blog.changyy.org/2017/09/python-roc-receiver-operating.html)
