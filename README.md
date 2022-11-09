# scRNAseq_analyze
Analyze scRNAseq and spatial transcriptome with scanpy.

## 文件结构

请将数据置于如下位置：
```angular2html
│
├─data
│  │  
│  ├─ SC-HCC-P2-Tumor
│  │
│  ├─ SC-HCC-P3-Tumor
│  │
│  └─ ST-HCC-2L
└─src
   │  
   ├─ process_cluster_P2.ipynb
   │
   ├─ process_cluster_2L.ipynb
   │
   └─ classifier.ipynb
```

## 运行
   Run (Seruat / Scanpy / scCancer) package to do data quality control, pre-processing, clustering and UMAP visualization .
  Try to label the major cell types based on the highly expressed genes in each cluster (may refer to scCancer package) 
   
```bash
python process_cluster_P2.ipynb
```
Train a classifier on one scRNAseq dataset and test on the other.
```bash 
python classifier.ipynb
```
Run (Seruat / Scanpy / stCancer) package to do data quality control, pre-processing 
   Use unsupervised clustering and differential expression analysis to define the major sub-regions of the HCC-2L based on the ST data 
   Try to locate the major cell types (use the results from the above scRNAseq analysis) in HCC-2L and compare the cell type enrichments among different sub-regions 

```bash
python process_cluster_2L.ipynb
```

## 
