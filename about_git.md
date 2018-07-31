# gitでの開発環境

## gitについて参考URL
[参照url](https://www.slideshare.net/matsukaz/git-28304397)  
[参照url](https://backlog.com/ja/git-tutorial/intro/intro1_1.html)  
[参照url](https://www.symmetric.co.jp/blog/archives/577)  
[参照url](https://eng-entrance.com/category/programming/git)  

## メリット
- html、css、jsファイル等のバージョン管理
- 画像のバージョン比較も可能 [参照url](https://www.cherrypieweb.com/weblog/technical/20130331014928.php)  
- dream weaver CC もgitに対応[参照url](https://blogs.adobe.com/creativestation/web-dreamweaver-cc-git-support)
- psdなどもgitで管理する？[参照url](https://www.cloudot.co.jp/blog/2906/)  

## デメリット
- ひと手間増える
- 競合とかブランチになると、難しい。
- 最初は競合とかブランチは気にしないで、ファイル共有として使ってみるのが、いいのでは？

<br>

# 開発環境の変更
## 現在の開発環境
- workdataのファイルを各個人が直接修正
- 同時に開かないように注意しながら作業
- 誰が修正したのかは、ディレクター or 修正した本人しか、わからない。

## 今後の開発環境  
- workdataから各個人PCにコピー（git clone）したファイルを修正
- 各個人pc内のwebサーバーで修正・確認することになる。
- 誰がいつどんな作業をしたのか、gitで、全員がわかるようになる。

## 個人PCで作業するにあたっての疑問点。
- php は使用するのか？  
もし、使用するならxampp？
- gulp のwebサーバーでは駄目なのか？  
gulp でもgulp-connect-php というのがあるらしい。  
でも、いちいち作業フォルダ内のgulpを起動するのか？
- xammp と gulp どっちでも、やりたい方法でいいんじゃない？  
xampp の方が、windowsの起動と同時に起動するようにしちゃえば楽じゃない？

# xamppを使用する場合
[参照url](https://qiita.com/rTachibana/items/b46009ae207dcd622935)
- xamppで心配なのは、**サーバーの設定**とかの共有方法
- windows シンボリックリンクで、xamppの設定ファイルを、workdataのwebサーバーの設定ファイルを読みに行くようにしたらどうか？
## xampp インストール方法
[参照url](https://techacademy.jp/magazine/1722)
## xampp セキュリティ設定
[参照url](https://techacademy.jp/magazine/2941)
※xamppのlocalhostにアクセスできなかったけど、proxyの設定を変更してもらったら、アクセスできるようになった。

# gitクライアント
## Source Tree（一番メジャーかな）
[参照url](https://eng-entrance.com/sourcetree-use)  
思ったより簡単。機能もよくみると、そんなに多くなさそう。シンプル。

# テスト用に作成したリポジトリ
## テスト用github
https://github.com/miyazaki-mba/git_test
## テスト用backlog
https://test-kaku.backlog.com/git/TEST

# github （使用してみた）
- githubへ接続するには、公開鍵が必要になる。  
1. gitをpcへインストール
2. 秘密鍵、公開鍵を作成
[参照url](https://qiita.com/reflet/items/5c6ba6e29fe8436c3185)
3. 公開鍵をgithubに設定
[参照url](https://qiita.com/ajitama/items/364d89b21daf8d3481bc)
4. 秘密鍵をsourcetreeに設定
[参照url](https://qiita.com/reflet/items/4f7b5c4a312bc27df10e)
5. 毎日パソコンを起動する毎に1回、秘密鍵のパスワードを入力しないといけない。まぁたいした作業じゃないし、セキュリティ上はいいかも。

# gitをworkdataのサーバーへインストール
1. workdataに、git をインストールしてもらえるように、Mr.Nakamuraに依頼。  
一旦、中村さんでgitについて理解してから、インストールしてくれることになった。