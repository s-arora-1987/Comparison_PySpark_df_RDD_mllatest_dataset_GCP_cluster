## Comparison of performance for collborative filtering reccomender training using PySpark df and PySpark RDD on a GCP cluster


<!-- TABLE OF CONTENTS -->
## Table of Contents

* [Motivation](#about-the-project)
* [Libraries Used](#prerequisites)
* [Files](#files)
* [Summary of Results](#summary)
* [Contact](#contact)
* [Acknowledgements](#acknowledgements)

<!-- ABOUT THE PROJECT -->
## Motivation

PySpark offers two options for storing a data table: Pandas like data frame structure (not exactly same as Pandas df), resilient distributed dataset (RDD) data structure. When it comes to simple low level actions on tables in a dataset, it is known that PySpark data frames are faster than RDD [1,2]. But that information alone does not tell much about how they compare in higher-level modeling actions, in terms of overall training error and training time for predictive model (e.g. recommender systems). Do dataframes enable faster training and better learning accuracy than RDD? Also, are they fast in making prediction post training?

### Libraries Used
I used following libraries for building this project:

- pandas 
- pyspark 2.3.2
- time 
- math
- matplotlib

### Files
The notebook  established a 'Comparison_PySpark_df_RDD_mllatest_dataset_GCP_cluster.ipynb' implements the code that compares training performance of a dataframe based collaborative-filtering recommender model with that of RDD based model. 

### Summary of Results
The results showed that both the training and the prediction of recommender system using dataframe were considerably faster as compared to ALS using RDD, without any compromise in learning accuracy. 

![RMSE](https://github.com/s-arora-1987/Comparison_PySpark_df_RDD_mllatest_dataset_GCP_cluster/blob/main/rmse_ALS.png)

![TrainingTime](https://github.com/s-arora-1987/Comparison_PySpark_df_RDD_mllatest_dataset_GCP_cluster/blob/main/time_ALS.png)

For further details of implementation and results, please see the medium blog post [Efficiency comparison between collaborative filtering using PySpark data frames and that using PySpark RDD"](https://sarora-69521.medium.com/efficiency-comparison-between-collaborative-filtering-using-pyspark-data-frames-and-that-using-88ff4e785679) 

### Contact
sa08751@uga.edu

### Acknowledgements
* [link 1](https://www.adsquare.com/comparing-performance-of-spark-dataframes-api-to-spark-rdd/)
* [link 2](https://spark.apache.org/docs/2.2.0/ml-collaborative-filtering.html) 


