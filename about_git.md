# gitでの開発環境

## メリット
- html、css、jsファイル等のバージョン管理  
誰がいつ、どのような修正をしたか履歴を残せる。
- 画像のバージョン比較も可能 [参照url](https://www.cherrypieweb.com/weblog/technical/20130331014928.php)  
- dream weaver CC もgitに対応[参照url](https://blogs.adobe.com/creativestation/web-dreamweaver-cc-git-support)
- 最近のエディターソフト（visual studio code等）も最初からgit対応している

## デメリット
- ひと手間増える  
これまでは、workdata内のファイルを直接編集していた。今後はgitを使用して個人pcにclone（クローン）して編集することになる。
- 「競合」とか「ブランチ」になると、gitの理解が難しい。
- NICのsvnと同じようなもの（ちょっと違うけど）

## 結論
- ソフトがgitに対応してきている事を考えると、git化はさけられないのでは？
- 最初は「競合」とか「ブランチ」は難しいので、気にせず、ただのファイル共有として使ってみる  
（現在のworkdataと何も変わらない使い方、オペレーションが少し変わるだけ）
- 少し触ってみて感じたのは、**実際に使ってみないと、全く、まったく、全然、理解できない**

<br>
<br>

# 開発環境の変更

## <a name="anc_git_img">（仮）変更イメージ</a>
<img src="img/img_environment.jpg" width="800">

## 現在の開発環境
- workdataのファイルを各個人が直接修正
- 同時に開かないように注意しながら作業
- 誰が修正したのかは、ディレクター or 修正した本人しか、わからない。

## 今後の開発環境  
- workdataから各個人PCにコピー（git clone）したファイルを修正
- 各個人pc内のwebサーバーで修正・確認することになる。
- ディレクターは、変わらずworkdataで確認。
- 誰がいつどんな作業をしたのか、全員がわかるようになる。

## 個人PCで作業するにあたっての問題点。
- 各個人PCで作業するには、webサーバーが必要。
- gulp のwebサーバーでは駄目なのか？  
gulp でもgulp-connect-php とかでweb serverを立てれる。  
でも、いちいち作業フォルダ内のgulpを起動するのか？
- xampp と gulp どっちでもいいけど、簡単なのはxamppかなぁ。  
xampp の方が、windowsの起動と同時に起動するようにしちゃえば楽。
- **ただ、xamppを使用する場合、注意しないといけない事もある [こちらを参照](#anc-xampp)**

<br>
<br>

# とにかく実際に触ってみよう。  
（触らないと、絶対わからない）  
<br>
## 1. git インストール
- [参照url](https://qiita.com/toshi-click/items/dcf3dd48fdc74c91b409)  
インストール途中でエディターを選択する場面がありますが、そのままデフォルトで。  

## 2. gitクライアント インストール
- **Source Tree（一番メジャーかな？？）**  
[参照url](https://eng-entrance.com/sourcetree-use)  
思ったより簡単なソフト。機能もよくみると、そんなに多くなさそう。シンプル。単純に使うなら、左上の大きいボタンだけでOK。  
[インストール方法 参照url](https://eng-entrance.com/sourcetree)  
※インストールの途中でAtlassianのアカウント登録をしないとインストールが進まない箇所がありますので登録してください。  
- Tortoise Git（tortoise SVNと同じ）  
[参照url](https://backlog.com/ja/git-tutorial/intro/intro2_1.html)  
なんとなくNIC案件でbad feelだったので、やめとく。

クライアントツールは、いろいろあるけど**source tree が参考サイトが多いので、とりあえずはこのソフトで慣れよう**。  
実際にはコマンドの操作をGUI化しているだけで、慣れてくると「コマンドの方が早いわ」ってなる可能性はある。

## 3. リモートリポジトリを作成
- ~~本来はworkdataをリモートリポジトリにする。(予定)~~  
- 現在は、まだ~~workdataを~~準備中なので、git hub をリモートリポジトリとしてgitを使ってみる。  
ただ、無料だとpublic（一般公開）なので、**実際の仕事のデータ（クライアントのhtml等）はアップしない。**
- git hubへ接続するには公開鍵が必要です（[下記参照](#anc-github)）
- backlogでもリモートリポジトリ作れる。

## 4. gitの簡単な操作を体験してみる  
どうでもいいファイル・リポジトリで、とにかく試す。  
まずは簡単な操作だけ。  
下記をやってみると、gitへの恐怖心が少し減る。  

1. リモートリポジトリからクローン
2. ファイルを適当に編集
3. ローカルリポジトリへコミット
4. リモートリポジトリへプッシュ
5. リモートリポジトリからプル

[参照url](https://eng-entrance.com/sourcetree-use)

**マージ・ブランチは後回し。まずは単純な操作に慣れる。**

<br>
<br>

### <div id="anc-github">git hub への接続方法</div>
git hubへ接続するには、公開鍵が必要になる。  

1. git hub に自分のアカウントを作成
2. 秘密鍵、公開鍵を作成
[参照url](https://qiita.com/reflet/items/5c6ba6e29fe8436c3185#gitbash%E3%81%AE%E8%B5%B7%E5%8B%95)
3. 公開鍵をgithubに設定
[参照url](https://qiita.com/0ta2/items/25c27d447378b13a1ac3)
4. 秘密鍵をsourcetreeに設定
[参照url](https://qiita.com/reflet/items/4f7b5c4a312bc27df10e)
5. 上記の方法でOKですが、gitlab等、他のリポジトリでも鍵を使用するため、下記にも設定してください。  
（また、現在 gitlabは、sourcetreeのアカウント作成ができないので、こちらの方法を行ってください。）
[参照url](https://qiita.com/kyamawaki/items/05abbbec5f617f3ae5eb)
6. アクセス可能

~~※毎日パソコンを起動するたびに1回、秘密鍵のパスワードを入力しないといけないけど、まぁたいした作業じゃないし、セキュリティ的にはいいかも。~~
- そのままだと、毎日パソコンを起動して、sourcetreeでSSH接続するたびに、「SSHエージェント」が起動してしまいます。  
それを回避し、windowsログイン時に「SSHエージェント」を起動する方法がありましたので、下記に記載します。  
[参照url](https://qiita.com/reflet/items/6d74851f033ddc325df9)

- SSHエージェントが起動した際に、秘密鍵のパスフレーズが要求されます。セキュリティ上は設定されていた方がイイですが、もし面倒な方がいましたら、下記の操作でパスフレーズを解除できます。  
[参照url](https://info.yama-lab.com/ssh%E7%A7%98%E5%AF%86%E9%8D%B5%E3%81%AE%E3%83%91%E3%82%B9%E3%83%95%E3%83%AC%E3%83%BC%E3%82%BA%E3%82%92%E8%A7%A3%E9%99%A4/)

<br>

---

### テスト用に作成してみたリモートリポジトリ（参考）
- テスト用github（宮崎用）
https://github.com/miyazaki-mba/git_test
- テスト用backlog（宮崎用）
https://test-kaku.backlog.com/git/TEST

みなさん自分のアカウントを作成して、リモートリポジトリを作成してください。

<br>

### gitをworkdataで使えるように準備中
~~1. workdataに、git をインストールしてもらえるように、Mr.Nakamuraに依頼。~~  
~~一旦、Mr.Nakamuraにgitについて理解してもらってから、~~  
~~workdataのサーバーにインストールしてもらうことになった。~~

そもそも、workdataではなく、githubなどのホスティングサーバーに置くようになるかもしれないので、workdataの件は一旦保留。  
詳しくは、後ほど、[3. Git hub の説明](https://github.com/miyazaki-mba/git_test/blob/master/about_github.md)を見てね。

<br>

### gitについて参考URL
いろいろ書かれているけど、操作してみないと、全くわからない。
- [参照url](https://www.slideshare.net/matsukaz/git-28304397)  
- [参照url](https://backlog.com/ja/git-tutorial/intro/intro1_1.html) 

- [参照url](https://www.symmetric.co.jp/blog/archives/577)  
- [参照url](https://eng-entrance.com/category/programming/git)  

- [用語とかざっくり 参照url](https://qiita.com/kyoyyy/items/161b6905f45bee2efe21)

<br>

## <div id="anc-xampp">個人PCでxamppを使用するにあたって</div>
1. xampp インストール方法
[参照url](https://techacademy.jp/magazine/1722)
2. xampp セキュリティ設定
[参照url](https://techacademy.jp/magazine/2941)  

### xampp 懸念事項
- xamppで心配なのは、**サーバーの設定**の共有方法
- 各個人PCのサーバーの設定が同じじゃないと、制作上おかしいことになる。  
「この人は表示されるけど、この人は表示できない等」
- windows シンボリックリンクで、xamppのapacheの設定ファイルを、workdataのwebサーバーの設定ファイルを読みに行くようにしたらどうか？  
それっぽい記事があった。
