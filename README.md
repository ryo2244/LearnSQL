# README

ここで登場するコマンドは VSCode 上のターミナルで検証を行っている。

## 当リポジトリの実行に必要な環境

- Docker Desktop

## PostgreSQL のコンテナへの入り方

まずターミナルで以下のコマンドを実行し、リポジトリを Clone 後 VSCode 上で開く。

```sh
git clone https://github.com/ryo2244/LearnSQL.git
cd LearnSQL
code .
```

PostgreSQL のコンテナに入るには Docker Desktop アプリが起動した状態で以下のコマンドを実行する。

```sh
docker compose up -d
docker compose exec sampledb bash
```

先ほどのコマンドの sampledb 部分は compose.yml に書いたサービス名によって決まるので別リポジトリでは異なるコマンドになる可能性もある。

psql コマンド実行後から終了させる処理

```sh
psql -U postgres
exit # psql の終了
```

Docker コンテナを終了する処理

```sh
exit # Docker のコンテナから抜ける
docker compose down
```
