This repo contains examples of training a model with scikit-learn and SparkML, as well as using MLflow.

- scikit-learn runs on a single machine (the Driver node). It loads the entire dataset into memory, which makes it fast for small datasets, but causes Out of Memory errors when the dataset is too large.
- SparkML splits the dataset across a cluster of worker machines. Instead of processing the data sequentially, it performs operations in parallel, allowing the pipeline to scale seamlessly.

Notebooks:
- 01_titanic_datasets - Loads training and test datasets into Delta tables
- 02_titanic_sklearn - Trains a random forest classifier using scikit-learn.
- 03_titanic_sparkml - Trains a random forest classifier using Apache Spark's MLlib library.
- 04_titanic_inference - Performs inference using native Pandas, Spark UDF, and native Spark pipelines.
- 05_titanic_pipeline - Defines a pipelipe to orchestrate the workflow end-to-end.