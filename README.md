This repo contains example notebooks using scikit-learn and SparkML.

- scikit-learn runs on a single machine (the Driver node). It loads the entire dataset into RAM, which makes it very fast for small datasets, but causes a crash (Out of Memory error) when handling hundreds of gigabytes of data.
- SparkML splits the dataset across a cluster of multiple worker machines. Instead of processing the data sequentially, it performs operations in parallel, allowing the pipeline to scale seamlessly to terabytes of data without code changes.