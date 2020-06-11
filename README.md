# README
## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false, index: ture|

### user association
- has_many :groups, through: :groups_users
- has_many :groups_users
- has_many :messages


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|groupname|integer|null: false, foreign_key: true|
|member|integer|null: false. oreign_key: true|

### groups association
- has_many :users, through: :groups_users
- has_many :groups_users
- has_many :messages

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|content|text||
|image|string||
|user|references|null: false, foreign_key: true|
|group|references|null: false, foreign_key: true|

### message associaton
- belongs_to :user
- has_many :group

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### groups_users association
- belongs_to :group
- belongs_to :user


