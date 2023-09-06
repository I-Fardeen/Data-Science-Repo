# PySpark Cheat Sheet 🐍🔥

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the world of PySpark, the Python library for Apache Spark! This cheat sheet provides essential PySpark commands and code examples to help you work with big data and distributed computing. Don't forget to follow the author, [Fardeen Ahmad Khan](https://github.com/I-Fardeen), for more PySpark insights and updates! 🙌

🚀 **Getting Started with PySpark**:
To start working with PySpark, make sure you have it installed and a SparkSession initialized.
```python
from pyspark.sql import SparkSession

spark = SparkSession.builder \
    .appName("MyPySparkApp") \
    .getOrCreate()
```

🗂️ **Loading Data**:
Load data into a Spark DataFrame from various sources like CSV, Parquet, or Hive.
```python
df = spark.read.csv("data.csv", header=True, inferSchema=True)
```

📝 **Basic DataFrame Operations**:
Perform common DataFrame operations like selecting, filtering, and aggregating data.
```python
df.select("column1", "column2")
df.filter(df["column1"] > 10)
df.groupBy("column1").agg({"column2": "avg"})
```

🔧 **Data Preprocessing**:
Prepare and clean data using PySpark transformations.
```python
from pyspark.ml.feature import StringIndexer, VectorAssembler

indexer = StringIndexer(inputCol="category", outputCol="category_index")
assembler = VectorAssembler(inputCols=["feature1", "feature2"], outputCol="features")
```

📊 **Machine Learning with PySpark**:
Build and train machine learning models using PySpark's MLlib.
```python
from pyspark.ml.regression import LinearRegression

lr = LinearRegression(featuresCol="features", labelCol="label")
model = lr.fit(train_data)
```

🔄 **Model Evaluation**:
Evaluate model performance with various metrics.
```python
from pyspark.ml.evaluation import RegressionEvaluator

evaluator = RegressionEvaluator(labelCol="label", predictionCol="prediction", metricName="rmse")
rmse = evaluator.evaluate(predictions)
```

💾 **Saving Models**:
Save trained models for future use.
```python
model.save("my_model")
```

📋 **Running Spark SQL Queries**:
Execute SQL queries on Spark DataFrames.
```python
df.createOrReplaceTempView("mytable")
result = spark.sql("SELECT column1, COUNT(*) FROM mytable GROUP BY column1")
```

🔗 **Working with RDDs**:
Interact with Resilient Distributed Datasets (RDDs) for lower-level Spark operations.
```python
rdd = spark.sparkContext.parallelize([1, 2, 3, 4, 5])
```

Explore these PySpark commands and examples to harness the power of distributed computing for your data analysis tasks. Happy Sparking! 🔥🐍

Made with :heart: by **Fardeen Ahmad Khan**
