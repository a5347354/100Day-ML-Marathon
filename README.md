# 機器學習 百日馬拉松
藉由這個活動，來好好學習python以及機器學習，並配合numpy和pandas兩個套件。

### 每日作業
- 資料清理數據前處理
 - [D1: 資料介紹與評估資料](Day_001_HW.ipynb)
 - [D2: EDA-1/讀取資料EDA: Data summary](Day_002_HW.ipynb)
 - D3: 如何新建一個 dataframe?3-2 如何讀取其他資料? (非 csv 的資料)
    - [D3 Homework 1](Day_003-1_HW.ipynb)
   <br>亂數randint、array, list, dataframe 之間的轉換、找出最多人口的國家max

    - [D3 Homework 2](Day_003-2_HW.ipynb)
   <br>讀取txt 或 網頁資料，切割字串split與用URL顯示圖片

 - [D4: EDA：欄位的資料類型介紹及處理](Day_004_HW.ipynb)
 <br>One Hot encoding - pandas.get_dummies([DATA])

 - [D5: EDA資料分佈](Day_005_HW.ipynb)
 <br>Mean、Median、Sample Standard Deviation、Hist

 - [D6: EDA: Outlier 及處理](Day_006_HW.ipynb)
 <br>找出並處理 Outliers、ECDF、直方圖 Histogram

[ECDF Note](Data\ Analysis/ECDF/README.md)

 - [D7: 常用的數值取代：中位數與分位數連續數值標準化](Day_007_HW.ipynb)
 <br>遺漏值未移除計算percentile會有問題、 NAs 以 q50 填補、Normalize function、列出重複最多的數值

 - [D8: DataFrame operationData frame merge/常用的 DataFrame 操作](Day_008_HW.ipynb)
 <br>分群 cut, groupby, apply & lambda

 - [D9: EDA：correlation相關係數簡介](Day_009_HW.ipynb)
 <br>計算相關係數np.corrcoef、畫出數據點分佈scatter

 - [D10: EDA from Correlation](Day_010_HW.ipynb)
 <br>計算相關係數np.corrcoef、觀察與其他欄位之分佈圖

 - [D11: EDA: 不同數值範圍間的特徵如何檢視/繪圖與樣式Kernel Density Estimation (KDE)](Day_011_HW.ipynb)
 <br>KDE圖形比較 seaborn.distplot、barplot

 - [D12：EDA: 把連續型變數離散化](Day_012_HW.ipynb)
 <br>等距劃分、等頻劃分 cut、qcut

 - [D13：程式實作 把連續型變數離散化](Day_013_HW.ipynb)
 <br>離散化實作

 - [D14：Subplots](Day_014_HW.ipynb)
 <br>subplot排版（多合一顯示）

 - [D15：Heatmap & Grid-plot](Day_015_HW.ipynb)
 <br>sns.heatmap Plot圖與sns.PairGrid Plot圖，np.random.uniform產生亂數

 - [D16：模型初體驗 Logistic Regression](Day_016_HW.ipynb)
 <br>Convert dataframe to csv and Upload to Kaggle

 - [D17：特徵工程簡介](Day_017_HW.ipynb)
 <br>LabelEncoder

 - [D18：特徵類型](Day_018_HW.ipynb)
 <br>df.dtypes.reset_index()、for in zip

 - [D19：數值型特徵-補缺失值與標準化](Day_019_HW.ipynb)
 <br>補缺失值：df.fillna() 0,-1,mean()
 <br>標準化：StandardScaler()、MinMaxScaler()
 <br>迴歸：LogisticRegression、cross_val_score

 - [D20：數值型特徵 - 去除離群值](Day_020_HW.ipynb)
 <br>clip 調整離群值
 <br>df[(df>0) & (df<100)] 移除離群值

 - [D21：數值型特徵 - 去除偏態](Day_021_HW.ipynb)
 <br>對數去偏 log1p、方根去偏 sqrt、分佈去偏 boxcox
    - [Note：Remove Skewness](Data%20Analysis/Missing%20Value數據缺失值處理/README.md)

 - [D22：類別型特徵 - 基礎處理](Day_022_HW.ipynb)
 <br>Categorical Variables：LabelEncode & OneHotEncoder
   - [Note：Label Encoding & One Hot Encoding](Data%20Analysis/22-Categorical%20Variables%20類別變數特徵/README.md)

 - [D23：類別型特徵 - 均值編碼](Day_023_HW.ipynb)
 <br>Categorical Variables：Mean Encoding
    - [Note：Mean Encoding](Data%20Analysis/22-Categorical%20Variables%20類別變數特徵/README.md)

 - [D24：類別型特徵 - 其他進階處理](Day_024_HW.ipynb)
    <br>Categorical Variables：Count Encoding & Feature Hash
   - [Note：Count Encoding & Feature Hash](Data%20Analysis/22-Categorical%20Variables%20類別變數特徵/README.md)

 - [D25：時間型特徵](Day_025_HW.ipynb)
 <br>Time Variables
    - [Note：Time Variables](Data%20Analysis/25-Time%20Variables%20時間型特徵/README.md)

 - [D26：特徵組合 - 數值與數值組合](Day_026_HW.ipynb)
 - [D27：特徵組合 - 類別與數值組合](Day_027_HW.ipynb)
    - [Note：Group by Encoding](Data%20Analysis/22-Categorical%20Variables%20類別變數特徵/README.md)
 - [D28：特徵選擇](Day_028_HW.ipynb)
 <br>Filter、Wrapper、Embedded三種主要方法
    - [Note：Feature Selection](Data%20Analysis/28-Feature%20Selection%20特徵選擇/README.md)
