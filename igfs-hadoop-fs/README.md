## To run
```
./ignite.sh ./igfs-hadoop-fs-config.xml
```

```
hdfs --config ./ignite_conf dfs -ls /
hdfs --config ./ignite_conf dfs -mkdir /wc-input
hdfs --config ./ignite_conf dfs -put <file> /wc-input
hdfs --config ./ignite_conf dfs -mkdir /output
hdfs --config ./ignite_conf dfs -rm -r /output && time hadoop --config ./ignite_conf jar /opt/hadoop/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.8.0.jar wordcount /wc-input /output
```

