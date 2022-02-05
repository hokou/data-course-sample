# data-course-sample

- [data-course-sample](#data-course-sample)
  - [計畫來源](#計畫來源)
  - [專案資料來源](#專案資料來源)
  - [專案成果](#專案成果)


## 計畫來源

資料人才種子計畫：[https://program.alphacamp.co/data-ai](https://program.alphacamp.co/data-ai)


## 專案資料來源

- [Amazon Review Data (2018)](https://nijianmo.github.io/amazon/index.html)
  - 這次的實作限縮「美妝（All Beauty）」類別的商品資料，包含兩種資料集
    - [All_Beauty.csv](http://deepyeti.ucsd.edu/jianmo/amazon/categoryFilesSmall/All_Beauty.csv)：提供使用者購買商品的紀錄
    - [meta_All_Beauty.json.gz](http://deepyeti.ucsd.edu/jianmo/amazon/metaFiles2/meta_All_Beauty.json.gz)：提供商品的基本資訊


## 專案成果

- [wk01](/README-wk01.md)：
  - 採用 rule-based 的推薦系統，分數：0.13390
- [wk02](/README-wk02.md)：
  - 採用 content-based 的推薦系統，分數：0.00339
  - 採用 content-based + rule-based 的推薦系統，分數：0.13729
- [wk03](/README-wk03.md)：
  - 採用 Collaborative filtering 的推薦系統，分數：0.00169
  - 採用 Collaborative filtering + rule-based 的推薦系統，分數：0.15932

