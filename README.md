Advanced Analytics with Spark Source Code
=========================================

Code to accompany [Advanced Analytics with Spark](http://shop.oreilly.com/product/0636920035091.do), by 
[Sandy Ryza](https://github.com/sryza), [Uri Laserson](https://github.com/laserson), 
[Sean Owen](https://github.com/srowen), and [Josh Wills](https://github.com/jwills).

[![Advanced Analytics with Spark](http://akamaicovers.oreilly.com/images/0636920056591/lrg.jpg)](http://shop.oreilly.com/product/0636920056591.do)

### Env

1版:spark1系    
2版:spark2系    

これで試した    

```
$ scala -version
Scala code runner version 2.12.0 -- Copyright 2002-2016, LAMP/EPFL and Lightbend, Inc
$ spark-shell --version
Welcome to
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /___/ .__/\_,_/_/ /_/\_\   version 2.1.0
      /_/
                        
Using Scala version 2.11.8, OpenJDK 64-Bit Server VM, 1.8.0_144
Branch 
Compiled by user jenkins on 2016-12-16T02:04:48Z
```

### Build

Pythonで動かしてみるSpark入門    
https://qiita.com/miyamotok0105/items/bf3638607ef6cb95f01b    

『Sparkによる実践データ解析』のサンプルコードの動かし方    
https://qiita.com/yu-iskw/items/aedc2fb95f508e621a20    

```
mvn clean package
```

対話形式で動かしたい場合    

```
spark-shell --master local[*]
```

### Data Sets

- Chapter 2: https://archive.ics.uci.edu/ml/machine-learning-databases/00210/
- Chapter 3: https://storage.googleapis.com/aas-data-sets/profiledata_06-May-2005.tar.gz
- Chapter 4: https://archive.ics.uci.edu/ml/machine-learning-databases/covtype/
- Chapter 5: https://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html (do _not_ use http://www.sigkdd.org/kdd-cup-1999-computer-network-intrusion-detection as the copy has a corrupted line)
- Chapter 6: https://dumps.wikimedia.org/enwiki/latest/enwiki-latest-pages-articles-multistream.xml.bz2
- Chapter 7: ftp://ftp.nlm.nih.gov/nlmdata/sample/medline/ (`*.gz`)
- Chapter 8: https://storage.googleapis.com/aas-data-sets/trip_data_1.csv.zip (from http://www.andresmh.com/nyctaxitrips/)
- Chapter 9: See https://github.com/sryza/aas/tree/master/ch09-risk/data ; included download scripts no longer work
- Chapter 10: ftp://ftp.ncbi.nih.gov/1000genomes/ftp/phase3/data/HG00103/alignment/HG00103.mapped.ILLUMINA.bwa.GBR.low_coverage.20120522.bam
- Chapter 11: https://github.com/thunder-project/thunder/tree/v0.4.1/python/thunder/utils/data/fish/tif-stack

[![Build Status](https://travis-ci.org/sryza/aas.png?branch=master)](https://travis-ci.org/sryza/aas)
