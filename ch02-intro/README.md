

```
mkdir linkage
cd linkage
wget https://archive.ics.uci.edu/ml/machine-learning-databases/00210/donation.zip
unzip donation.zip

mvn clean package

spark-submit --class com.cloudera.datascience.intro.RunIntro target/ch02-intro-2.0.0-jar-with-dependencies.jar

```

