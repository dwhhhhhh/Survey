## TLS分割&识别（H&E图像）

| Model (Backbone/Pipeline)                                    | Task                                                         | Dataset                                                   | Performance                                     | Article Title                                                | Publication Source & Date                  | Link                                               |
| ------------------------------------------------------------ | ------------------------------------------------------------ | --------------------------------------------------------- | ----------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------ | -------------------------------------------------- |
| Encoder: UNet++ <br />Decoder: EfficientNet-b0               | Segmentation                                                 | Pre-training: ImageNet, Fine-tuning: TCGA-LUAD, TCGA-LUSC | Dice: 89%                                       | Next-generation lung cancer pathology: Development and validation of diagnostic and prognostic algorithms | *Cell Report Medicine*, September 17, 2024 | https://doi.org/10.1016/j.xcrm.2024.101697         |
| ResNet50                                                     | Segmentation                                                 | Pre-training: Camelyon16, Fine-tuning: GDPH               | intra-class correlation coefficient: 0.894      | Computerized tertiary lymphoid structures density on H&E-images is a prognostic biomarker in resectable lung adenocarcinoma | *iScience*, September 15, 2023             | https://doi.org/10.1016/j.isci.2023.107635         |
| Segmentation: morphological image processing, Classification: decision tree | Segmentation, Classification of TLSs into 3 maturation states | 7 subsets of TCGA                                         | Segmentation: N/A, Classification accuracy: 96% | Development and Validation of a Machine Learning Model for Detection and Classification of Tertiary Lymphoid Structures in Gastrointestinal Cancers | *JAMA Netw Open*, January 24, 2023         | https://doi.org/10.1001/jamanetworkopen.2022.52553 |
| EfficientNet-b0                                              | Segmentation                                                 | TCGA-ESCC, TCGA-NSCLC                                     | Dice: 91%                                       | Deep learning on tertiary lymphoid structures in hematoxylin-eosin predicts cancer prognosis and immunotherapy response | *npj Precision Oncology*, March 22, 2024   | https://doi.org/10.1038/s41698-024-00579-w         |
| UNI (DINOv2)                                                 | 34 representative CPath tasks                                | TCGA, Mass-100K                                           | N/A                                             | Towards a general-purpose foundation model for computational pathology | *Nature Medicine*, March 19, 2024          | https://doi.org/10.1038/s41591-024-02857-3         |

## 在H&E图像上表现较好的一些基础模型

