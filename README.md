# Docker-Compose para APM

### Objetivo

O objetivo é ilustrar um docker-compose que irá montar 3 imagens para nós. São elas:
- ElasticSearch - Porta 9200
- Kinana - Porta 5601
- APM Server - Porta 8200 e 8201

### Projeto

A execução de um docker-compose se da pelos seguintes comandos:
```
docker-compose build
```
e
```
docker-compose up -d
```
Para checar se tudo está em pé então execute o comando:
```
docker ps -a
```
E verá as 3 imagens sendo executadas:
```
CONTAINER ID   IMAGE                                                 COMMAND                  CREATED          STATUS          PORTS
                       NAMES
4a3f2cc41e69   docker.elastic.co/kibana/kibana:7.7.0                 "/usr/local/bin/dumb…"   31 seconds ago   Up 26 seconds   0.0.0.0:5601->5601/tcp                           kibana
c5d8bcb7fec9   docker.elastic.co/apm/apm-server:7.7.0                "/usr/local/bin/dock…"   31 seconds ago   Up 26 seconds   0.0.0.0:8200->8200/tcp, 0.0.0.0:8201->8200/tcp   apm-server
ea791a3b4c89   docker.elastic.co/elasticsearch/elasticsearch:7.7.0   "/tini -- /usr/local…"   33 seconds ago   Up 28 seconds   0.0.0.0:9200->9200/tcp, 9300/tcp                 elasticsearch
```
Caso tenha dúvidas você pode me procurar por aqui ou no meu [LinkedIn pessoal](https://www.linkedin.com/in/felipebossolani/)
