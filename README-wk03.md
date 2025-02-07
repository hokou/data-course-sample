# data-course-sample

## 專案目的

打造一個採用 Collaborative filtering 的推薦系統  


## 資料

- 訓練資料
  - 2000-01-10 - 2018-08-31(all)：370752  
  - 2018-09-01 - 2018-09-30(1y)：48612  
  - 2018-09-01 - 2018-09-30(3m)：7027  
  - 2018-09-01 - 2018-09-30(1m)：1662  

- 測試資料
  - 2018-09-01 - 2018-09-30：590 


## 作法

- User-based collaborative filtering
- Item-based collaborative filtering
- 使用 surprise 實作 collaborative filtering
  - 因記憶體限制，採用 1 年的資料當測試資料
  - User-based
  - UItem-based
- 針對推薦數不足的數量，加入前 1 個月賣最好的商品
  - 以之前使用 rule-based 採用賣出數最多的資料來看，愈近期的推薦分數愈高，因此採用前 1 個月的資料
    - 3 個月的資料分數為 0.13390 (0.13389830508474576)
    - 1 個月的資料分數為 0.15763 (0.1576271186440678)


## 結果

- 第一階段：依 collaborative filtering 實作
- 第二階段：依 collaborative filtering 實作，空的補上前一個月的 top 10 推薦
  - 可以發現分數幾乎都是依靠 rule-base 而增加的
- 使用 surprise 實作 user base 失敗，因此無相關資料
  - 比對資料發現，以 1 年的資料 48612 筆來看，去除重複的物品後為 8907，但去除重複的使用者後為 45373，數量差距很大，才會導致計算量增加 
  - 將資料降至 3 個月會有程式碼錯誤，推測要進行 id 轉換，考量目前 user 重複性不高，推薦效果較差，因此暫無調整
- 原本以為 Item-based 搭配 rule 的推薦分數會最高，但實際卻略低，推測原因是因為原本 Item-based 就比較有資料，因此遇到空 list 的機會較低，才會導致分數略低
- Item-based 手刻與使用套件，使用的資料是不同的，一個為全部，一個為 1 年，但分數卻相同，後續可以再確認是不是推薦的物品都相似

| 方法 | 訓練資料 | 第一階段 | 第二階段 |
| :----: | :----: | :----: | :----: |
| User-based  | all | 0.0 |0.15932203389830507|
| Item-based | all | 0.001694915254237288 |0.15423728813559323|
| surprise-item | 1 year | 0.001694915254237288 |0.15932203389830507|
