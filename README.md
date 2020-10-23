# docker_postgres_local
posgreのローカル開発環境

## 起動

```bash
mkdir docs
mkdir data
docker-compose up
```

## アクセス情報

ユーザー：postgres
パスワード：postgres

例：
```bash
psql -U postgres -h localhost
```

## ドキュメント作成

以下のコマンドを実行するとdocsディレクトリにドキュメントが生成される。

```bash
docker run --network docker_postgres_default --rm -v "$PWD/docs:/output" -v "$PWD/schemaspy.properties:/schemaspy.properties" schemaspy/schemaspy:lates
```
