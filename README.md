# 说明 

在Linux系统，$PWD表示当前目录路径

```
git clone https://github.com/zoesimin/neo4jDB.git
cd neo4jDB
docker run \
    --name testneo4j \
    -p7474:7474 -p7687:7687 \
    -d \
    -v $PWD/neo4j/data:/data \
    -v $PWD/neo4j/logs:/logs \
    -v $PWD/neo4j/import:/var/lib/neo4j/import \
    -v $PWD/neo4j/plugins:/plugins \
    --env NEO4J_AUTH=neo4j/123456 \
    neo4j:3.5.0
```

data数据持久化的目录: ```$PWD/neo4j/data```

在浏览器上打开```http://0.0.0.0:7474```，用户名为 neo4j，密码为 123456，登陆



参考资料 :

[https://neo4j.com/developer/docker-run-neo4j/](https://neo4j.com/developer/docker-run-neo4j/)
