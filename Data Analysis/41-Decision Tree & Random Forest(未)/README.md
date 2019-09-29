# Decision Tree & Random Forest
## 介紹


## 常見的資訊料
- 熵 Entropy
- Gini不純度 Gini Impurity


## 常見問題
1. 在分類問題中，若沒有任何限制，決策樹有辦法在訓練時將 training loss 完全降成 0 嗎？
<br>若資料是符合函數的假設，亦即沒有一對多的情形，這時候如果不對決策樹進行限制，決策樹是可以為每一個訓練樣本找到其對應的規則，就能夠把訓練 loss 降為 ０
2. 決策樹只能用在分類問題嗎？還是可以用來解決回歸問題？
<br>決策樹同樣可以用來做回歸問題，這時評量資料相似程度則會用該群的平均數為每個值計算差距，可以想像標準差要是越小，該群中的樣本越相似。更多資訊可[參考](https://www.saedsayad.com/decision_tree_reg.htm)

## Reference
