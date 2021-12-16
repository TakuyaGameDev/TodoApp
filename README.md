# TodoApp
laravel+vagrant+postgreSQL Linux基礎8-3

# 起動方法
URL検索欄に "192.168.33.10" と入力したらlogin画面に入ります。

サインアップ(新規登録)でご自分のメールアドレスと任意のパスワードを入力し、新規登録をし
login時にそのメールアドレスと新規登録時に入力したパスワードを入力してlogin完了です。

# パスワードリセットメール確認方法
login時に決めて頂いたメールアドレス宛にメールリセットのリンクが送信されます。
※login時には実際に送られるアドレスを入力してください。

.envファイルの設定

.envファイルの一部編集

MAIL_MAILER=smtp<br>
MAIL_HOST=smtp.mailtrap.io<br>
MAIL_PORT=2525<br>
MAIL_USERNAME=自分のUSERNAMEを入力<br>
MAIL_PASSWORD=自分のPASSWORDを入力<br>
MAIL_ENCRYPTION=null<br>
MAIL_FROM_ADDRESS=todoapp@email.com<br>
MAIL_FROM_NAME="ToDo App"<br>

MAIL_USERNAMEとMAIL_PASSWORDは<br>Mailtrapにログインし<br>My InBoxをクリック<br>この画面の<br>
![スクリーンショット 2021-12-16 142649](https://user-images.githubusercontent.com/87398533/146313850-a0c0774f-161e-4b14-8332-dba5aef0c651.png)<br>
"Show Credentials"をクリックし<br>こういう感じになるので<br>
![スクリーンショット 2021-12-16 142711_LI](https://user-images.githubusercontent.com/87398533/146314075-53708781-887e-43eb-b2ec-cfe2815f52d9.jpg)<br>
USERNAMEとPASSWORDのところのやつをそのまま.envの MAIL_USERNAMEとMAIL_PASSWORDに入力<br>
アプリに戻って再度パスワードリセット操作をすると、そこのIn MyBoxの中にパスワードリセットのリンクが書かれたメールが届いています。

#開発環境<br>
virtualBox,vagrant(仮想環境),php,postgreSQL(データベース)
