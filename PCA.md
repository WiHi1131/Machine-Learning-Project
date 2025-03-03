<a href = "https://wihi1131.github.io/Machine-Learning-Project/">Home</a>

# PCA

Principal Component Analysis, or PCA, is a means by which to reduce the complexity of a dataset. Using sophisticated linear algebra and coding techniques, we can use PCA to eliminate unnecessary parts of our data that do not give us a lot of information. By using PCA as a statistical "editing" technique, we can learn which parts, or "dimensions" of our dataset summarize that dataset the best. Reduced datasets can often be easier to use to train machine learning models. 

# Data

## Before Cleaning

<div>
  <img src = "images/pre_pca_data.PNG" title = "Pre-PCA Data" alt = "Pre-PCA Data">
  <div>
    <p>
      <b>This is the data that PCA will be performed on, before cleaning. Note that the "label" in this case would be placement. Note also the many quantitative features. Time measurements (game length and time eliminated) are in seconds. Link to data: <a href = "https://github.com/WiHi1131/Machine-Learning-Project/blob/main/data/PRE_PCA.csv">Pre-PCA Data</a></b>
    </p>
  </div>
</div>

## After Cleaning

<div>
  <img src = "images/PCA_clean.PNG" title = "PCA Data" alt = "Cleaned PCA Data">
  <div>
    <p>
      <b>This is the data that PCA will be performed on, after cleaning. Note that the "placement" column has been removed, and both non-quantitative columns have also been removed. Link to data: <a href = "https://github.com/WiHi1131/Machine-Learning-Project/blob/main/data/PCA.csv">Cleaned PCA Data</a></b>
    </p>
  </div>
</div>

# Visualizations of the Data

<div>
  <img src = "images/PCA_2D_Vis.png" title = "PCA 2D" alt = "PCA 2D Plot">
  <div>
    <p>
      <b>This is a scatterplot of the two principal components when PCA is performed on the data and the dimensions of the data are reduced to two. Note that data was scaled before PCA was performed.</b>
    </p>
  </div>
</div>

<div>
  <img src = "images/PCA_3D_Vis.png" title = "PCA 3D" alt = "PCA 3D Plot">
  <div>
    <p>
      <b>This is a 3D plot of the three principal components remaining when PCA is performed on the data and dimensions are reduced to three.</b>
    </p>
  </div>
</div>

<a href = "https://wihi1131.github.io/Machine-Learning-Project/">Home</a>
