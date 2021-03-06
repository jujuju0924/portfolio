# JAPONICAL

全国の知られていないお土産を投稿し、googlemap上で何県のお土産なのかがわかるサービスです。

[![Image from Gyazo](https://i.gyazo.com/12f9d51897ff4182af81738a16a28e7a.jpg)](https://gyazo.com/12f9d51897ff4182af81738a16a28e7a)

# URL
https://japonical.work/

非ログイン時は投稿データのみを見る事ができます。
簡単ログインのボタンを押す事でメールアドレスやユーザーネームを登録せずに投稿する事が可能です。

# 制作背景
前職で出張が多く、出張の際に寄った店舗の方と話をする機会が多々ありました。
その際にまだまだ個人商店や地方商店はネット化出来ていない店舗も多く、地方を経済活発にする為には一般客への認知が課題だと思いました。
認知の為にはWeb化が必須だと思いますが、Webが得意では無い方々にも気軽に投稿出来て地方誘致に繋げられるよう、本サービスを作成しました。
前職では社内で出張帰りのお土産を何にするか共有していた事もあり、その手間を省く側面もございます。
本アプリで地方を元気にしたいと考えて作成しました。

# 言語・使用技術

## フロント
* Haml
* Scss
* jQuery

## バックエンド
* Ruby 2.5.1
* Ruby on Rails 5.2.4

## サーバー
* Nginx 1.15.8

## DB
* MySQL 5.7

## インフラ・開発環境等
* Docker/docker-compose
* AWS（VPC,EC2,S3,RDS,ALB,ACM,Route53）
* RSpec

## 機能一覧
* ユーザー機能(devise使用）
* ユーザー新規登録
* ユーザーログイン・ログアウト機能
* 記事投稿、編集、削除機能
* 画像投稿機能(carrierwave)
* タグ機能(現段階では登録のみ、acts-as-taggable-on)
* コメント機能（Ajax）
* いいね 機能（Ajax）
* 検索機能
* ページネーション機能(kaminari)
* 住所&経度・緯度取得機能(geocoder)　　
* 地図表示機能(Maps JavaScript API) 

## アーキテクチャ図
[![Image from Gyazo](https://i.gyazo.com/e2b0dcff5e962ecf5991765d9a5ad8fe.png)](https://gyazo.com/e2b0dcff5e962ecf5991765d9a5ad8fe)

注　元々はEC2を２つ起動しておりましたが、一旦1つ起動にしております。
