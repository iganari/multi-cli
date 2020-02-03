# multi-cli

Multi Cloud Contaner on Docker Compose.

## Want

I want to be able to carry the execution environment freely by managing the CLI of each cloud with Docker Compose.

## Official Document

+ Overview of Docker Compose.
  + https://docs.docker.com/compose/

## How to Use

+ Start Docker Compose.

```
docker-compose up -d
```

+ Use Container.

```
docker-compose exec gcloud /bin/ash
```
```
docker-compose exec azure /bin/ash
```
```
docker-compose exec aws /bin/ash
```

## Set Alias

+ Setting Alias on Bash for using easy.

```
alias dg='cd ${Your Repository's PATH}/multi-cli && docker-compose exec gcloud /bin/ash && cd -' 
alias dz='cd ${Your Repository's PATH}/multi-cli && docker-compose exec azure  /bin/ash  && cd -'
alias dw='cd ${Your Repository's PATH}/multi-cli && docker-compose exec aws    /bin/ash  && cd -'
```

## Comment

Have fun !! :)
