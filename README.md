## 数据集使用方法

#### complex networks

加载数据集

```python
"""
	数据集格式
	'name' # 数据集名称 
    'topo' # 拓扑 :csr_matrix: int32
    'attr' # 属性 :csr_matrix: float64
    'label'# 标签 :ndarray：int64
"""
import pickle as pkl
with open("cora.pkl",'rb') as f:
    data = pkl.load(f) # data['...']
```

#### 转为DGL

```python
import dgl
graph = dgl.from_scipy(data['topo']) # 数据集中自带自环
```

#### csr_matrix转格式

```python
# 转ndarray
data['topo'].toarray()
# 转矩阵
data['topo'].todense()
```



#### topology networks

加载数据集

```python
"""
	数据集格式
	'name' # 数据集名称 
    'topo' # 拓扑 :csr_matrix: int32
    'label'# 标签 :ndarray：int64
"""
import pickle as pkl
with open("cora.pkl",'rb') as f:
    data = pkl.load(f) # data['...']
```



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



