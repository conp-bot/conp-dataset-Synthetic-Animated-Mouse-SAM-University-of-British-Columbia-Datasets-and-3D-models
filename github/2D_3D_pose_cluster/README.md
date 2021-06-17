# 2D/3D pose clustering

The following code are implemented:

To classify the 2D and 3D poses, we used an unsupervised clustering algorithm called PhenoGraph. Each 2D/3D pose matrix with N rows (each containing all joints from a frame) is partitioned into clusters by a graph that represents their similarity. The graph is built in two steps, first it finds k nearest neighbors for each pose (using Euclidean distance) resulting in N sets of k nearest neighbors. In the second step, a weighted graph is built such that the weight between nodes depends on the number of neighbors they share. Louvain community detection is then performed on this graph to partition the graph that maximizes modularity.


## Usage

Requirements:
- python3
- pytorch
- torchvision
- numpy
- scipy
- scikit-learn
- phenograph

To classify the 2D and 3D poses with coordinates in CSV file:

Run:

```
python 2D_3D_pose_cluster.py

```

Expected output: Color codeed cluster of  2D and 3D poses.
Expected run time for demo on a "normal" desktop computer: Several minutes.


