<h1>Laravelで開発を行うための流れ</h1>

<h2>Section 0</h2>

xamppや、MAMP等ローカル開発環境をインストールし、DBを立ち上げる<br>

composer のインストール　https://getcomposer.org/<br>

laravel インストール laravel version 6 install command ⇒ composer create-project "laravel/laravel 6.*" --prefer-dist "プロジェクト名"<br>

version指定しない場合は最新版がインストールされる


<h2>Section 1</h2>

<h3>.envファイルの初期設定</h3>

<b>ディレクトリ位置</b> /laravelproject/.env　

.envファイルは開発するアプリ名や、データーベースの接続情報等を記述するファイルです。

DB_CONNECTION=mysql<br>
DB_HOST=127.0.0.1<br>
DB_PORT=3306<br>
DB_DATABASE=laravel<br>
DB_USERNAME=root<br>
DB_PASSWORD=<br>

初期設定ではこうなっていると思いますが、まずはDB_DATABASE=laravel　のlaravelの部分がデーターベースの名前（テーブルではない）<br>
を作成済み/作成するデーターベースの名前と合わせるようにしましょう。<br>
Windows兼xammpユーザーの方だと、DBのUSERNAME=root やPASSWORD=""はデフォルトで設定されていると思いますので変更の必要はありません。<br>

<h3>configディレクトリのapp.phpの初期設定</h3>
<b>ディレクトリ位置</b> /Laravel-project/config/app.php
初期設定が必要な項目が3つほどあります。

1. app.phpの42行目 "debug" と書かれた行にfalseと記載がありますが、trueに変更しておきます。
2. app.phpの70行目 "timezone" と書かれた行にUTCと記載がありますが、Asia/Tokyoに変更しておきます。
3. app.phpの83行目 "locale" と書かれた行にenと記載がありますが、jaに変更しておきます。


<h2>Section 2</h2>
<h3></h3>
