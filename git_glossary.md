# git 用語

- チェックアウト checkout  
そのブランチを「選択する」という事。フォーカスを当てる。アクティブにする。
ローカルでファイルを編集する際に、例えば、ブランチが2つあると、2つとも編集できるけど、
実際には、どっちかを「選択」して編集しないといけない。
その際に、「選択する」ことを「チェックアウト」と言っている。

- origin  
リモートリポジトリの場所(URL)の別名

- master  
ブランチの名前  
つまり、"git pull origin master" は、  
originという名前のレポジトリのマスターブランチから、git pull しろと命令している。

- originとか masterというのは、それぞれの初期値（デフォルト値）  
つまり、 "git pull" = "git pull origin master"

- HEAD  
自分が今どのブランチで作業しているかを示す特別なポインタ。ブランチの先頭を表す名前。

<br>
<br>

---
## sourcetree を見ながら
### masterとorigin/masterの違い
- master  
作業ディレクトリと結びついているブランチ（ローカルリポジトリのブランチ）

- origin/master  
リモートリポジトリoriginにあるリモートブランチmasterと結びついているブランチ。  
リモートブランチmasterをローカルリポジトリでトラッキングするためのブランチ（リモートトラッキングブランチ）です。  
リモートブランチを参照するために利用しています。  
[参照url](https://nekosoftware.wordpress.com/2015/02/03/git%E3%81%AE%E3%81%B5%E3%82%8F%E3%81%A3%E3%81%A8%E3%81%97%E3%81%9F%E7%9F%A5%E8%AD%98%E3%82%92%E8%AA%BF%E6%9F%BB%E3%81%97%E3%81%A6%E3%81%BF%E3%81%9F/)

- origin/HEAD
リモートリポジトリoriginの、デフォルトブランチを表しています。
git clone する際は、デフォルトブランチからダウンロードされる。

<br>
<br>

---
## git とは直接関係ないけど
gitを調査する中で、関係してきた言葉（最近よく見る言葉）
- ビルドとデプロイ  
[参照url](https://qiita.com/isoyam/items/3d1fc5cf7403cdf4818d)

- アジャイル開発  
[参照url](https://hnavi.co.jp/knowledge/blog/agile_software_development/)

- DevOps （デブオプス）  
[参照url](https://qiita.com/bremen/items/44c3de10413f45f9f41e)

