# 使用docker部署nexus

## docker run

```shell
docker volume create nexus
docker run --restart=always -d -p 8081:8081 -v nexus:/nexus-data --name nexus sonatype/nexus3:latest
```

## docker-compose

[docker-compose up -d](docker-compose.yml)