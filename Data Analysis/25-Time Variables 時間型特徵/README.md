# Time Variables 類別變數
## 介紹
時間有著週期性，通常會將時間的各個特徵拆開，年、月、日、時、分、秒，或改成週以及星期，就可以看出一些特徵．
<br>年週期：聖嬰現象、大事件變動（選舉）等
<br>月週期：四季溫度相關（稻穗、養殖）等
<br>周週期：週末假日出遊、星期一購買率可能價低？等
<br><img src="Time Variables 01.png" width="600">


```python
import datetime
df['year'] = df['time'].apply(lambda x: datetime.datetime.strftime(x, '%Y')).astype('int64')
df['month'] = df['time'].apply(lambda x: datetime.datetime.strftime(x, '%m')).astype('int64')
df['day'] = df['time'].apply(lambda x: datetime.datetime.strftime(x, '%d')).astype('int64')
# 星期 return 0~6
df['week'] = df['time'].apply(lambda x: datetime.datetime.strftime(x, '%w')).astype('int64')
```

<br>也可使用多個時間特徵並結合正弦函數sin或餘弦函數cos
<br>年週期（正：冷/負：熱）= cos((月/6+日/180)π)
<br>3月15日 = cos((1/2+15/180)π) = cos(95/180 π)
<br>周週期（正：精神飽滿/負：疲倦）= sin((星期幾/3.5 + 小時/84)π)
<br>日週期（正：精神飽滿/負：疲倦）= sin((小時/12+分/720+秒/43200)π)

```python
df['year_cycle'] = df['month']/6 + df['day']/180
df['year_cycle'] = df['year_cycle'].apply(lambda x: math.cos(x * math.pi))
```

## Reference
[datetime — Basic date and time types](https://docs.python.org/3/library/datetime.html)
