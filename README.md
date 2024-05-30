The diffrent files involve scripts used to answer the four research questions and the Python code for predicting software defects based on sparse autoencoder for feature selection
and Support Vector Machine for classification.

-- RQ1 SelectRelevantMetrics
In this script, we focus on identifying metrics with higher weights as they are likely to be more informative in capturing faultrelated patterns. We apply ranking mechanism to select the top 10 metrics
with the highest weights. The set of identified important metrics is then used in the binary classification phase. Then the the feature set is restricted to only include the metrics considered most relevant by the autoencoder. These steps
are ensured by incorporating cross-validation at different stages of the analysis.

--RQ2 AverageMetricsValuesforDefectNonDefectClasses
In this script, the results RQ1 are used to identify the top metrics in the bottleneck layer associated with defect identification. We calculate the average values for each metric among the set of defective entities.
This provides a quantitative representation of the typical characteristics associated with defects. Similarly, we collect metric values for non-defective entities. The average metric values of defective classes are compared to nondefective
entities. The objective is establish thresholds that serve as indicators for defect identification based on whether a metric value falls below or exceeds the established levels.

--RQ3 SubsetMetricsforDefectPrediction
the results obtained from the previous RQ1 identifying the most 10 relevant metrics in the bottelenk for each project is used. The occurrence rate of each metric among all projects is computed to determine its overall importance. By
analyzing the frequency of occurrence of each metric across all projects, we can identify the most important metrics in the context of the entire bottleneck layer.

--RQ4 USAE_ParametersSet_1 USAE ParametersSet_2
In these scripts, we explore various parameters that govern the architecture of the unsupervised SAE on its effectiveness in predicting defects. The objective is to assess the extent to which adjusting different parameters can
lead to improvements in the autoencoder’s predictive performance. By systematically varying parameters such as the number of hidden layers, the size of the bottleneck layer, and the sparsity constraints, the study aims to elucidate
their influence on the autoencoder’s ability to accurately identify and classify defect instances.

 
--SupervisedSparseAutoencoder  --SemiSupervisedSparseAutoencoder --UsupervisedSparseAutoencode
In these scripts, we first employ supervised feature selection approaches (SupervisedSparseAutoencoder), incorporating widely-used methods like Principal Component Analysis (PCA), Information Gain (IG), and Recursive Feature Elimination (RFE) in combination 
with Support Vector Machines (SVM) for classification. Secondly, we delve into the realm of semi-supervised learning (SemiSupervisedSparseAutoencoder) by using sparse autoencoders for feature selection alongside SVM for classification. 
Finally, we explore the potential of unsupervised sparse autoencoders (UsupervisedSparseAutoencode), which will serve the dual purpose of feature extraction and classification.  
