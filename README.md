# SWAN-SF_DATAREP

Three solar flare classification strategies using the SWAN-SF dataset are assessed by focusing on data representations. Graph-based, time series-based, and vector-based methods to ascertain the optimal approach for representing the characteristics of the SWAN-SF dataset, which relies on photospheric magnetic field parameters, are explored. The graph representation aims to capture spatial dependencies, the time series representation aims to uncover temporal patterns, and the vector representation aims to capture the last timestamp of the multivariate time series closest in time to the flaring event. 
![graphs2](https://github.com/OnurVural/SWAN-SF_DATAREP/assets/63475639/ee249e58-b816-4664-8374-a4f44b4fd7dd)

# Content Details

* <code> DATA/ </code> contains data points, in case of training all components from scratch, the folders to keep data files must be placed under here (names and paths can be specified while running the relevant notebook cells).
 For starting from scratch, partitions 1 and 2 can be used for training and testing, else graph structures created from those partitions are also added here!

* <code>MODELS/</code> contains pre-trained models
  
* <code> CODE/ </code> contains the necessary modules, in case of training all components from scratch, to create all the graphs from the bottom-up, the execution must start from hss.ipynb and euclidian_dist.ipynb. The details for each notebook file is as follows:
  - <code>hss.ipynb</code>: Includes the creation of graphs with correlation matrix, training and testing downstream classifiers, and Laplacian node embeddings.
  - <code>euclidian_dist.ipynb</code>: Includes the creation of graphs with Euclidian distance matrix, training and testing downstream classifiers, and Laplacian node embeddings.
  - <code>Node2vec.ipynb</code>: Includes the node2vec embedding algorithm, training and testing downstream classifiers with node embedding results.
  - <code>gnc_cor.ipynb</code>: Includes creation, training and testing of a 2-layer graph convolutional network for graphs created by correlation matrix.
  - <code>gnc_ed.ipynb</code>: Includes creation, training and testing of a 2-layer graph convolutional network for graphs created by correlation matrix.
  - <code>tsMethod.ipynb</code>: Includes training and testing of components for vector-based LTV classification and time series-based MVTS classification.
  - <code>sampling.ipynb</code>: Includes a test for undersampling
  - <code>module1.ipynb</code>: This module is a step-by-step guide to run all experiments and document results in a single notebook file
    
# Execution Details 
* To replicate the experiments and document results in a single file, the newly created module1.ipynb file is sufficient.
* The other notebook files give a more detailed demonstration of the reasoning behind the corresponding methods for each data representation technique regarding the selection of methodologies, parameters etc.
* Prerequisites: To use all of the partitions, you need to download the SWAN-SF partitions from: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EBCFKM
After downloading, the partitions have to be placed under DATA folder with their original names
* As the experiments are being made, the models will be saved under MODELS folder
* All experiments are done with python 3.9.13, pytorch 2.1.0, numpy 1.25.2, networkx 2.8.8

  
  
