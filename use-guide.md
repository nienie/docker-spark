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

6. Spark management webstie.

Chrome: "http://127.0.0.1:8080"

7. Test spark cluster
```bash
# login spark master
docker exec -it {container-id} /bin/bash
cd spark
bin/spark-submit --class org.apache.spark.examples.SparkPi --master spark://spark-master:7077 examples/jars/spark-examples_2.11-2.4.0.jar 100 2>&1 | grep "Pi is roughly"
```
