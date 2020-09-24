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
docker-compose exec gcloud /bin/ash
```
```
docker-compose exec azure /bin/ash
```
```
docker-compose exec aws /bin/ash
```

## エイリアス

+ 短いコマンドで実行できるようエイリアスを貼っておきます。

```
alias dg='cd ${Repositoryを置いているPATH}/multi-cli && docker-compose exec multi-cli-gcloud /bin/ash && cd -' 
alias dz='cd ${Repositoryを置いているPATH}/multi-cli && docker-compose exec multi-cli-azure  /bin/ash  && cd -'
alias dw='cd ${Repositoryを置いているPATH}/multi-cli && docker-compose exec multi-cli-aws    /bin/ash  && cd -'
```

## 補足

+ コンテナ内で docker コマンドを使えるようにするために、 Docker outside of Docker = DooD を採択している
  + 参考: https://blog.nijohando.jp/post/docker-in-docker-docker-outside-of-docker/

