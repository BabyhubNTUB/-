##會員資料member
~~~
名稱：member/add
方法：post
input
{Id,displayName,password,appellation}
return
ture|false
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
{result:’success’}
{result:’fail’}
~~~

~~~
名稱：member/query
方法：get
input
{id}
return
{id,displayName,appellation,lineId}|{false}
~~~

##寶寶資料baby
~~~
名稱：baby/add
方法：post
input
{babyNo,id,name,birthday,gender}
return
{result:’success’}
{result:’fail’}
~~~

~~~
名稱：baby/del
方法：delete
input
{name,password}
return
{result:’success’}
{result:’fail’}
~~~

~~~
名稱：baby/query
方法：get
input
{name}
Return
{babyNo,id,name,birthday,gender}
{result:’fail’}
~~~


##成長紀錄growingRecord
~~~
名稱：growingRecord/add
方法：post
input
{serNo,babyNo,recordDateTime,height,weight,drinkMilk}
return
{result:’success’}
{result:’fail’}
~~~

~~~
名稱：growingRecord/del
方法：delete
input
{babyNo,recordDateTime}
return
{result:’success’}
{result:’fail’}
~~~

~~~
名稱：growingRecord/update
方法：put
input
{height,weight,drinkMilk}
return
{result:’success’}
{result:’fail’}
~~~

~~~
名稱：growingRecord/query
方法：get
input
{babyNo,recordDateTime}
return
{serNo,babyNo,recordDateTime,height,weight,drinkMilk}
~~~





| First Header  | Second Header |
| ------------- | ------------- |
| Content Cell  | Content Cell  |
| Content Cell  | Content Cell  |
