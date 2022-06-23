## 数据集使用方法

#### 非重叠社区

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



