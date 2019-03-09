

| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |  |


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
