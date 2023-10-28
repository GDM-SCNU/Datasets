## 数据集使用方法

#### complex networks

加载数据集

```python
"""
import pickle as pkl
with open(dataset_addr, "rb")as f:
    dataset = pkl.load(f)
```

#### complext networks
- Blogcatalog
- Citeseer
- Cora
- Cornell
- Flickr
- Pubmed
- Texas
- UAI2010
- Washington
- Wisconsin

#### topology networks
- Email
- Wiki

#### multiplex networks
- ACM
- Amazon
- DBLP
- IMDB

#### dynamic networks
- Cellphone
- DBLP
- Dynamic_cora
- highSchool
- Java

#### overlapping complex networks

```python
"""
	数据集格式
	'name' # 数据集名称 
    'topo' # 拓扑 :csr_matrix
    'attr' # 属性 :csr_matrix
    'label'# 标签 :csr_matrix n×k, 1表示隶属该社区，否则为0
    
    文件名：数据集
    Fb_X:Facebook X
    mag_chem:Chemistry, mag_cs:Computer Science, mag_med:Medicine, mag_end: Engineering
"""
import pickle as pkl
with open("cora.pkl",'rb') as f:
    data = pkl.load(f) # data['...']
```

References: 

[1] Oleksandr S, Günnemann S (2019) Overlapping Community Detection with Graph Neural Networks. preprint arXiv

#### 说明

1. 所有数据集均带有节点自环
2. 数据集中，除标签外，其余矩阵仅有1或0标志