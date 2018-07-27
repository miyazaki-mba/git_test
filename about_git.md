# gitでの開発環境


---
## gitについて
https://www.slideshare.net/matsukaz/git-28304397
https://backlog.com/ja/git-tutorial/intro/intro1_1.html
https://www.symmetric.co.jp/blog/archives/577
https://eng-entrance.com/category/programming/git

## gitのメリット
- 画像の比較もできる
https://www.cherrypieweb.com/weblog/technical/20130331014928.php

- dream weaver CC もgitに対応
https://blogs.adobe.com/creativestation/web-dreamweaver-cc-git-support

- psdなどもgitで管理する？
https://www.cloudot.co.jp/blog/2906/

- 競合とかブランチが難しい。
- 最初は競合しないで、ファイル共有として使ってみるのが、いいのでは？


---
## 現在の開発環境
- 現状 workdataのファイルを直接修正
- 今後 workdataから各個人PCにコピー（git clone）したファイルを修正する

### 今後の開発環境  
各個人pc内のwebサーバーで確認することになる。

- php は使用するのか？
もし、使用するならxampp？
- gulp のwebサーバーでは駄目なのか？
gulp でもgulp-connect-php というのがあるらしい。
でも、いちいちgulpを起動するのか？
- xammp と gulp　どっちでも、やりたい方法でいいんじゃない？
xampp がシンプルでいいのでは？

### xamppを使用した場合
https://qiita.com/rTachibana/items/b46009ae207dcd622935
- xamppで心配なのは、サーバーの設定とかの共有方法
- windows シンボリックリンクで、xamppの設定ファイルを、workdataのwebサーバーの設定ファイルを読みに行くようにしたらどうか？

### xampp インストール方法
https://techacademy.jp/magazine/1722

### xampp セキュリティ設定
https://techacademy.jp/magazine/2941

※xamppのlocalhostにアクセスできなかったけど、proxyの設定を変更してもらったら、アクセスできるようになった。


---
## gitクライアント Source Tree　（一番メジャーかな）
https://eng-entrance.com/sourcetree-use
思ったより簡単。機能もそこまでおおくない

## テスト用に作成したbacklog
https://test-kaku.backlog.com/git/TEST



---
## github （使用してみる）
- githubへpushするには、公開鍵が必要になる。  
1. gitをpcへインストール
2. 秘密鍵、公開鍵を作成
https://qiita.com/reflet/items/5c6ba6e29fe8436c3185
3. 公開鍵をgithubに設定
https://qiita.com/ajitama/items/364d89b21daf8d3481bc
4. 秘密鍵をsourcetreeに設定
https://qiita.com/reflet/items/4f7b5c4a312bc27df10e

---
## gitをworkdataのサーバーへインストール
workdataに、git をインストールしてもらえるように中村さんに依頼。
一旦、中村さんでgitについて理解してから、インストールしてくれることになった。