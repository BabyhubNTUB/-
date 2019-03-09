| 目錄 |
| --- |
| [T01member會員資料](#T01member會員資料) |
| [T02 baby(寶寶資料)](#T02寶寶資料(baby)) |
| [T03 growingRecord(寶寶成長紀錄)](#T03寶寶成長紀錄growingRecord) |
| [T04 forum(討論區文章)](#T04討論區文章forum) |
| [T05 forumComment(討論區文章留言)](#T05forumComment(討論區文章留言)) |
| [T06 pregnancyKnowledge(孕期知識)](#T06pregnancyKnowledge(孕期知識)) |
| [T07 vaccination(接種清單)](#T07vaccination(接種清單)) |
| [T08 diary(日記)](#T08diary(日記)) |
| [T09 milestoneDone(里程碑完成)](#T09milestoneDone(里程碑完成)) |
| [T10 education(小孩教育)](#T10education(小孩教育)) |
| [T11 forumLike(文章喜歡)](#T11forumLike(文章喜歡)) |
| [T12 manager(管理者)](#T12manager(管理者)) |
| [T13 vaccine(疫苗清單)](#T13vaccine(疫苗清單)) |
| [T14 milestone(里程碑)](#T14milestone(里程碑)) |
| [T15 forumType(文章類別)](#T15forumType(文章類別)) |
| [T16 hospital(醫院)](#T16hospital(醫院)) |

## T01member會員資料
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

## T02baby(寶寶資料)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | babyNo | 寶寶編號 | P |  | int | 50 | AI |
| 2 | id | 會員帳號 | F |  | char | 50 | T01 |
| 3 | name | 寶寶名稱或姓名 |  |  | varchar | 50 | 可用綽號 |
| 4 | birthday | 生日 |  |  | date |  |  |
| 5 | gender | 性別 |  |  | enum |  | '男','女' |
| 6 | photo | 大頭貼 |  | v | varchar | 500 |  |

## T03growingRecord(寶寶成長紀錄)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | serNo | 流水號 | P |  | int | 50 | AI |
| 2 | babyNo | 寶寶編號 | F |  | int | 50 | T02 |
| 3 | recordDateTime | 紀錄日期時間 |  |  | datetime |  |  |
| 4 | height | 身長 |  | v | float | 6 | 50.34cm |
| 5 | weight | 體重 |  | v | float | 5 | 7.05kg |
| 6 | drinkMilk | 喝奶量 |  |  | int | 10 | c.c. |

## T04forum(討論區文章)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | forumNo | 文章流水號 | P |  | int | 50 | AI |
| 2 | typeNo | 文章類別編號 | F |  | int | 50 | T15 |
| 3 | id | 會員帳號 | F |  | char | 50 | T01 |
| 4 | forumname | 文章名稱 |  |  | varchar | 50 |  |
| 5 | forumDateTime | 發文日期時間 |  |  | datetime |  |  |
| 6 | content | 文章內容 |  |  | text |  | rich editor |

## T05forumComment(討論區文章留言)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | serNo | 流水號 | P |  | int | 50 | AI |
| 2 | forumNo | 文章流水號 | F |  | int | 50 | T04 |
| 3 | id | 會員帳號 | F |  | char | 50 | T01 |
| 4 | comDateTime | 留言日期時間 |  |  | detetime |  |  |
| 5 | content | 留言內容 |  |  | text |  |  |

## T06pregnancyKnowledge(孕期知識)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | serNo | 流水號 | P |  | int | 50 | AI |
| 2 | managerNo | 管理者帳號 | F |  | char | 20 | T12 |
| 3 | title | 標題 |  |  | vachar | 20 |  |
| 4 | content | 內容 |  |  | text |  |  |
| 5 | source | 出處 |  | v | varchar | 255 |  |

## T07vaccination(接種清單)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | serNo | 流水號 | P |  | int | 50 | AI |
| 2 | babyNo | 寶寶編號 | F |  | int | 50 | T02 |
| 3 | vacNo | 疫苗流水號 | F |  | int | 50 | T13 |
| 4 | hospitalNo | 接踵醫院 | F | v | int | 50 | T16 |
| 5 | vaccination | 是否接種 |  |  | enum |  | '已接種','未接種' |
| 6 | vacDate | 接種日期 |  | v | date |  |  |

## T08diary(日記)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | serNo | 流水號 | P |  | int | 50 | AI |
| 2 | babyNo | 寶寶編號 | F |  | int | 50 | T02 |
| 3 | id | 會員帳號 | F |  | char | 10 | T01 |
| 4 | diaryDate | 日期 |  |  | date |  |  |
| 5 | diary | 內容 |  |  | text |  | rich editor |
| 6 | dVideo | 影音檔 |  | v | vachar | 500 |  |

## T09milestoneDone(里程碑完成)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | serNo | 流水號 | P |  | int | 50 | AI |
| 2 | babyNo | 寶寶流水號 | F |  | int | 50 | T02 |
| 3 | msNo | 里程碑編號 | F |  | int | 50 | T14 |
| 4 | reach | 是否達成 |  |  | enum |  | '達成','未達成' |
| 5 | reachDate | 達成日期 |  | v | date |  |  |

## T10education(小孩教育)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | serNo | 流水號 | P |  | int | 50 | AI |
| 2 | managerNo | 管理者編號 | F |  | char | 20 | T12 |
| 3 | title | 標題 |  |  | vachar | 20 |  |
| 4 | content | 內容 |  |  | text |  |  |
| 5 | source | 出處 |  | v | varchar | 255 |  |

## T11forumLike(文章喜歡)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | serNo | 流水號 | P |  | int | 50 | AI |
| 2 | id | 會員帳號 | F |  | char | 50 | T01 |
| 3 | forumNo | 文章流水號 | F |  | int | 50 | T04 |

## T12manager(管理者)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | managerNo | 帳號 | P |  | char | 20 |  |
| 2 | password | 密碼 |  |  | varchar | 20 | 加密 |
| 3 | name | 姓名 |  |  | char | 10 |  |
| 4 | cellphone | 手機 |  |  | char | 10 |  |

## T13vaccine(疫苗清單)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | vacNo | 疫苗流水號 | P |  | int | 50 | AI |
| 2 | managerNo | 管理者帳號 | F |  | char | 20 | T12 |
| 3 | varname | 疫苗名稱 |  |  | varchar | 50 |  |
| 4 | varAge | 適合接種年齡 |  |  | int | 10 | 出生後幾天 |
| 5 | vacReaction | 接種後反應 |  |  | text |  |  |

## T14milestone(里程碑)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | msNo | 里程碑流水號 | P |  | int | 50 | AI |
| 2 | managerNo | 管理者帳號 | F |  | char | 20 | T12 |
| 3 | name |  | 里程碑名稱 |  | varchar | 20 |  |
| 4 | content |  | 內容 |  | text |  |  |
| 5 | mVideo |  | 影音檔 | v | varchar | 500 |  |

## T15forumType(文章類別)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | typeNo | 文章類別編號 | P |  | int | 50 | AI |
| 2 | managerNo | 管理者帳號 | F |  | char | 20 | T12 |
| 3 | name | 名稱 |  |  | varchar | 20 |  |

## T16hospital(醫院)
| | 欄位名稱(英) | 欄位名稱(中) | P/F | NULL | 資料型態 | 長度 | 說明 |
| ---  | ---  | --- | --- | --- | --- | --- | --- |
| 1 | hospitalNo | 醫院編號 | P |  | int | 50 | AI |
| 2 | name | 醫院名稱 |  |  | char | 20 | T12 |
| 3 | longitude | 經度 |  |  | float | 20 |  |
| 4 | latitude | 緯度 |  |  | float | 20 |  |
| 5 | address | 地址 |  |  | char | 50 |  |
| 6 | phone | 電話 |  |  | char | 10 |  |
