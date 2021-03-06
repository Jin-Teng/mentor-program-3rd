# 作業

## API 文件

Base URL: https://lidemy-book-store.herokuapp.com

| 說明     | Method | path       | 參數                   | 範例             |
|--------|--------|------------|----------------------|----------------|
| 獲取所有書籍 | GET    | /books     | _limit:限制回傳資料數量           | /books?_limit=5 |
| 獲取單一書籍 | GET    | /books/:id | 無                    | /books/10      |
| 新增書籍   | POST   | /books     | name: 書名 | 無              |
| 刪除書籍   | DELETE   | /books/:id     | 無 | 無              |
| 更改書籍資訊   | PATCH   | /books/:id     | name: 書名 | 無              |


## hw1：來自秋秋鞋的任務

有一天，住你隔壁的鄰居秋秋鞋跑來按門鈴，說有事想要找你討論，他最近在做一個知識型的 YouTube 頻道，可是快要沒有靈感了。

這時，他想到一個好主意！他只要能夠看到書店提供的書籍相關資訊，就可以從中汲取靈感，之後就可以發想相關題材，頻道就不會一直不更新了。

身為秋秋鞋的好朋友，這個重責大任當然就交給你了！

請閱讀開頭給的 API 文件並串接，用 node.js 寫出一個程式，執行後會在 console 列出前十本書籍的 id 以及書名。

順帶一提，叫做秋秋鞋是因為他很喜歡秋天。

範例：

``` js
node hw1.js

1 克雷的橋
2 當我想你時，全世界都救不了我
3 我殺的人與殺我的人
....
```

## hw2：不滿足的秋秋鞋

雖然說上次你幫秋秋鞋完成了列出書籍清單的程式，但是一次列出十本實在是太少了，大概一個禮拜就可以把這些資訊消化完，但是經營頻道卻是長期的事情，他需要更多更多的資料才行。例如說一次應該要輸出二十本書，然後可以輸入一個 id 就返回書籍資料，這樣他就可以隨便想一個數字，然後看看是哪本書，對於靈感很有幫助。

請你閱讀開頭給的 API 文件並串接，用 node.js 寫出一個程式並接受參數，輸出相對應的結果，範例如下：

``` js
node hw2.js list // 印出前二十本書的 id 與書名
node hw2.js read 1 // 輸出 id 為 1 的書籍資料
```

## hw3：最後的考驗

原本以為上次就已經是最後一次幫忙，沒想到秋秋鞋還是又跑來找你了。他說他想要更多功能，他想把這整個書籍資料庫當作自己的來用，必須能夠刪除、新增以及修改書本，這樣他就可以管理自己的書籍了。

雖然你很想問他說為什麼不用 Excel 就好，但你問不出口，再加上你最近剛學成是需要練習的機會，於是你就答應了。

請閱讀開頭給的 API 文件並串接，用 node.js 寫出一個程式並接受參數，輸出相對應的結果，範例如下：

``` js
node hw3.js list // 印出前二十本書的 id 與書名
node hw3.js read 1 // 輸出 id 為 1 的書籍
node hw3.js delete 1 // 刪除 id 為 1 的書籍
node hw3.js create "I love coding" // 新增一本名為 I love coding 的書
node hw3.js update 1 "new name" // 更新 id 為 1 的書名為 new name
```

## hw4：探索新世界

上次幫秋秋鞋做完那個小程式以後，你會寫程式的消息似乎就傳開了，有一位 Twitch 平台實況主果凍跑來聯繫你，想請你幫忙做個東西。

事情是這樣的，他原本是 LOL 的玩家，但因為某些原因帳號被 ban 掉了，為了維持實況的熱度，需要去找其他遊戲來玩，可是他又不知道哪些遊戲比較熱門，會有比較多人觀看。

因此，他寫請你寫一個小程式，能夠去撈取 Twitch 上面受歡迎的遊戲，他就能夠參考這個列表來決定要實況哪個遊戲。

由於你偶爾也會看他的實況，所以你欣然接受了這個挑戰，準備來串串看真實世界的 API。

請參考 [Twitch API](https://dev.twitch.tv/docs/api/) 的文件，寫一隻程式去呼叫 Twitch API，並拿到「最受歡迎的遊戲列表（Get Top Games）」然後依序印出 id 跟遊戲名稱。

``` js
node hw4.js

21779 League of Legends
29595 Dota2
511224 Apex Legends
33214 Fortnite
....
```

## hw5：簡答題

請將答案寫在 [hw5.md](hw5.md)。

1. 請以自己的話解釋 API 是什麼？
2. 請找出三個課程沒教的 HTTP status code 並簡單介紹
3. 假設你現在是個餐廳平台，需要提供 API 給別人串接並提供基本的 CRUD 功能，包括：回傳所有餐廳資料、回傳單一餐廳資料、刪除餐廳、新增餐廳、更改餐廳，你的 API 會長什麼樣子？請提供一份 API 文件。

## 挑戰題

寫一個 node.js 的程式並串接 Twitch API，輸出遊戲「League of Legends」底下最受歡迎的前 200 個實況的名稱與 id。

## 超級挑戰題

寫一個 node.js 的程式並串接 Twitch API，接收一個參數是遊戲名稱，輸出那個遊戲底下最受歡迎的前 200 個實況的名稱與 id。

``` js
// 範例
node twitch.js "Apex Legends"
```

