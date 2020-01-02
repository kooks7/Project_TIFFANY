## 1. PROJECT NAME

TIFFANY (본인 인증 서비스)

## 2. DETAIL SKILLS

web : EJS

server : Node.js

![Node.js logo.svg](https://upload.wikimedia.org/wikipedia/commons/thumb/d/d9/Node.js_logo.svg/220px-Node.js_logo.svg.png)

, FileUpload

## 3. 설계 구성도

|            | 김민재 X 최재성 Project |             |                        |             |
| ---------- | ----------------------- | ----------- | ---------------------- | ----------- |
|            | url                     | http method | biz JS                 | View / Data |
| 메인페이지 | /                       | get         | ./routes/index         |             |
| 로그인     | /login                  | post        | ./routes/login         |             |
| 로그아웃   | /logout                 | get         | ./routes/logout        |             |
| 회원가입   | /member_insert          | post        | ./routes/member_insert |             |
| 사진올리기 | /photo_insert           | post        | ./routes/photo_insert  |             |
|            | /upload                 | post        | app.js에 직접구현      |             |
| 수정       | /modify                 | post        | ./routes/modify        |             |
| 탈퇴       | /member_deleter         | get         | ./routes/member_delete |             |

|            | INDEX.ejs    |              |          |           |               |         |            |
| ---------- | ------------ | ------------ | -------- | --------- | ------------- | ------- | ---------- |
|            | PAGE_NAME    | INPUT        | TYPE     | id        | name          | Button  | btn_id     |
| #login     | LOGIN        | ID           | text     | login_id  | login_id      |         |            |
|            |              | PASSWORD     | password | login_pwd | login_pwd     | Login   | login_btn  |
| #signup    | SIGN UP      | ID           | text     | id        | id            |         |            |
|            |              | NAME         | text     | name      | name          |         |            |
|            |              | PASSWORD     | password | password  | password      |         |            |
|            |              | NAME         | text     | name      | name          |         |            |
|            |              | PHONE        | tel      | phone     | phone         |         |            |
|            |              | IDENTITY_NUM | text     | id_num    | id_num        |         |            |
|            |              | Email        | email    | email     | email         |         |            |
|            |              | ADDRESS      | textarea | address   | address       | Sign up | signup_btn |
| #logout    | LOGOUT       |              |          |           |               | LOGOUT  | logout_btn |
| #id_update | PHOTO UPDATE | PHOTO_FILE   | file     | id_photo  | id_photo_name | UPLOAD  | photo_btn  |

## 4. DB

| DB(MySQL)    |              |      |             |         |                |
| ------------ | ------------ | ---- | ----------- | ------- | -------------- |
| FIELD        | TYPE         | NULL | KEY         | DEFAULT | EXTRA          |
| mem_id       | int(100)     | No   | Primary key | NULL    | auto_increment |
| ID           | varchar(50)  | YES  |             | NULL    |                |
| NAME         | varchar(50)  | YES  |             | NULL    |                |
| PASSWORD     | varchar(50)  | YES  |             | NULL    |                |
| IDENTITY_NUM | varchar(50)  | YES  |             | NULL    |                |
| PHONE        | varchar(50)  | YES  |             | NULL    |                |
| ADDRESS      | varchar(255) | YES  |             | NULL    |                |
| EMAIL        | varchar(100) | YES  |             | NULL    |                |
| PHOTO_PATH   | varchar(255) | YES  |             | NULL    |                |