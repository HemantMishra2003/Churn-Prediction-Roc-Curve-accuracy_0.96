   #Project Overview
 
    This Bank Churn Prediction project aims to predict whether a customer 
    will leave the bank (churn) or continue using its services.
    This is critical for businesses to:
         A. Improve customer retention
         B.Identify high-risk customers
         C.Reduce revenue loss
         
   # About accuracy 
    we got our best possible accuracy by catboost.
           accuarcy matrix: 
      my overall score is 90.40
      precion : 92
      recall  : 87
      roc_curve : 96
      Cohen's Kappa : 808
      
  # how to use this model for prediction
      1.import importaant requirement / libraries
      
      2.import pickle
       # pick my trained pickle model
       with open('catboost_cat_model.pkl', 'rb') as file:
       model = pickle.load(file)
       
      3.make prediction
          y_pred = model.predict(x_test) 
      4 .save ur prediction
          import pandas as pd

      df_pred = pd.DataFrame(y_pred, columns=['Prediction'])
     df_pred.to_csv('predictions/catboost_predictions.csv', index=False)





  
      
      
   
   
