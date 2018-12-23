# use-guide

1. Setup spark cluster.
```bash
docker-compose up -d
```

2. Enter spark-master.
```bash
docker exec -it {container-id} /bin/bash
```

3. List all containers。
```bash
docker ps -a
```

4. Stop container.
```bash
docker stop {container-id}
```

5. Delete container.
```bash
docker rm {container-id}
```

