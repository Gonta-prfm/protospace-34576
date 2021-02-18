# テーブル設計

## users テーブル

| Clumn      | Type   | Option     |
| name       | string | null false |
| email      | string | null false |
| password   | string | null false |
| profile    | text   | null false |
| occupation | text   | null false |
| position   | text   | null false |

### Association

- has_many :prototyoes
- has_many :comments

## prototypes テーブル

| Culumn     | Type       | Option                        |
| title      | string     | null false                    |
| catch_copy | text       | null false                    |
| concept    | text       | null false                    |
| user       | references | null: false, foreign_key: true|

### Association

- has_many :comments
- belongs_to :user

## comments テーブル

| Culumn    | Type       | Option                         |
| text      | text       | null false                     |
| user      | references | null: false, foreign_key: true |
| prototype | references | null: false, foreign_key: true |

### Association

- belongs_to :user
- belongs_to :prototype


