## To run
```
./ignite.sh ./igfs-hadoop-fs-cache-config.xml
```

```
hdfs dfs -mkdir /wc-input
hdfs dfs -put <file> /wc-input
hdfs dfs -mkdir /output
hdfs --config ./ignite_conf dfs -rm -r /output && time hadoop --config ./ignite_conf jar /opt/hadoop/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.8.0.jar wordcount /wc-input /output
```

