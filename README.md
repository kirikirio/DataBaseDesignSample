# chat-space DB設計
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|username|string|null: false|
### Association
- has_many :posts
- belongs_to :group

## postsテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|null: false|
|image|text||
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- belongs_to :post
## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|username|string|null: false|
|group_name|string|null: false|
### Association
- has_many :users
- has_many :posts
