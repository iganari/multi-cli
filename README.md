# multi-cli

Multi Cloud Contaner on Docker Compose

## Want

+ 各クラウドの CLI を Docker Compose で管理というか、Docker を使うことによって、ホストを汚さずに実行出来るようにしたい

## Official Document

+ Overview of Docker Compose
  + https://docs.docker.com/compose/

## How to Use

+ Start Docker Compose

```
docker-compose up -d
```

+ Use Container

```
docker-compose exec gcloud /bin/bash
```
```
docker-compose exec azure /bin/bash
```
```
docker-compose exec aws /bin/bash
```

## Set Alias

+ Setting Alias on Bash for using easy

```
alias dg='cd ${Your Repository's PATH}/multi-cli && docker-compose exec gcloud /bin/bash && cd -' 
alias dz='cd ${Your Repository's PATH}/multi-cli && docker-compose exec azure /bin/bash  && cd -'
alias dw='cd ${Your Repository's PATH}/multi-cli && docker-compose exec azure /bin/bash  && cd -'
```
