# middleware-app-practice

## 概要
COACHTECH 教材 Tutorial 10-2「ミドルウェア ハンズオン演習」で作成した成果物です。カスタムミドルウェアを使って、管理者のみアクセスできる「管理者専用ページ」を保護しました。

## 使用技術
- PHP 8.x
- Laravel 10.x
- カスタムミドルウェア
- Laravel Fortify（認証）

## 学んだこと
- sail artisan make:middleware でのミドルウェア作成と Kernel.php での登録
- ルートへのミドルウェア適用方法（->middleware('check_admin')）

## 動作確認
管理者、一般ユーザーのそれぞれでアクセスして確認する必要があります。
1．管理者でログイン
ブラウザで http://localhost にアクセスし、admin@example.com / password でログインします。その後、「管理者ページにアクセス」をクリックします。管理者ページが表示されれば成功です。

2．一般ユーザーでログイン
まず、ログアウトを行います。user@example.com / password でログインし、「管理者ページにアクセス」をクリックします。403エラーが表示されれば成功です。
