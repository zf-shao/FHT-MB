## FHT-MB
This is the implementation for our paper Filter-enhanced Hypergraph Transformer for Multi-Behavior Sequential Recommendation, accepted by ICASSP'24.


## Datasets
Tmall: https://tianchi.aliyun.com/dataset/649

RetailRocket: https://www.kaggle.com/datasets/retailrocket/ecommerce-dataset

## Environments:
We implemented all of our programs on a machine with Intel(R) Xeon(R) Gold 6150 CPU, 29GB memory, and NVidia Gefoce GTX 3090.

## About Scales:
The granularity of periodic behavior habits is defined as “scales” in our method. 

Referring to equation (2) in the paper, we define “scales” as the denominator to the sequence length, which are actually parameters. The function of “scales” is to partition the multi-behavior sequence of users into sub-sequences with different scale settings, and then further generate scale-specific behavior embedding for better recommendation, which corresponds to the behavior habits changes mentioned in our paper, i.e., item transitions with different periodic trends. We set two different scale settings in the paper, and they are searched by the average sequence length of different datasets. 
