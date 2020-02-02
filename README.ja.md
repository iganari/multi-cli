# multi-cli

各クラウドの CLI を Docker Compose で。

## やりたいこと

+ 各クラウドの CLI を Docker Compose で管理を用いることで、実行環境を持ち運び出来るようにしたい。

## 公式ドキュメント

+ Overview of Docker Compose
  + https://docs.docker.com/compose/

## 起動方法 (WIP)

+ Docker Compose を起動します。

```
docker-compose up -d
```

+ 実行方法は下記の通り。

```
docker-compose exec gcloud /bin/bash
```
```
docker-compose exec azure /bin/bash
```
```
docker-compose exec aws /bin/bash
```

## エイリアス

+ 短いコマンドで実行できるようエイリアスを貼っておきます。

```
alias dg='cd ${Repositoryを置いているPATH}/multi-cli && docker-compose exec gcloud /bin/bash && cd -' 
alias dz='cd ${Repositoryを置いているPATH}/multi-cli && docker-compose exec azure /bin/bash  && cd -'
alias dw='cd ${Repositoryを置いているPATH}/multi-cli && docker-compose exec azure /bin/bash  && cd -'
```
