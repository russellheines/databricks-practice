This repo contains examples of training a model with scikit-learn and SparkML, as well as using MLflow.

- scikit-learn runs on a single machine (the Driver node). It loads the entire dataset into RAM, which makes it very fast for small datasets, but causes Out of Memory errors when the dataset is too large.
- SparkML splits the dataset across a cluster of worker machines. Instead of processing the data sequentially, it performs operations in parallel, allowing the pipeline to scale seamlessly.

Notebooks:
- 01_titanic_sklearn - Example of training a random forest classifier using scikit-learn.
- 02_titanic_sparkml - Example of training a random forest classifier using Apache Spark's MLlib library.
- 03_titanic_mlflow - Example of using MLflow to log experiments and register models.
- 04_titanic_hyperopt - Example of using Hyperopt to find the best hyperparameters.
- 05_titanic_inference - Examples of interference using native Pandas, Spark UDF, and native Spark pipelines.
