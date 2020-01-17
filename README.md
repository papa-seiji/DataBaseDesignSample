# DataBaseDesignSample
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|id|integer|null: false|
|email|string|null: false|
|password|string|null: false|
|nickname|string|null: false|
### Association
- has_many :groups_users
- has_many :groups, through:groups_users
- has_many :messages


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
### Association

- has_many :groups_users
- has_many :users,through:groups_users
- has_many :messages



groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|refarences|null: false, foreign_key: true|
|group_id|refarences|null: false, foreign_key: true|

### Association
- has_many :users
- has_many :group

## messageテーブル
|Column|Type|Options|
|------|----|-------|
|text|string|null: false|
|image|string|null: false|
|user_id|refarences|null: false, foreign_key: true|
|group_id|refarences|null: false, foreign_key: true|
### Association

- belongs_to :group
- belongs_to:users
- 