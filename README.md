# Project Overview
 
 This Bank Churn Prediction project aims to predict whether a customer 
 will leave the bank (churn) or continue using its services.
 This is critical for businesses to:
         A. Improve customer retention
         B.Identify high-risk customers
         C.Reduce revenue loss
         
         
 # About my Model training 
         # problems
   since this dataset have quite randomenss ..
   and not much coorelation to among cloumns ..
   and columns to output...
   so its hard to  accurate  than 85 ...    
   
           # solution 1 
         
   so what i did is to combine columns
   in pairs  by using heapmap and self intuition
   which was useful for our model
   to undertanding the pattern. and by this our accuracy 
   got increased by from 85 to 90 + , 
   even though columns correlation are weak.
   
        # solution 2
   I also applied log  transformation to refrained
   my model from  skewness and outliers in numerical columns.
   
              conclusion: 
   and by this our accuracy 
   got increased  from 85 to 90 + 
   
 #  About accuracy 
 
 we got our best possible accuracy by catboost.
 
          accuarcy matrix: 
           
      My overall score : 90.40
      precion : 92
      recall : 87
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





  
      
      
   
   
