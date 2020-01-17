# DataBaseDesignSample
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|email|string|null: false|
|password|string|null: false|
|nickname|string|null: false|
### Association
- has_many :groups_users, through:groups_users
- has_many :groups,


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|Type|Options|

|integer|null: false, foreign_key: true|
### Association
- belongs_to :users
- has_many :groups_users



groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user