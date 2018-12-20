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
路徑：/member/delete
方法：DELETE
request 請求：
  {
    id:"帳號(信箱)",
    password:"密碼",
  }
response 回傳(成功)：
  {
    code:"0"
  }
===
response 回傳(失敗)：
  {
    code:"-1"
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
  }
===
response 回傳(失敗)：
  {
    code:"-1"
    message:"更新失敗"
  }
~~~

~~~java
描述:查詢會員資料
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
  {  }
~~~


======================================


## 寶寶資料baby
~~~
名稱：baby/add
方法：post
input
{babyNo,id,name,birthday,gender}
return
ture|false
~~~

~~~
名稱：baby/del
方法：delete
input
{name,password}
return
ture|false
~~~

~~~
名稱：baby/query
方法：get
input
{name}
Return
{babyNo,id,name,birthday,gender}|false
~~~


## 成長紀錄growingRecord
~~~
名稱：growingRecord/add
方法：post
input
{serNo,babyNo,recordDateTime,height,weight,drinkMilk}
return
ture|false
~~~

~~~
名稱：growingRecord/del
方法：delete
input
{babyNo,recordDateTime}
return
ture|false
~~~

~~~
名稱：growingRecord/update
方法：put
input
{height,weight,drinkMilk}
return
ture|false
~~~

~~~
名稱：growingRecord/query
方法：get
input
{babyNo,recordDateTime}
return
{serNo,babyNo,recordDateTime,height,weight,drinkMilk}|false
~~~


## 討論區文章forum
~~~
名稱：forum/add
方法：post
input
{forumNo,typeNo,id,forumName,forumDateTime,content}
return
ture|false
~~~

~~~
名稱：forum/del
方法：delete
input
{forumNo}
return
ture|false
~~~

~~~
名稱：forum/update
方法：put
input
{forumName}|{content}
return
ture|false
~~~

~~~
名稱：forum/query
方法：get
input
{forumNo}|{forumName}
return
{forumNo,typeNo,id,forumName,forumDateTime,content}|false
~~~


## 討論區文章留言forumComment
~~~
名稱：forumComment/add
方法：post
input
{serNo,forumNo,id,comDateTime,content}
return
ture|false
~~~

~~~
名稱：forumComment/del
方法：delete
input
{serNo}
return
ture|false
~~~

~~~
名稱：forumComment/update
方法：put
input
{content}
return
ture|false
~~~

First Header  | Second Header
------------- | -------------
Content Cell  | Content Cell
Content Cell  | Content Cell

| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
