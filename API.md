## 會員資料member
~~~node.js
描述：用於登入
路徑：member/add
HTTP方法：POST
reguest 請求：
  {
    "id":"帳號/信箱",
    "password":"密碼",
    "code":"驗證碼"
  }
response 回傳：
  {
    ture|false
  }
~~~

~~~
名稱：member/del
方法：delete
input
{id,password}
return
ture|false
~~~

~~~
名稱：member/update
方法：put
input
{displayName,password}
return
ture|false
~~~

~~~
名稱：member/query
方法：get
input
{id}
return
{id,displayName,appellation,lineId}|false
~~~

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
