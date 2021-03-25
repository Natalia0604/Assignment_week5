# Assignment_week5_MYSQL
## 要求三
## 1.使用 INSERT 指令新增一筆資料到 user 資料表中,這筆資料的 username 和password 欄位必須是 ply。接著繼續新增至少 4 筆隨意的資料。
### SQL 指令: INSERT INTO user(name,username,password) VALUES('papaya','pa','pap');
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/%E6%96%B0%E5%A2%9E%E8%B3%87%E6%96%99.png)

## 2.使用 SELECT 指令取得所有在 user 資料表中的使用者資料。
### SQL 指令: SELECT * FROM user;
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/%E6%96%B0%E5%A2%9E10%E7%AD%86%E8%B3%87%E6%96%99.png)

## 3.使用 SELECT 指令取得 user 資料表中總共有幾筆資料。
### SQL 指令:SELECT count(*) FROM user;
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/user%E6%9C%89%E5%B9%BE%E7%AD%86%E8%B3%87%E6%96%99.png)

## 4.使用 SELECT 指令取得所有在 user 資料表中的使用者資料,並按照 time 欄位,由近到遠排序。
### SQL 指令: SELECT * FROM user ORDER BY time DESC;
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/time%20%E8%BF%91%E5%88%B0%E9%81%A0%E6%8E%92%E5%BA%8F.png)

## 5.使用 SELECT 指令取得 user 資料表中第 2 ~ 4 共三筆資料,並按照 time 欄位,由近到遠排序。
### SQL 指令: SELECT * FROM user ORDER BY time DESC LIMIT 1,3;
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/time2to4.png)

## 6.使用 SELECT 指令取得欄位 username 是 ply 的使用者資料。
### SQL 指令: SELECT * FROM user WHERE username='ply';
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/username_ply.png)

## 7.使用 SELECT 指令取得欄位 username 是 ply、且欄位 password 也是 ply 的資料。
### SQL 指令:SELECT＊　FROM user WHERE (usename='ply' AND password='ply');
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/usernameply_passwordply.png)

## 8.使用 UPDATE 指令更新欄位 username 是 ply 的使用者資料,將資料中的 name 欄位改成【丁滿】。
### SQL 指令:UPDATE user set name='丁滿' WHERE ='ply';
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/%E4%B8%81%E6%BB%BF.png)

## 9.使用 DELETE 指令刪除所有在 user 資料表中的資料。
### SQL 指令: delete from user;
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/old/%E5%88%AA%E9%99%A4%E6%89%80%E6%9C%89%E8%B3%87%E6%96%99.png)
## 要求四
## 10.使用 SELECT 搭配 JOIN 的語法,取得所有留言,資料中須包含留言會員的姓名。
### SQL 指令:SELECT user.name, message.content FROM user INNER JOIN message ON message.user_id = user.id;
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/%E5%8F%96%E5%BE%97%E6%89%80%E6%9C%89%E6%9C%83%E5%93%A1%E5%A7%93%E5%90%8D%E5%8F%8A%E7%95%99%E8%A8%80%E5%85%A7%E5%AE%B9.png)

## 11.使用 SELECT 搭配 JOIN 的語法,取得 user 資料表中欄位 username 是 ply 的所有留言,資料中須包含留言會員的姓名。
### SQL 指令: SELECT user.name, user.username, message.content FROM user INNER JOIN message ON (message.user_id =1)&(user.id=1);
![image](https://github.com/Natalia0604/Assignment_week5/blob/main/week5/join_username_ply.png)
