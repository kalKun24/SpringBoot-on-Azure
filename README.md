# SpringBoot-on-Azure
## Setup
### Springプロジェクトを追加
`README.md`と同じ階層へプロジェクト下でプロジェクトを`clone`

`.env`ファイルの`project-name=`をプロジェクトフォルダの名前に変更する。
デフォルトは`spring-project`

プロジェクトフォルダ内に`Dockerfile`を追加
```
FROM openjdk:21

RUN microdnf install findutils
RUN sh gradlew build
```

### コンテナ立ち上げ
`docker-compose up -d`

### CosmosDBのセットアップ
`curl -k https://localhost:8081/_explorer/emulator.pem > emulatorcert.crt`で証明書をダウンロード
※コンテナ起動ごとに証明書が切り替わるため注意

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