# README
## userテーブル

|Column|Type|Options|
|------|----|-------|
|id|integer|null: false, |
|nickname|integer|null: false, |
|email|integer|null: false, |
|possword|integer|null: false, |

### user association
- has_many :group, through: :groups_users
- has_many :groups_user
- belongs_to :message


## groupテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|groupname|integer|null: false, foreign_key: true|
|member|integer|null: false. oreign_key: true|

### groups association
- has_many :user, through: :groups_users
- has_many :groups_users
- belongs_to :message

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|body|integer|null: false, foreign_key: true|
|image|string|null: false. oreign_key: true|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### message associaton
- has_many :user
- has_many :group

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### groups_users association
- belongs_to :group
- belongs_to :user
- belongs_to :message


This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
