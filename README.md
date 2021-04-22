# embulk_mysql_docker

EmbulkとMySQLのDocker環境

## 使い方
### 起動
```bash
$ docker-compose up --build
```

```bash
$ docker-compose ps
            Name                         Command             State          Ports
----------------------------------------------------------------------------------------
embulk_mysql_docker_embulk_1   bash                          Up
embulk_mysql_docker_mysql_1    docker-entrypoint.sh mysqld   Up      3306/tcp, 33060/tcp
```

### Embulk
```bash
$ docker exec -it embulk_mysql_docker_embulk_1 bash
```

```
root@029af15f9037:/app# embulk --version
embulk 0.9.23
```

### MySQL
```bash
$ docker exec -it embulk_mysql_docker_mysql_1 mysql
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 51
Server version: 5.7.29 MySQL Community Server (GPL)

Copyright (c) 2000, 2020, Oracle and/or its affiliates. All rights reserved.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql>
```
