# README

# chat-SPACE DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|nickname|string|null: false|
### Association
- has_many :posts
- belongs_to :group

## postsテーブル
|Column|Type|Options|
|------|----|-------|
|image|text||
|text|text|null: false|
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- belongs_to :group


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group_name|text|null: false|
|user_id|integer|null: false, foreign_key: true|
### Association
- has_many :posts
- has_many :users

## how to use GitHub Desktop