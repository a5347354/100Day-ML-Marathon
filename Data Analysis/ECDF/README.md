# Empirical distribution function 經驗累積分佈函數圖
## 介紹與實作
> 用於觀察資料的分布，可顯示所有的數據點．
> <br>直方圖可以直觀的找到眾數，但在數據量較少的地方無法顯示出來．

#### 條件
* 排序
* 累計



#### Example 1
```python
from statsmodels.distributions.empirical_distribution import ECDF
# 資料
cdf_ecdf = ECDF(app_train['AMT_INCOME_TOTAL'],side='right')
cdf_x = cdf_ecdf.x[1:]
cdf_y = cdf_ecdf.y[1:]



#------------------畫圖------------------
plt.plot(list(cdf_x), cdf_y/cdf_y.max())
plt.xlabel('Value')
plt.ylabel('ECDF')
plt.xlim([cdf_x.min(), cdf_x.max() * 1.05]) # 限制顯示圖片的範圍
plt.ylim([-0.05,1.05]) # 限制顯示圖片的範圍

plt.show()

# 改變 y 軸的 Scale, 讓我們可以正常檢視 ECDF
plt.plot(np.log(list(cdf_x)), cdf_y/cdf_y.max())
plt.xlabel('Value (log-scale)')
plt.ylabel('ECDF')

plt.ylim([-0.05,1.05]) # 限制顯示圖片的範圍

plt.show()
```



## Reference
[Exploratory Data Analysis : 探索資料-ECDF](https://medium.com/ai反斗城/exploratory-data-analysis-探索資料-ecdf-7fa350c32897)
