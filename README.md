# multi-cli

各クラウドの CLI を Docker Compose で。

## やりたいこと

+ 各クラウドの CLI を Docker Compose で管理というか、Docker を使うことによって、ホストを汚さずに実行出来るようにしたい
+ var は置いておく？ OR auth をやる?

## 公式ドキュメント

+ Overview of Docker Compose
  + https://docs.docker.com/compose/

## 起動方法 (WIP)

```
$ docker-compose up -d
$
$ docker-compose exec gcloud /bin/bash
#
# gcloud version
Google Cloud SDK 278.0.0
bq 2.0.52
core 2020.01.24
gsutil 4.47
```
