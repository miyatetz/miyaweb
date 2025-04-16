# 概要
これは[宇都宮大学鉄道研究会のサイト](https://miyatetz.github.io/miyaweb/)です。

JekyllとGitHub Pagesを利用しています。

# ライター追加の仕方
ライターを追加したい場合はこのレポジトリ、またはmiyatetzオーガニゼーションに対してライターのアカウントをレポジトリの編集が可能な権限をつけた状態で追加してください。

# 記事の書き方
## 記事を作る
マークダウン方式で書くことで記事を追加出来ます。

まずは.md形式のファイルを`_drafts`フォルダ内に作成してください。

その際、名前は`2023-12-28-titlename.md`のようにすると整理しやすいです。

作成したのちファイルの初めに以下の内容を記述してください。
```
---
layout: post
title:  "記事のタイトル"
date:   YYYY-MM-DD 22:00:00 +0900
categories: Test
---
```




## 記事を書く
先ほど記述した内容の次の行から記事の本文を書くことができます。

マークダウンでは段落や画像、水平線、外部リンクの追加など様々なことができます。

くわしくは[マークダウンチートシート](https://gist.github.com/mignonstyle/083c9e1651d7734f84c99b8cf49d57fa)を参照してください。

### 便利な編集方法

マークダウン編集には、
[Visual Studio Code](https://code.visualstudio.com/)というテキスト編集ソフトの
拡張機能 [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)の使用をお勧めします。

Wordの要領でマークダウンの編集が可能になります。

詳しい導入方法については

[Visual Studio Codeのダウンロードとインストール](https://www.javadrive.jp/vscode/install/index1.html)および
[Markdown All in Oneの導入](https://zenn.dev/ctrlkeykoyubi/articles/vscode-markdown-all-in-one)をご覧ください。

導入後の操作方法（ショートカット）
| キー              | 説明                                                                 |
|------------------|----------------------------------------------------------------------|
| Ctrl + B         | 選択した文字の太字にする   |
| Ctrl + I         | 選択した文字を斜体にする                                              |
| Ctrl + Shift + ] | 見出しレベルを上げる                                                 |
| Ctrl + Shift + [ | 見出しレベルを下げる                                                 |
| Ctrl + M         | 数式入力の文字入れる                                          |
| Alt + C          | チェックリストのオンオフ                                             |
| Ctrl + Shift + V | プレビューのオンオフ             |
| Ctrl + K → V     | エディタの横にプレビュー。      |
| Ctrl + Z         | 操作を1つ取り消す（Undo）                                           |


### 画像の追加について
画像などを追加する場合は`assets`フォルダ内に追加してそのパスを指定してください。
```
![キャプション]({{site.baseurl}}/images/sample.png)
```

## 記事を公開する
記事を公開するには公開したい記事のマークダウンファイルを`_drafts`フォルダから`_posts`フォルダに移動してください。

移動した状態でコミットするとその場で公開されます。

# 保守の仕方
## ホームページの内容を変更する
ホームページの内容を変更する場合は`index.markdown`の内容を変更してください。

## `about`の内容を変更する
`about`内の内容を変更したい場合は`about.markdown`の内容を変更してください。

## サイトが更新されないときは
このサイトはGitHub PagesのActionsにあるJekyllを用いてマークダウンからhtmlやcssをコミットされるたびに生成しています。

そのため記事公開のコミットをしても、生成が終わるまでは更新されません。

もし、３分以上待っても更新されなかった場合、何かしらの問題が発生したと考えられます。

### GitHub Actionsの確認
このレポジトリの`Actions`タブから正しく生成されているかを確認できます。最新のコミットに対しての生成が失敗している場合ここに表示されます。

### Jekyll on Windowsでの確認
GitHub上でちゃんと動かない場合、JekyllをWindowsで動作させることで問題を特定できる場合があります。

このリポジトリを自分の端末にクローンして試してください。
