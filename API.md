~~~java
描述：
路徑：
方法：POST,DELETE,PUT,GET
request 請求：
  {
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~
## 會員資料member
~~~java
描述：新增會員資料
路徑：/member/add
方法：POST
request 請求：
  {
    id:"帳號(信箱)",
    displayName:"名稱/姓名",
    password:"密碼",
    appellation:"稱謂"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"帳號創建成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"此帳號已存在"
  }
~~~

~~~java
描述：刪除會員資料
路徑：/member/del
方法：DELETE
request 請求：
  {
    id:"帳號(信箱)",
    password:"密碼",
  }
response 回傳(成功)：
  {
    code:"0"
    message:"帳號刪除成功"
  }
===
response 回傳(失敗)：
  {
    code:"-1"
    message:"帳號刪除失敗(密碼錯誤)"
  }
~~~

~~~java
描述：更新會員資料
名稱：/member/update
方法：PUT
request 請求：
  {
    id:"帳號(信箱)",
    displayName:"名稱/姓名",
    password:"密碼",
    photo: "大頭貼"
  }
response 回傳(成功)：
  {
    code:"0"
    message:"更新成功"
  }
===
response 回傳(失敗)：
  {
    code:"-1"
    message:"更新失敗"
  }
~~~

~~~java
描述：查詢會員資料
名稱：/member/query
方法：GET
request 請求：
  {
    id:"帳號(信箱)"
  }
response 回傳(成功)：
  {
    id:"帳號/信箱",
    displayName:"會員名稱",
    appellation:"稱謂",
    lineId:"LINEID",
    photo: "大頭貼"
    code:"0"
  }
===
response 回傳(失敗)：
  {
    code:"-1"
  }
~~~


======================================


## 寶寶資料baby
~~~java
描述：新增寶寶資料
名稱：/baby/add
方法：POST
request 請求：
  {
    babyNo:"寶寶編號",
    id:"帳號(信箱)",
    name:"寶寶名字",
    birthday:"寶寶生日",
    gender:"寶寶性別",
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"新增寶寶成功"
  }
===
response 回傳(失敗)：
  {
    code:"-1"
    message:"無法新增"
  }
~~~

~~~java
描述：刪除寶寶資料
路徑：/baby/del
方法：DELETE
request 請求：
  {
    id:"會員帳號(信箱)",
    babyNo:"寶寶編號"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~

~~~java
描述：查詢寶寶資料
路徑：/baby/query
方法：GET
request 請求：
  {    
    id:"會員帳號(信箱)",
    babyNo:"寶寶編號"
  }
===
response 回傳(成功)：
  {
    code:"0",
    babyNo:"寶寶編號",
    id:"帳號(信箱)",
    name:"寶寶名字",
    birthday:"寶寶生日",
    gender:"寶寶性別"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"沒有找到"
  }
~~~


======================================


## 成長紀錄growingRecord
~~~java
描述：新增成長紀錄
路徑：/growingRecord/add
方法：POST
request 請求：
  {
    serNo:"成長紀錄編號",
    babyNo:"寶寶編號",
    recordDateTime:"紀錄日期時間",
    height:"身高",
    weight:"體重",
    drinkMilk:"喝奶量"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"新增成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"新增失敗"
  }
~~~

~~~java
描述：刪除成長紀錄
路徑：/growingRecord/del
方法：DELETE
request 請求：
  {
    babyNo:"寶寶編號",
    recordDateTime:"紀錄日期時間"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"刪除成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"刪除失敗"
  }
~~~

~~~java
描述：更改寶寶成長紀錄
路徑：/growingRecord/update
方法：PUT
request 請求：
  {
    height:"身高",
    weight:"體重",
    drinkMilk:"喝奶量"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~

~~~java
描述：查詢成長紀錄
路徑：/growingRecord/query
方法：GET
request 請求：
  {
    babyNo:"寶寶編號",
    recordDateTime:"紀錄日期時間"
  }
===
response 回傳(成功)：
  {
    code:"0"
    serNo:"成長紀錄編號",
    babyNo:"寶寶編號",
    recordDateTime:"紀錄日期時間",
    height:"身高",
    weight:"體重",
    drinkMilk:"喝奶量"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~


======================================


## 討論區文章forum
~~~java
描述：新增文章
路徑：/forum/add
方法：POST
request 請求：
  {
    forumNo:"文章編號",
    typeNo:"文章類別",
    id:"會員帳號(信箱)",
    forumName:"文章名稱",
    forumDateTime:"發文日期時間",
    content:"文章內容"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~

~~~java
描述：刪除文章
路徑：/forum/del
方法：DELETE
request 請求：
  {
    forumNo:"文章編號"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~

~~~java
描述：更新文章
路徑：/forum/update
方法：PUT
request 請求：
  {    
    forumNo:"文章編號",
    typeNo:"文章類別",
    forumName:"文章名稱",
    content:"文章內容"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~
~~~
名稱：
方法：put
input
return
ture|false
~~~

~~~java
描述：查詢文章
路徑：/forum/query
方法：GET
request 請求：
  {
  }
===
response 回傳(成功)：
  {
    code:"0"
    forumNo:"文章編號",
    typeNo:"文章類別",
    id:"會員帳號(信箱)",
    forumName:"文章名稱",
    forumDateTime:"發文日期時間",
    content:"文章內容"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~


======================================


## 討論區文章留言forumComment
~~~java
描述：新增討論區留言
路徑：/forumComment/add
方法：POST
request 請求：
  {
    serNo:"留言編號",
    forumNo:"文章編號",
    id:"諱言帳號(信箱)",
    comDateTime:"留言日期時間",
    content:"留言內容"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~

~~~java
描述：刪除討論區留言
路徑：/forumComment/del
方法：DELETE
request 請求：
  {
    serNo:"留言編號"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~

~~~java
描述：更改討論區留言
路徑：/forumComment/update
方法：PUT
request 請求：
  {
    serNo:"留言編號",
    content:"留言內容"
  }
===
response 回傳(成功)：
  {
    code:"0"
    message:"成功"
  }
===
response 回傳(失敗)：
  { 
     code:"-1"
     message:"失敗"
  }
~~~

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

|First H | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
