# PredictRepeatShopper
http://www.meetup.com/nj-datascience/events/229293067/    H2O Sparkling Water

## Install spark on Mac:

1. **Install Java Development Kit** from [oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
2. Add following code to your e.g. `.bash_profile`
```bash
# For Apache Spark
if which java > /dev/null; then export JAVA_HOME=$(/usr/libexec/java_home); fi
```

3. get [homebrew](http://brew.sh/)
```shell
brew update
brew install scala
brew install apache-spark
```

4. in your `.bash_profile`
```export SPARK_HOME="/usr/local/Cellar/apache-spark/1.6.1/libexec/"
export MASTER="local-cluster[3,2,1024]"
fi```


## Install [sparkling water](http://h2o-release.s3.amazonaws.com/sparkling-water/rel-1.6/1/index.html):
1. [download sparkling water here](http://h2o-release.s3.amazonaws.com/sparkling-water/rel-1.6/1/sparkling-water-1.6.1.zip)
2. unzip it
3. cd into the sparkling water directory
4. `bin/sparkling-shell --conf "spark.executor.memory=1g"`


You now have sparking water shell running on your machine. Congrats.

In the sparking shell type the following commands:

```
import org.apache.spark.h2o._
val h2oContext = H2OContext.getOrCreate(sc)
```

The last line that is output will be the path to your H20 Flow web ui.

