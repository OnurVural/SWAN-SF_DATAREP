# SWAN-SF_DATAREP

Three solar flare classification strategies using the SWAN-SF dataset are assessed by focusing on data representations. Graph-based, time series-based, and vector-based methods to ascertain the optimal approach for representing the characteristics of the SWAN-SF dataset, which relies on photospheric magnetic field parameters, are explored. The graph representation aims to capture spatial dependencies, the time series representation aims to uncover temporal patterns, and the vector representation aims to capture the last timestamp of the multivariate time series closest in time to the flaring event. 

# Exec. Details

* DATA/ contains data points, in case of training all components from scratch, the folders to keep data files must be placed under here (names and paths can be specified while running the relevant notebook cells).
 For starting from scratch, partitions 1 and 2 can be used for training and testing, else graph structures created from those partitions are also added here!

* MODELS/ contains pre-trained models
  
* CODE/ contains the necessary modules, in case of training all components from scratch, to create all the graphs from the bottom-up, the execution must start from hss.ipynb and euclidian_dist.ipynb. The details for each notebook file is as follows:
  - hss.ipynb: Includes the creation of graphs with correlation matrix, training and testing downstream classifiers, laplacian node embeddings.
  - euclidian_dist.ipynb: Includes the creation of graphs with Euclidian distance matrix, training and testing downstream classifiers, laplacian node embeddings.
  - Node2vec.ipynb: Includes the node2vec embedding algorithm, training and testing downstream classifiers with node embedding results.
  - gnc_cor.ipynb: Includes creation, training and testing of a 2-layer graph convolutional network for graphs created by correlation matrix.
  - gnc_ed.ipynb: Includes creation, training and testing of a 2-layer graph convolutional network for graphs created by correlation matrix.
  - sampling.ipynb: Includes a test for undersampling
  - COMING SOON: In a few months, a single complete module allowing all operations is planned to come!
 
* All experiments are done with python 3.9.13, pytorch 2.1.0, numpy 1.25.2, networkx 2.8.8

  
  
