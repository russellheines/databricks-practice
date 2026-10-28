This repo contains examples of training a model with scikit-learn and SparkML, as well as using MLflow.

- scikit-learn runs on a single machine (the Driver node). It loads the entire dataset into RAM, which makes it very fast for small datasets, but causes a crash (Out of Memory error) when handling hundreds of gigabytes of data.
- SparkML splits the dataset across a cluster of multiple worker machines. Instead of processing the data sequentially, it performs operations in parallel, allowing the pipeline to scale seamlessly to terabytes of data without code changes.

Notebooks:
- 01_titantic_sklearn - Example of training a random forest classifier using scikit-learn.
- 02_titantic_sparkml - Example of training a random forest classifier using Apache Spark's MLlib library.
- 03_titantic_mlflow - Example of using MLflow to log experiments and register models.
