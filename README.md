# git-practice
Git練習用のリポジトリです

## 前提
- Windowsでも利用は可能ですが、基本的にMac前提です

## Git環境の構築

### Gitのインストール有無を確認する

- ターミナルを起動する
- Gitバージョン確認コマンドを実行する
```
$ git --version
```
- 以下のようにバージョンが表示されればインストール済みです
```
git version x.xx.x
```
- gitが見つからない場合は次のステップでGitのインストールを行なってください

### Gitをインストールする（Mac）

- Brew経由でGitをインストールする
```
$ brew update
$ brew install git
```
- Gitバージョン確認コマンドを実行する
```
$ git --version
```

### Gitの初期設定

Gitのグローバル設定に名前とメールアドレスを登録します。
こちらを設定することでコミット時に誰がコミットを行なったか分かるようになります。

- ユーザー名を設定する
```
$ git config --global user.name "xxxxxx"
```

- メールアドレスを設定する
```
$ git config --global user.email "xxx@xxx.co.jp"
```

## GitHubを使ってみよう

### GitHubアカウントを作成する

開発者として、自分のGitHubアカウントを持っていた方が今後役立つと思いますので、GitHubアカウントを取得しましょう。
GitHubのFreeプランで問題ありません。

- GitHubとは？
  - GitリポジトリをホスティングできるWebサービス
  - Gitの機能に加え、他プロジェクトのフォークやプルリク、ISSUEトラッキング、Wikiなど、ソフトウェア開発に必要な機能を多数持っている

- GitHubにアクセスする
  - https://github.com/

- 新規登録フォームに名前、メールアドレス、パスワードを入力し、登録してください

- 「Free」プランを選択してください

- 登録が完了すると、Githubから認証メールが届くので、メール内のURLをクリックすることで、作成完了です


### 最初のリモートリポジトリを作成する

- 自分のGitHubページの右上の「＋」をクリックし「New repository」を選択する
- Repository nameにリポジトリ名を入力する(例:test)
- Descriptionにリポジトリの説明を入力する(任意)
- Publicを選択する
- Create repositoryをクリックする

### ローカルリポジトリを作成する

- 自分のPCの任意の場所にディレクトリを作成する
```
$ mkdir test
$ cd test
```

- Git管理の初期設定を行う
```
$ git init
```

- リモートリポジトリを設定する
URL部分は自分の作ったリポジトリのURLを設定してください
```
$ git remote add origin https://github.com/xxxx/test.git
```

### ローカルリポジトリにファイルをコミットする

- ファイルを作成する
vimなどでファイルの内容は自由に変更してください
```
$ touch test.txt
```

- ファイルをGit管理に加える
```
$ git add test.txt
```

- コミットする
```
$ git commit -m "はじめてのコミット"
```

### リモートリポジトリに変更をプッシュする

- 以下のコマンドを実行する
```
$ git push origin master
```

- GitHubの画面でtest.txtが追加されていることを確認する