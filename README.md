# laravel-docker-template
## 環境構築
１．coachtech/laravelへ移動後、開発環境をGitHubよりクローン。名前を変更しておく。
　　git clone git@github.com:Estra-Coachtech/laravel-docker-template.git
　　mv laravel-docker-template HTML-creation

２．開発の履歴を残すためリポジトリを新たに作成しローカルリポジトリから紐づけを行う。
　　cd HTML-creation
　　git remote set-url origin git@github.com:hosomitadasi/HTML-creation.git

３．ローカルリポジトリのデータをリモートリポジトリに反映させる。
　　git add .
　　git commit -m "HTML作成用プログラミング作成"
　　git push origin main

４．Docker の構築を実行
　　docker-compose up -d --build

５．Laravelパッケージをインストール
　　docker-compose exec php bash
　　composer install

６．envのコピーを実行
　　cp .env.example .env

７．APPキーの作成を実行
　　php artisan key:generate
