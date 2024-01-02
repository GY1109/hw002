# 人工智慧期末報告-天氣預報的時間序列預測
11124201 許昱鴻 11124203 黃恩維 11124240 蘇韋齊
## 準備資料
●可使用之Colab帳號

●馬克斯普朗克生物地球化學研究所記錄的耶拿氣候資料集
## 實際操作
## 1 導入和設定

<img width="212" alt="1" src="https://github.com/30zzz/AI1228/assets/113405753/bade69d0-d9ff-4fd7-9e05-a216e9fd228f">

<img width="520" alt="2" src="https://github.com/30zzz/AI1228/assets/113405753/c0182065-0e37-4c48-9080-8d3791bf1d04">

## 2 數據可視化

為了讓我們了解我們正在使用的數據，每個特徵都繪製在下面。這顯示了 2009 年至 2016 年期間每個特徵的獨特模式。它還顯示了存在異常的位置，這些異常將在標準化過程中得到解決。

<img width="508" alt="3" src="https://github.com/30zzz/AI1228/assets/113405753/d1b460fb-61da-4721-9276-2c4c2edac535">

<img width="512" alt="4" src="https://github.com/30zzz/AI1228/assets/113405753/b5c83d40-af8a-4481-9cda-da84b2b77d19">

## 3 資料預處理

此模型顯示前 5 天的數據，即每小時採樣一次的 720 個觀測值。72（12小時*每小時6次）觀測後的溫度將作為標籤。

<img width="308" alt="5" src="https://github.com/30zzz/AI1228/assets/113405753/eb60ba7e-1553-4527-9342-1dbccc57b62c">

<img width="409" alt="6" src="https://github.com/30zzz/AI1228/assets/113405753/7d422d3e-fc85-4dde-9b5d-c7e1e4d46af2">

## 4 訓練資料集

此timeseries_dataset_from_array函數接受以相等間隔收集的資料點序列以及時間序列參數（例如序列/視窗的長度、兩個序列/視窗之間的間距等），以產生批次的子時間序列輸入和取樣目標從主要時間序列來看。

<img width="288" alt="7" src="https://github.com/30zzz/AI1228/assets/113405753/fe62cbfe-a281-44d3-9525-7c48f4909fe8">

<img width="374" alt="8" src="https://github.com/30zzz/AI1228/assets/113405753/63730537-d6c4-4e14-9f00-50c14dbadb6d">

## 5 驗證資料集

<img width="350" alt="999" src="https://github.com/30zzz/AI1228/assets/113405753/50154729-1e96-4983-8774-27b8e4155b14">

## 6 訓練

可以使用下面的函數將損失視覺化。一分之後，損失停止減少。

<img width="332" alt="1" src="https://github.com/30zzz/AI1228/assets/113405753/f4d93168-3a83-4c4d-9460-740c419d3e3f">

<img width="482" alt="2" src="https://github.com/30zzz/AI1228/assets/113405753/fc43de4a-9ebb-438b-9a01-b94618695c5a">

## 7 預言

經過訓練的模型現在能夠對驗證集中的 5 組值進行預測。

<img width="483" alt="3" src="https://github.com/30zzz/AI1228/assets/113405753/d227dfb1-c7dc-42ec-92c2-577a01c5bb67">

<img width="449" alt="4" src="https://github.com/30zzz/AI1228/assets/113405753/4ac081d0-7868-44be-a350-eab05eddc7c2">

<img width="461" alt="5" src="https://github.com/30zzz/AI1228/assets/113405753/b37da828-b2bd-42d4-8b18-886b7c83cc80">

<img width="463" alt="6" src="https://github.com/30zzz/AI1228/assets/113405753/b655071d-b281-4797-9267-7e6ee3c1b991">

<img width="448" alt="7" src="https://github.com/30zzz/AI1228/assets/113405753/374ca40d-003a-404f-8636-8fd4405d4e45">


<img width="428" alt="8" src="https://github.com/30zzz/AI1228/assets/113405753/3aa361d2-9cc7-4191-9b58-fd0f693174e4">
