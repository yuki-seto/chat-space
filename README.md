#database
====

## user

|column|type|
|:--:|:--:|
|name|string|
|e_mail|string |
|password|string|
>所属しているグループ情報はgroup_userを経由してchat_groupから引っ張る

## message

|column|type|
|:--:|:--:|
|body|text|
|image|string|
|group_id|integer|
|user_id|integer|

## group

|column|type|
|:--:|:--:|
|name|string|
>所属しているユーザ情報はgroup_userを経由してuserから引っ張る

## group_user

|column|type|
|:--:|:--:|
|user_id|integer|
|group_id|integer|
>ユーザとチャットグループが多対多の関係であるため中間テーブルを設ける
