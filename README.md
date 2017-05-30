[Ignite Map/Reduce](map-reduce-in-memory/README.md)

[Ignite IGFS Hadoop](igfs-hadoop-fs/README.md)

[Ignite IGFS Hadoop Cache](igfs-hadoop-fs-cache/README.md)




![ScreenShot](https://cloud.githubusercontent.com/assets/5940291/26463938/f6465e64-4153-11e7-8d67-b8424188c07c.png
)

## Local setup

```
cd /opt
wget -P /opt "http://mirror.nexcess.net/apache//ignite/2.0.0/apache-ignite-hadoop-2.0.0-bin.zip"
unzip 
ln -sfn /opt/apache-ignite-hadoop-2.0.0-bin/ ignite
rm apache-ignite-hadoop-2.0.0-bin.zip
```

## Run locally
```
/opt/ignite/bin/ignite.sh /opt/ignite/examples/config/example-cache.xml
```

## Run as a docker container
```
docker run -it --net=host -e "IGNITE_CONFIG=/opt/ignite/examples/config/example-cache.xml" apacheignite/ignite:2.0.0
```

## To run an example
```
sbt
>runMain examples.HelloIgnite
```
