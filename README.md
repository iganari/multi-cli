# multi-cli

各クラウドの CLI を Docker Compose で。

## やりたいこと

+ 各クラウドの CLI を Docker Compose で管理というか、Docker を使うことによって、ホストを汚さずに実行出来るようにしたい
+ var は置いておく？ OR auth をやる?

## 公式ドキュメント

+ Overview of Docker Compose
  + https://docs.docker.com/compose/

## 起動方法 (WIP)

+ Docker Compose を起動します。

```
docker-compose up -d
```

+ 実行方法

```
docker-compose exec gcloud /bin/bash
```
```
docker-compose exec azure /bin/bash
```

## エイリアス

+ 短いコマンドで実行できるようエイリアスを貼っておきます。

```
alias dgcp='cd ${Repositoryを置いているPATH}/multi-cli && docker-compose exec gcloud /bin/bash && cd -' 
alias  daz='cd ${Repositoryを置いているPATH}/multi-cli && docker-compose exec azure /bin/bash  && cd -' 
```
