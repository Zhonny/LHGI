# LHGI
The code is for paper "Unsupervised Embedding Learning for Large-Scale Heterogeneous Networks Based on Metapath Graph Sampling"

you need pytorch and torch_geometric

How to install geometric click in :https://pytorch-geometric.readthedocs.io/en/latest/install/installation.html

test data in release LHGI1.0

How to build your dataset:

from torch_geometric.data import HeteroData

data = HeteroData()

data['business'].x=torch.eye(2614)

data['reservation'].x = torch.eye(2)

data['service'].x=torch.eye(2)

data['stars_level'].x = torch.eye(9)

data['user'].x = torch.eye(1286)

data['business'].y =yy #you can build node label you wanted,like torch.tensor([0,1,0,1,2,3,0,1])

data['user'].num_nodes = 1286
