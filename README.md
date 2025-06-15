# 🖼️ Image Clustering – Unsupervised Learning Project
Image Clustering is an end‑to‑end computer‑vision pipeline that automatically groups unlabeled images into visually similar clusters.
It combines a pre‑trained Convolutional Neural Network (CNN) for feature extraction with classic unsupervised learning algorithms—K‑Means for clustering and t‑SNE for 2‑D visualisation.
|                       | Details                                                                                                            |
| --------------------- | ------------------------------------------------------------------------------------------------------------------ |
| **Learning Paradigm** | Unsupervised                                                                                                       |
| **Algorithms**        | CNN (ResNet‑18) features → K‑Means, t‑SNE                                                                          |
| **Primary Library**   | PyTorch / Torchvision                                                                                              |
| **Dataset**           | Any Torchvision image set (default: **CIFAR‑10**)                                                                  |
| **Output**            | • Cluster assignments for every image<br>• 2‑D scatter plot coloured by cluster<br>• Sample image grid per cluster |

# 📊 Key Steps
Load Images : 
Torchvision handles download & preprocessing (resize → tensor → normalise).

Feature Extraction : 
A pre‑trained ResNet‑18 (last FC layer removed) converts each image to a 512‑dimensional embedding.

Dimensionality Reduction : 
Optional PCA (for speed) followed by t‑SNE for 2‑D visualisation.

Clustering : 
K‑Means assigns each embedding to one of k clusters.
Alternative algorithms (DBSCAN, Agglomerative) can be enabled with a flag.

Visual Inspection : 

• Scatter plot coloured by cluster

• n sample thumbnails per cluster for qualitative sanity‑check
