# README

## 環境構築
- Apple M2 Pro
- macOS Venture 13.5.1
- Docker Desktop 4.22.1


Dockerfile, docker-compose.yml, Gemfile, Gemfile.lockファイルのみ配置されている状態で実行する。  
ただし、Gemfile.lockは空ファイルにすること。

```
docker-compose run web rails new . --force --database=mysql --skpi-bundle
```

config/database.ymlを編集する。
```
password: password
host:db
```

```
docker-compose build
docker-compose up -d
docker-compose run web rails db:create
```