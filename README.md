# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

# DB設計

## usersテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false, unique: true, index: true|
|email|string|null: false, unique: true|
|age|	integer|null: false|
|introduction|texrt|null: false|

### Association
- has_many : posts

## foodsテーブル

|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|image|string|null: false|
|price|integer|null: false|
|introduction|text|null: false|

### Association
- has_many :users

## postsテーブル

|Column|Type|Options|
|------|----|-------|
|title|string|null: false|
|image|string|
|video|string|
|text|text|null: false|

### Association
- has_many :comments
- belongs_to :user

## commentsテーブル

|Column|Type|Options|
|------|----|-------|
|text|text|null: false|

### Association
- belongs_to :post

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
