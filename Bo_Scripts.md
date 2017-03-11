### Build spark
In pathToSpark/spark folder do 
```
build/mvn -DskipTests clean package
```

### Start spark shell on local machine
In pathToSpark/spark folder do
```
./bin/spark-shell  
```
### Test repartitionWithWeight in sc on local machine
In spark context do 
```
$ import collection.mutable.HashMap
$ var locWeight = HashMap("127.0.0.1"-> 3, "127.0.0.2"->1)
$ var part = sc.textFile("two_diamonds_400.txt")
$ part = part.repartitionWithWeight(4, locWeight)
$ part.count()
```
