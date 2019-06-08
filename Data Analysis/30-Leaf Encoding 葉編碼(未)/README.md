# Leaf Encoding 葉編碼
## 介紹
簡單來說就是將，針對特徵使用決策樹 Decision tree，產生出來的葉節點，當作新的特徵(分類型特徵)，再以新特徵進行羅吉斯迴歸Logistic regression 合併預測，當然也可結合其他算法，例如分解機Factorization Machine．
<br><img src="Leaf Encoding.png" width="600">



## Reference
[Feature transformations with ensembles of trees¶](https://scikit-learn.org/stable/auto_examples/ensemble/plot_feature_transformation.html#example-ensemble-plot-feature-transformation-py)
[CTR预估 十一: Algorithm-GBDT Encoder](https://zhuanlan.zhihu.com/p/31734283)
