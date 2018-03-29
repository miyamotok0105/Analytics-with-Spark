

```
mkdir linkage
cd linkage
wget https://archive.ics.uci.edu/ml/machine-learning-databases/00210/donation.zip
unzip donation.zip

mvn clean package

spark-submit --class com.cloudera.datascience.intro.RunIntro target/ch02-intro-2.0.0-jar-with-dependencies.jar

```

対話形式で動かしてみる    

```
spark-shell --master local[*]
```


```
import org.apache.spark.{SparkConf, SparkContext}
import org.apache.spark.SparkContext._
import org.apache.spark.rdd.RDD
import org.apache.spark.util.StatCounter
val sc = new SparkContext(new SparkConf().setAppName("Intro"))
val rawblocks = sc.textFile("/Users/miyamoto/Projects/sample/Analytics-with-Spark/ch02-intro/linkage/donation/block_1.csv")

//「アクション」
//RDDは作成した後にアクション実行時に分散処理される。
//countアクション
rawblocks.count()
//collectアクションはすべてのオブジェクトを取得しArrayとして返す。クラスタ内ではなく、ローカルメモリに置かれる。
rawblocks.collect().take(5)

rawblocks.take(5).foreach(println)

rawblocks.take(5).length

rawblocks.first



```