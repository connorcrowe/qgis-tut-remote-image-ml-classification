# qgis-tut-remote-image-ml-classification
This is an assignment for a course completed called Machine Learning in GIS. The purpose was to learn and practice GIS and geospatial machine learning skills. The data used was provided by the course.
**Specific Skills:**
- Remote imagery, imagery bands, imagery management
- Image classification
- Supervised classification
- Unsupervised classification

## Problem
The objective was to classify different land use and land cover (LULC) types by using different machine learning classification methods on remote imagery from Bonn, Germany. The classification will be into 3 classes.
- Urban/developed (red)
- Vegetation (green)
- Water (blue)

## Solution
**K-Means Clustering**
An unsupervised k-means clustering was done using OfeoToolbox. The resulting classification appears to classify greenery accurately, but vastly under-classifies urban areas and considers them to be water.
![](/images/kmeans.png)

**Decision Tree & Random Forest**
For the decision tree and random forest classification, training and validation points were selected from the image since the methods are supervised and require training data. Both algorithms improved with a greater selection of training data to a point. Both algorithms appeared to classify more accurately than the K-means method, especially since it didn't mistake roads/development for water (as much). The random forest outperformed the decision tree, as was expected. The decision tree falsely identified water more often, and failed to identify urban/developed area more often.
![](/images//dt.png) ![](/images/rf.png)

**Support Vector Machine**
The suppor vector machine method is also supervised and therefore required sampling some of the image for training and validation. The SVM performed overall similarly to the random forest method. The SVM was better at identifying roads as urban and not water compared to the RF, and the SVM was able to properly distinguish bridges. It did however under classify urab/developed areas in favour of greenery a little bit more than the random forest did. 
![](/images/svm.png)


