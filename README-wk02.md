# data-course-sample

## 專案目的

打造一個採用 content-based 的推薦系統  


## 資料

訓練資料：2000-01-10 - 2018-08-31  
測試資料：2018-09-01 - 2018-09-30  
數量：370752 / 590  

訓練資料：2018-06-01 - 2018-08-31  
測試資料：2018-09-01 - 2018-09-30  
數量：7027 / 590  


## 作法

- 先比對一下驗證上有重複的使用者，發現重複性太低，導致依照使用者的推薦資料幾乎都是空的
  - 全部的區間對比測試只有 38 位重複  
  - 換到前 3 個月對比測試只有 4 位重複  
- 參考同學的作法 `df = df.reset_index()` 調整排序，得到第一階段分數
- 原本有加入正則想減少訓練所耗記憶體，但搭配 reset_index 卻會導致推薦變 0，只能先取消
- 最後搭配上次的 top 10 推薦，把空的推薦補上，得到第二階段分數


## 結果

- 第一階段：依照購買記錄推薦
- 第二階段：依照購買記錄推薦，空的補上 top 10 推薦
  - 上次 top 10 的推薦分數有 0.13389830508474576

| 訓練資料 | 重複人數 | 第一階段 | 第二階段 |
| :----: | :----: | :----: | :----: |
| 全部  | 38 | 0.005084745762711864 |0.13559322033898305|
| 3個月 | 4 | 0.003389830508474576 |0.13728813559322034|