[***UNI***](https://doi.org/10.1038/s41591-024-02857-3), [*Nature Medicine*](https://www.nature.com/nm)

[***PathoDuet***](https://doi.org/10.1016/j.media.2024.103289), [Medical Image Analysis](https://www.sciencedirect.com/journal/medical-image-analysis)

[***CTransPath***](https://doi.org/10.1016/j.media.2022.102559), [Medical Image Analysis](https://www.sciencedirect.com/journal/medical-image-analysis)

[***Virchow***](https://doi.org/10.1038/s41591-024-03141-0), [*Nature Medicine*](https://www.nature.com/nm)

[***REMEDIS***](https://doi.org/10.1038/s41551-023-01049-7), [*Nature Biomedical Engineering*](https://www.nature.com/natbiomedeng)



## 基于组学信息的深度细胞聚类模型 ##

| Model   | Data         | Category | Article Title                                                | Publication Source & Date                        | Link                                       | Remark                                                       |
| ------- | ------------ | -------- | ------------------------------------------------------------ | ------------------------------------------------ | ------------------------------------------ | ------------------------------------------------------------ |
| ADClust | scRNA-seq    | AE       | A parameter-free deep embedded clustering method for single-cell RNA-seq data | *Briefings in Bioinformatics*, May 06, 2022      | https://doi.org/10.1093/bib/bbac172        | No need to predefine the number of clusters                  |
| DSSC    | sp-scRNA-seq | GNN      | A model-based constrained deep learning clustering approach for spatially resolved single-cell data | *Genome Research*, September 28, 2022            | https://doi.org/10.1101/gr.276477.121      | Integration of spatial information of cells in the clustering process; graph attention mechanism |
| scDFC   | scRNA-seq    | AE       | scDFC: A deep fusion clustering method for single-cell RNA-seq data | *Briefings in Bioinformatics*, June 06, 2023     | https://doi.org/10.1093/bib/bbad216        | Dual AE captures attribute features and structural features, respectively |
| scDCC   | scRNA-seq    | AE       | Model-based deep embedding for constrained clustering analysis of single cell RNA-seq data | *Nature Communications*, March 25, 2021          | https://doi.org/10.1038/s41698-024-00579-w | Domain knowledge is integrated in the clustering process     |
| scDSC   | scRNA-seq    | GNN      | Deep structural clustering for single-cell RNA-seq data jointly through autoencoder and graph neural network | *Briefings in Bioinformatics*, February 16, 2022 | https://doi.org/10.1093/bib/bbac018        | Information transfer mechanism; mutual supervision strategy  |

## 基于形态信息的深度细胞聚类模型 ##

| Model     | Clustering Type                           | Category            | Article Title                                                | Publication Source & Date                     | Link                                              |
| --------- | ----------------------------------------- | ------------------- | ------------------------------------------------------------ | --------------------------------------------- | ------------------------------------------------- |
| SpaCell   | Cell-type clustering                      | CNN&AE              | SpaCell: integrating tissue morphology and spatial gene expression to predict disease cells | *Bioinformatics*,  December 01, 2019          | https://doi.org/10.1093/bioinformatics/btz914     |
| stLearn   | Cell-type clustering                      | N/A                 | Robust mapping of spatiotemporal trajectories and cell–cell interactions in healthy and diseased tissues | *Nature Communications*, November 25, 2023    | https://doi.org/10.1038/s41467-023-43120-6        |
| SpaGCN    | Spatial clustering & Cell-type clustering | GCN                 | SpaGCN: Integrating gene expression, spatial location and histology to identify spatial domains and spatially variable genes by graph convolutional network | *Nature Methods*, October 28, 2021            | https://doi.org/10.1093/bib/bbac172               |
| SEDR      | Spatial clustering & Cell-type clustering | VAE                 | Unsupervised spatially embedded deep representation of spatial transcriptomics | *Genome Medicine*, January 12, 2024           | https://doi.org/10.1186/s13073-024-01283-x        |
| CCST      | Spatial clustering & Cell-type clustering | DGI                 | Cell clustering for spatial transcriptomics data with graph neural networks | *Nature Computational Science*, June 27, 2022 | https://doi.org/10.1038/s43588-022-00266-5        |
| SCAN-IT   | Spatial clustering & Cell-type clustering | DGI                 | Model-based deep embedding for constrained clustering analysis of single cell RNA-seq data | *BMVC*, October 11, 2022                      | https://pmc.ncbi.nlm.nih.gov/articles/PMC9552951/ |
| STAGATE   | Spatial clustering & Cell-type clustering | GAT                 | Deciphering spatial domains from spatially resolved transcriptomics with an adaptive graph attention auto-encoder | *Nature Communications*, April 01, 2022       | https://doi.org/10.1038/s41467-022-29439-6        |
| SpaceFlow | Spatial clustering & Cell-type clustering | GNN                 | Identifying multicellular spatiotemporal organization of cells with SpaceFlow | *Nature Communications*, July 14, 2022        | https://doi.org/10.1038/s41467-022-31739-w        |
| GraphST   | Spatial clustering & Cell-type clustering | self-supervised GCL | Spatially informed clustering, integration, and deconvolution of spatial transcriptomics with GraphST | *Nature Communications*, March 01, 2023       | https://doi.org/10.1038/s41467-023-36796-3        |

