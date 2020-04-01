# kaggle-iee-fraud-detection
This repo includes my Bronze Medal solution (Top 10% finish) to the [Kaggle competition](https://www.kaggle.com/c/ieee-fraud-detection) hosted by IEEE-CIS to detect fraud transactions.

Stacking & Blending Strategy :

A. Easiest - Weighted blending of top scoring public kernels - https://www.kaggle.com/priteshshrivastava/ieee-cis-blend

B. Linear stacking - https://www.kaggle.com/aharless/simple-linear-stacking-lb-9730

C. Stacking with a meta model :
  - Create a pipeline of kernels starting from data loading & reducing memory usage
  - Create a hold out validation set 
    - should we split this by time?
    - https://www.kaggle.com/kyakovlev/ieee-cv-options
  - Create single models reading the split data and predicting on val & test sets
    - A. Catboost - https://www.kaggle.com/priteshshrivastava/ieee-pipeline-2-a-model-a-catboost-feat-sel
      - Errors due to missing values / data type
    - B. Random Forest - https://www.kaggle.com/priteshshrivastava/ieee-pipeline-2-b-model-b-random-forest
    - C. XGBoost - https://www.kaggle.com/priteshshrivastava/ieee-pipeline-2-c-model-c-xgboost
  - Create a meta model that trains on val preds and predicts on test set
    - https://www.kaggle.com/priteshshrivastava/ieee-pipeline-3-stacking-with-meta-model
  - [Optional] Blend this output with other kernels (?)
  - useful kernels : https://www.kaggle.com/yw6916/lgb-xgb-ensemble-stacking-based-on-fea-eng
  

  
