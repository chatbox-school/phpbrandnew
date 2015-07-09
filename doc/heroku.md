# heroku の使い方

https://www.heroku.com/

新しい料金体系の紹介はこちらから

https://www.heroku.com/pricing

PHP アプリケーションの作り方

https://devcenter.heroku.com/articles/getting-started-with-php#introduction

1. アカウントの作成
2. heroku toolbelt のインストール https://toolbelt.heroku.com/
3. heroku 画面から新規アプリケーションを作成。
4. deployのタブを参考にgitのリモートに追加。
5. composer initを実行してcomposer.jsonを作成
6. Procfile を作成して以下のコードを記述


````
web: vendor/bin/heroku-php-apache2 web/
````

7. 以下のコマンドでデプロイ用のファイルをcomposerに追加

````
composer require heroku/heroku-buildpack-php:*
````

