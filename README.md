# SpringBoot-on-Azure
## Setup
`docker-compose up -d`

### CosmosDBのセットアップ
`https://localhost:8081/_explorer/index.html`へアクセス
※コンテナ立ち上がり直後はアクセス出来ない可能性あり。少し時間をおいてアクセス推奨。

必要な情報を`.env`ファイルへ記述
```
# CosmosDB
cosmos-url=
cosmos-primary-key=
primary-connection-string=
mongo-connection-string=
```

### Springプロジェクトを追加
`README.md`と同じ階層へプロジェクト下でプロジェクトを`clone`
