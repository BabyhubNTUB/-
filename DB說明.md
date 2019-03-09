| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |  |
[](#)

| 目錄 |
| --- |
| [T01會員資料member](#T01會員資料member) |
| [T02寶寶資料baby](#T02寶寶資料baby) |
| [T03寶寶成長紀錄growingRecord](#T03寶寶成長紀錄growingRecord) |
| [T04討論區文章forum](#T04討論區文章forum) |

## T01會員資料member
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | id | 會員帳號 | P |  | char | 50 | mail |
| 2 | displayName | 會員名稱或姓名 |  |  | char | 50 | 可用綽號 |
| 3 | password | 會員密碼 |  |  | varchar | 20 | 加密 |
| 4 | appellation | 稱謂 |  |  | varchar |  | '爸爸','媽媽'' |
| 5 | lineId | 會員LineID |  |  | enum | 50 |  |
| 6 | code | 驗證碼 |  | v | char | 6 |  |
| 7 | codeTime | 驗證碼有效時間 |  | v | time |  |  |
| 8 | photo | 大頭貼 |  | v | varchar | 500 |  |

## T02寶寶資料baby
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | babyNo | 寶寶編號 | P |  | int | 50 | AI |
| 2 | id | 會員帳號 | F |  | char | 50 | T01 |
| 3 | name | 寶寶名稱或姓名 |  |  | varchar | 50 | 可用綽號 |
| 4 | birthday | 生日 |  |  | date |  |  |
| 5 | gender | 性別 |  |  | enum |  | '男','女' |
| 6 | photo | 大頭貼 |  | v | varchar | 500 |  |

## T03寶寶成長紀錄growingRecord
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | serNo | 流水號 | P |  | int | 50 | AI |
| 2 | babyNo | 寶寶編號 | F |  | int | 50 | T02 |
| 3 | recordDateTime | 紀錄日期時間 |  |  | datetime |  |  |
| 4 | height | 身長 |  | v | float | 6 | 50.34cm |
| 5 | weight | 體重 |  | v | float | 5 | 7.05kg |
| 6 | drinkMilk | 喝奶量 |  |  | int | 10 | c.c. |

## T04討論區文章forum
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | forumNo | 文章流水號 | P |  | int | 50 | AI |
| 2 | typeNo | 文章類別編號 | F |  | int | 50 | T15 |
| 3 | id | 會員帳號 | F |  | char | 50 | T01 |
| 4 | forumname | 文章名稱 |  |  | varchar | 50 |  |
| 5 | forumDateTime | 發文日期時間 |  |  | datetime |  |  |
| 6 | content | 文章內容 |  |  | text |  | rich editor |
