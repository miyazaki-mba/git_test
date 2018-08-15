# Git hub の説明（gitではなく、git habの方）
### Git hub 画面の説明
1. 画面上部  
[参照url](http://www.atmarkit.co.jp/ait/articles/1701/05/news009.html)

- 「Watch」はTwitterの「フォロー」  
フォローしたいリポジトリを「watch」をセレクトして「watching」にすると、ヘッダーの「ベルのマーク」の通知機能で、更新情報の通知を受け取れる。  
是非、Git hubに会員登録して、このgit hubのリポジトリに対して「watching」にしてみてください。  
- 「Star」はFacebookの「いいね！」  
[参照url](https://efcl.info/2014/07/30/find-github-release/)

- Marketplace は、リポジトリを販売している場所  
[参照url](https://japan.cnet.com/article/35101578/)

- explore は、イケイケなリポジトリを紹介している場所  
[参照url](https://qiita.com/luckypool/items/21eb5f515358ee33529c)

---

1. issue （イシュー）は、問題点  
[参照url](https://seleck.cc/647)

2. Fork と pull Request （フォークとプルリクエスト）、他の人のリポジトリを自分のリポジトリにコピー。それを作者にpullしてもらうように通知する。  
[参照url](http://kik.xii.jp/archives/179)  
[参照url](https://qiita.com/YumaInaura/items/acff806290c8953d3185)

3. projeccts リポジトリを管理。issueやノートを使用する。  
[参照url](https://qiita.com/nafu/items/8996738177c601dd81f9)
- zenhub  
[参照url](https://qiita.com/GeckoTang/items/f75b9a1c20c8e5091147)

4. wiki は、取扱い説明などを記載する？

5. insights はclone数や、issueの進行状況など

<br>
<br>

# git hub を導入した開発環境
以前、gitを導入した開発環境イメージを記載しました。  
ですが、以前の開発環境イメージだと、gitの履歴を見る場合に、作業しない人（ディレクター）もpullして自分のpcで確認する必要があります。  
※サイトを閲覧するだけなら、workdataのドメインで見れますが、gitの履歴を見るには、gitでpullしないと見れない。  
<br>
何か足りないなぁと思ってました。  
で、googleすると、**git hubを業務で使用**してました。  
（似たようなツールがgit hub以外にも、存在する。git lab、bitbucket、backlogなど）  
gitホスティングサービスと言っているみたいです。  
[参照url]  (https://qiita.com/k-yamada-github/items/07253054dc852a77d693)
<br>
<br>
なので正しい開発環境は下記です。  
## 開発環境（git hub使用）  
<img src="img/img_environment_02.jpg" width="800">

## git hub 導入している会社が増えている
- git hubが便利なので、業務で使う会社が増えている  
（大企業が軒並み利用している）
- 企業で利用する場合は、1ユーザー約1000円/月～(10ユーザー 1年 120,000円)

- 「Team」プランから契約可能  
- もし、ソースファイルを社内に置きたいなら「Enterprise」プラン　1ユーザー約2,327円/月～  
[参照url](https://github.co.jp/pricing.html)  
[参照url](http://careerhack.en-japan.com/report/detail/863)


## git hub 以外の似たツール
- git lab  
[参照url](https://bitbucket.org/product/pricing?tab=cloud)
社内サーバーにインストール可能。（でもメンテナンスしないといけない）  
git labのサーバー

- bitbucket  
[参照url](https://bitbucket.org/product/pricing?tab=cloud)  
10アカウントの場合、standardプランで、222円。（10ユーザー 1年 26,640円） 

- 比較しているサイト  
[参照url](https://qiita.com/hiroponz/items/c1ed4d6c10484233bf88)