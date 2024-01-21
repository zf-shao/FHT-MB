## FHT-MB
This is the implementation for our paper Filter-enhanced Hypergraph Transformer for Multi-Behavior Sequential Recommendation, accepted by ICASSP'24.


## Datasets
Tmall: https://tianchi.aliyun.com/dataset/649

RetailRocket: https://www.kaggle.com/datasets/retailrocket/ecommerce-dataset

## Environments:
We implemented all of our programs on a machine with Intel(R) Xeon(R) Gold 6150 CPU, 29GB memory, and NVidia Gefoce GTX 3090.

## Train:
python run_FHT.py --model=[FHT] --dataset=[retail_beh] --gpu_id=[0] --batch_size=[2048]

## Description:
Firstly, our method is to solve the problem of sequential recommendation in multi-behavior scenarios, which belongs to the category of sequential learning. Additionally, one crucial technique of our method is the Fast Fourier Transform, which is essential in the digital signal processing area. Secondly, as shown in Fig.1, Fig.2 and Paragraph 2 in the introduction section, our method focuses on exploring multi-behavior dependencies(e.g., add-to-cart, add-to-favorite, and click behaviors) while incorporating the evolution of sequential information into the recommendation framework, so it's straightforward from the paper's structure that our method emphasizes "Multi-Behavior Sequential Recommendation."

About 'Scales':
The granularity of periodic behavior habits is defined as “scales” in our method (referer to [MBHT](https://github.com/yuh-yang/MBHT-KDD22)). 

Referring to equation (2) in the paper, we define “scales” as the denominator to the sequence length, which are actually parameters. The function of “scales” is to partition the multi-behavior sequence of users into sub-sequences with different scale settings, and then further generate scale-specific behavior embedding for better recommendation, which corresponds to the behavior habits changes mentioned in our paper, i.e., item transitions with different periodic trends. We set two different scale settings in the paper, and they are searched by the average sequence length of different datasets. 

## Acknowledgement:
@inproceedings{shao2024filter,
  title={Filter-enhanced hypergraph transformer for multi-behavior sequential recommendation},
  author={Shao, Zhufeng and Wang, Shoujin and Lu, Wenpeng and Zhang, Weiyu and Guan, Hongjiao and Zhao, Long},
  booktitle={IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)},
  pages={1--5},
  year={2024},
  organization={IEEE}
}
