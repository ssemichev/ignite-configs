## To start Ignite cluster
```
./ignite.sh ./map-reduce-config.xml
```


## To run Ignite Map/Reduce
```
hdfs dfs -mkdir /wc-input
hdfs dfs -put <file> /wc-input
hdfs dfs -mkdir /output
hdfs dfs -rm -r /output && time hadoop --config ./ignite_conf jar /opt/hadoop/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.8.0.jar wordcount /wc-input /output
```

## To run a pure Hadoop job
```
hdfs dfs -rm -r /output && time hadoop jar /opt/hadoop/share/hadoop/mapreduce/hadoop-mapreduce-examples-2.8.0.jar wordcount /wc-input /output
```

