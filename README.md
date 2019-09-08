# kaggle-iee-fraud-detection
Kaggle competition hosted by IEEE-CIS to detect fraud transactions

Stacking & Blending Strategy :

A. Easiest - Weighted blending of top scoring public kernels - https://www.kaggle.com/priteshshrivastava/ieee-cis-blend

B. Linear stacking - https://www.kaggle.com/aharless/simple-linear-stacking-lb-9730

C. Stacking with a meta model :
  - Create a pipeline of kernels starting from data loading & reducing memory usage
  - Create a hold out validation set (should we split this by time ?)
  - Create single models reading the split data and predicting on val & test sets
  - Create a meta model that trains on val preds and predicts on test set
  - [Optional] Blend this output with other kernels (?)
  - useful kernels : https://www.kaggle.com/yw6916/lgb-xgb-ensemble-stacking-based-on-fea-eng
  

  
