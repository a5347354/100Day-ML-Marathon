# Introduction of Machine Learning 機器學習介紹
## 介紹
機器學習屬於人工智慧下的分支，簡單來說就是讓***機器從資料中找尋規律與趨勢而不需要給定特殊規則***
> Field of study that gives computers the ability to learn without being explicity programmed.&nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  - Arthur Lee Samuel, 1959

<br><img src="What is Machine Learning.png" width="600">


## 機器學習又可分為哪些
目前可分為以下三種
<br>＊[監督式學習 Supervised Learning](#-監督式學習-supervised-learning)
<br>＊[非監督式學習 Unsupervised Learning](#-非監督式學習 unsupervised-learning)
<br>＊[半監督學習 Semi-supervised Learning](#-半監督學習-semi-supervised-learning)
<br>＊[強化學習 Reinforcement Learning](#-強化學習-reinforcement-learning)
<br><img src="Machine Learning.jpg" width="600">


### ＊ 監督式學習 Supervised Learning
 在訓練的過程中告訴機器答案，也就是「有標籤」的資料
 <br>例如：給機器各看了 1000 張貓和狗（標籤）的照片後，詢問機器新的一張照片中是貓還是狗
### ＊ 非監督式學習 Unsupervised Learning
訓練資料沒有標準答案、不需要事先以人力輸入標籤，故機器在學習時並不知道其分類結果是否正確。訓練時僅須對機器提供輸入範例，它會自動從這些範例中找出潛在的規則。
<br>例如：帶機器 1000 次去動物園看動物，他會慢慢開始分辨某類動物會飛，某類動物都是在水裡，是不同種類的動物，但不知道此類動物的名字．
### ＊ 半監督學習 Semi-supervised Learning
將資料分群的過程當中，先使用有標籤過的資料先切出一條分界線，再利用剩下無標籤資料的整體分布，調整出兩大類別的新分界。如此不但具有非監督式學習高自動化的優點，又能降低標籤資料的成本。
<br>例如：帶機器去 1000 次去動物園看動物，只告訴他其中一次動物園的所有動物，將有助於幫助學習
### ＊ 強化學習 Reinforcement Learning
透過觀察環境而行動，並會隨時根據新進來的資料逐步修正、以獲得最大利益。
<br>例如：讓機器去跟真人對話，講了半天後，那個人勃然大怒把電話掛掉，機器只會知道他做得不好，但不知道哪裡做錯，經由多次訓練，他會越來越好．



## Reference
[機器學習的機器是怎麼從資料中「學」到東西的？超簡單機器學習名詞入門篇！](https://kopu.chat/2017/07/28/機器是怎麼從資料中「學」到東西的呢/)
[Stanford 李飛飛教授 TED Talk - 如何教懂電腦看圖像](https://www.ted.com/talks/fei_fei_li_how_we_re_teaching_computers_to_understand_pictures?language=zh-tw)
