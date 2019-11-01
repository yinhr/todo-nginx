# todo-nginx
todo管理アプリのリバースプロキシ（nginx）

## Description
フロントエンドからのリクエストをバックエンドのAPIサーバにルーティングする

ECSタスクとして稼働させAPIエンドポイントはService Discoveryで設定したローカルドメインを使用

## todo管理アプリ
以下参照

[todo管理アプリについて](https://www.notion.so/prmcy/ToDo-14f83b283c4b4bd088ee9f11ebe5be13)

## Usage

### ディレクトリ構成
```
[project root]
├── client/ (yinhr/todo-frontend）
├── db/
│   ├── Dockerfile (下記Gist参照)
│   └── my.cnf (下記Gist参照)
├── nginx/ (yinhr/todo-nginx *このリポジトリ）
├── server/ (yinhr/todo-backend)
└── docker-compose.yml (下記Gist参照)
```
* [Dockerfile](https://gist.github.com/yinhr/3ff5456bc9859af9de7bde2923b84f94)
* [my.cnf](https://gist.github.com/yinhr/ee5fe7dc88831de8f5994447c89cff93)
* [docker-compose.yml](https://gist.github.com/yinhr/bfe1c20f700df5fca2a44ad18f7f3102)

### コンテナ起動
```
docker-compose up --build
```

### ブラウザで下記にアクセス
```
http://localhost:3000
```
