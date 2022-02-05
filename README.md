# data-course-sample

- [data-course-sample](#data-course-sample)
  - [計畫來源](#計畫來源)
  - [專案資料來源](#專案資料來源)
  - [專案成果](#專案成果)
  - [心得](#心得)


## 計畫來源

- 資料人才種子計畫：[https://program.alphacamp.co/data-ai](https://program.alphacamp.co/data-ai)
- 招募 50 名種子挑戰者
  - 具有一定 Python/工具基礎，通過技術評估
  - 每週投入 15-20 小時實作、積極參與班級討論
  - 連續六週持續並完成學習，全額免費
  - Top 10% 表現優異者，獲得業界導師推薦與 3 個月 Mentor Coaching


## 專案資料來源

- [Amazon Review Data (2018)](https://nijianmo.github.io/amazon/index.html)
  - 這次的實作限縮「美妝（All Beauty）」類別的商品資料，包含兩種資料集
    - [All_Beauty.csv](http://deepyeti.ucsd.edu/jianmo/amazon/categoryFilesSmall/All_Beauty.csv)：提供使用者購買商品的紀錄
    - [meta_All_Beauty.json.gz](http://deepyeti.ucsd.edu/jianmo/amazon/metaFiles2/meta_All_Beauty.json.gz)：提供商品的基本資訊
- iCook Data：經過整理過的資料


## 專案成果

- [wk01](README-wk01.md)：
  - file：[wk01_sample](wk01_sample.ipynb)
  - 採用 rule-based 的推薦系統，分數：0.13390
- [wk02](README-wk02.md)：
  - file：[wk02_sample-content-based](wk02_sample-content-based.ipynb)
  - 採用 content-based 的推薦系統，分數：0.00339
  - 採用 content-based + rule-based 的推薦系統，分數：0.13729
- [wk03](README-wk03.md)：
  - file：[wk03_sample-collaborative-filtering](wk03_sample-collaborative-filtering.ipynb)
  - 採用 Collaborative filtering 的推薦系統，分數：0.00169
  - 採用 Collaborative filtering + rule-based 的推薦系統，分數：0.15932
- wk04/wk05：
  - iCook 專案，採用 rule-based
  - wk04 分數：0.00608
  - wk05 分數：0.00842


## 心得

- 一開始看到課程的時候就有點心動想要參加，畢竟是自己還算熟悉的 Python，好不容易通過技術評估後就趕緊報名，沒想到後來卻變成保證金制度，然後名額限縮至 50 名，聽到報名人數有 800 多人，真是嚇到我了，後來有幸能夠被選上，真的是超乎預料之外
- 課程上的安排很扎實，學習過程讓我們體驗到推薦系統的原理與相關作法，一開始對推薦系統不太熟悉，又要完成每週的進度，像一開始的 rule-based 真是差點就過不了關，會有一些想法但卻不知道怎麼靠程式(pandas)實作，因此如果想要參與，對於 pandas 在對各種資料集的組合或篩選的語法建議要多熟悉，才不會手忙腳亂，最後用了一個比較簡單的做法來實作，意外的效果還不差，後來在助教分享時也了解這算是意料之中，也是後來 Richard(iCook 技術長) 提到的簡單卻有用，但是長期對使用者來說，信賴感就比較難建立，因此才會針對使用者做不同的推薦
- 參與的同學都超強大的，有各種不同領域的，因此從同學分享的作業成果可以學習到很多想法與概念，也很佩服各位同學可以在這麼短的時間實做出那麼多種想法，觀察各個同學的做法可以讓自己有更多的想法與了解程式的用法，每看一個都很有收穫，可惜時間有限(繳交期限)，沒辦法把每個同學的做法都詳細看過，後續要再安排時間多加學習
- 每週的工作坊算是比較特別的體驗，初期的案例討論，尤其後期 Richard 不藏私的分享，讓我收穫很多，讓我們確實了解一個平台在經營時遇到的問題與做法，而且實際遇到的問題其實是需要各種不同的方法來實踐，最終才成為一個比較完整解決方案的
- 工作坊中其實還有一個特別的點是同學的分享(Show & Tell)，在前一天通知被選上的同學，然後在隔天的工作坊分享，幾乎每位都讓人佩服，竟然能在這麼短時間做投影片並整理概念分享，想到如果換成自己，肯定手忙腳亂
- 在這幾週的學習過程中可以看到 AC 團隊的投入，不管是教材內容與工作坊的準備，就連課程規劃也有一直在調整修正，可以感受到那種想讓大家有更好的學習體驗的心意
