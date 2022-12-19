# Redmine用テーマ "farend basic customized"

## このテーマについて

下記のテーマを元に個人的にカスタマイズしたものです。
https://github.com/farend/redmine_theme_farend_basic

> Redmine用のカスタムテーマです。日本語環境で見やすい画面を実現することを目的に、Redmine付属のデフォルトテーマを元に作成したものです。
> farend basicテーマの主な特徴は以下の通りです。
>
> * 日本語フォントを優先して使用するよう設定を行いました。これにより、￥記号がバックスラッシュとして表示されていた問題が解決します（WindowsおよびメイリオがインストールされているMacのみ）
> * メイリオフォントがインストールされている環境ではメイリオを使って文字が表示されますので、画面上の文字が読みやすくなります。
> * 文字と背景のコントラストを高めて読みやすくするために、文字の色を全体的に見直しました。
> * チケット一覧画面において優先度に対応した色分け表示を行うための設定をRedmine標準添付のAlternateテーマから取り込みました。
> * チケット一覧画面において期限が超過したチケットをオレンジ色で表示するよう変更しました。
> * チケット一覧画面において担当者・作者欄の自分の名前を太字で表示するよう変更しました。


## 利用環境

- Redmine 4.2
	- インストールディレクトリ： /var/lib/redmine
- Ubuntu Linux 20.04.5 LTS 日本語環境 Remix

## インストール方法

### 1: テーマが格納されたディレクトリを作成

以下のコマンドを実行してください。
インストール環境の権限次第では直接cloneできるかもしれません。
下記はRedmine の所有者が www-data というユーザーである場合の例です。

cloneは初回のみ：
```
cd github-workspace/

git clone https://github.com/hvygmr/redmine_theme_farend_basic_customized.git
#or
git clone git@github.com:hvygmr/redmine_theme_farend_basic_customized.git

git pull
sudo rsync -auv --exclude=.git redmine_theme_farend_basic_customized/* /var/lib/redmine/public/themes/farend_basic_customized/
sudo chown -R www-data:www-data /var/lib/redmine/public/themes/farend_basic_customized
```

サーバーの再起動などは不要で、設定の変更画面のドロップダウンに表示されるようになります（後述）。

### 2: テーマの設定を変更

Redmineの管理画面で新しいテーマを利用する設定を行います。

「管理」→「設定」→「表示」画面内の項目「テーマ」で「Farend basic customized」を選択、
画面最下部の「保存」ボタンをクリックしてください。

