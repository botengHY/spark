#Spark

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

#AWS EC2

### ec2 public dns
```
ec2-52-91-175-30.compute-1.amazonaws.com
ec2-52-205-171-223.compute-1.amazonaws.com
ec2-52-207-234-132.compute-1.amazonaws.com
ec2-54-152-18-243.compute-1.amazonaws.com
ec2-54-166-109-227.compute-1.amazonaws.com
ec2-54-166-181-97.compute-1.amazonaws.com
ec2-54-173-214-238.compute-1.amazonaws.com
ec2-54-211-235-198.compute-1.amazonaws.com
ec2-54-224-117-152.compute-1.amazonaws.com
ec2-54-234-112-145.compute-1.amazonaws.com
```
### ssh to ec2 instances
```
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-52-91-175-30.compute-1.amazonaws.com
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-52-205-171-223.compute-1.amazonaws.com
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-52-207-234-132.compute-1.amazonaws.com
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-54-152-18-243.compute-1.amazonaws.com
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-54-166-109-227.compute-1.amazonaws.com
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-54-166-181-97.compute-1.amazonaws.com
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-54-173-214-238.compute-1.amazonaws.com
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-54-211-235-198.compute-1.amazonaws.com
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-54-224-117-152.compute-1.amazonaws.com
ssh -y -i ~/thesis/utilities/spark_ec2.pem ubuntu@ec2-54-234-112-145.compute-1.amazonaws.com
```

# Setting up EC2 Spark environment
1. Install java following http://tipsonubuntu.com/2016/07/31/install-oracle-java-8-9-ubuntu-16-04-linux-mint-18/
2. Install scala following 



























