# EchoEA

code for **"EchoEA: Echo Information between Entities and Relations for Entity Alignment"**

## Environment

- PyTorch 1.8.1 + cuda 10.2
- apex (alternative)
- torch-scatter, torch-sparse, torch-cluster, torch-spline-conv, torch-geometric

```shell
pip install torch-scatter -f https://pytorch-geometric.com/whl/torch-1.8.1+cu102.html
pip install torch-sparse -f https://pytorch-geometric.com/whl/torch-1.8.1+cu102.html
pip install torch-cluster -f https://pytorch-geometric.com/whl/torch-1.8.1+cu102.html
pip install torch-spline-conv -f https://pytorch-geometric.com/whl/torch-1.8.1+cu102.html
pip install torch-geometric
```

## How to Run

Prepare attribute similarity and value similarity:
```shell
python sim_based_on_attr_n_value.py
```

Complete version:
```shell
python train.py
```
Ablation:
- Basic: train_basic.py
- w/o PAN: train_basic_woPAN.py
- w/o EN: train_basic_woEN.py
- w/o CAN: train_basic_woCAN.py

## Datasets

* ent_ids_1: ids for entities in source KG;
* ent_ids_2: ids for entities in target KG;
* ref_ent_ids: entity links encoded by ids;
* triples_1: relation triples encoded by ids in source KG;
* triples_2: relation triples encoded by ids in target KG;

## Acknowledgement

We cite the datasets and codes of these repos: GCN-Align, RREA, EMGCN, RAGA. Thanks for their great contributions!

0. GCN-Align: [paper](https://www.aclweb.org/anthology/D18-1032.pdf), [code](https://github.com/1049451037/GCN-Align)
1. RREA: [paper](https://arxiv.org/pdf/2008.07962.pdf), [code](https://github.com/MaoXinn/RREA)
2. RAGA: [paper](https://arxiv.org/abs/2103.00791), [code](https://github.com/zhurboo/RAGA)
3. EMGCN: [paper](https://ieeexplore.ieee.org/document/9262038), [code](https://github.com/vinhsuhi/EMGCN)

