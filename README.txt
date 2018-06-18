
***********************************************************************************************
                         
                                   Plan B Final Project (CS-797)           
                                   Road Surface Score Prediction

                                    Name : Sindhuri Punyamurthula
                                   


************************************************************************************************

Name of the ppt : RoadSurfaceScore.pptx

Dataset : 1) Images
             Training => ./IMAGES/Train
             Testing  => ./IMAGES/Test

          2) CSV Files
             Training => Trainold.csv
             Testing  => Test.csv

Note : The scores in the csv file are from -1 to 3.These have been rescaled to 0 to 4 
       before using in the models.
##########################################################################################


6 different Scenarios/Models 

Model 1 : Lstm with histogram of pixel values ( different bin sizes )
          Best Model : 16 bins
          File Name : HistPix_Bins.ipynb

Model 2 : Lstm with histogram of color ( different bin sizes )
          Best Model : 10 bins
          File Name : HistColor_Bins.ipynb

Model 3 : CNN-LSTM on images
          File Name : CNN-LSTM.ipynb
          Model Name : CNNLSTM.h5

Model 4 : Support Vector Regression using both hist of pixel(16bin) and 
          hist. of color(10 bin) as feature set.
          Best Model : Hist. of pixel - 16 bins
          File Name : SVR.ipynb
          
Model 5 : Bidirectional LSTM using both hist of pixel(16bin) and 
          hist. of color(10 bin) as feature set.
          Best Model : Hist. of pixel - 16 bins 
          File Name : Bidirectional-LSTM.ipynb
          

Model 6 : Stacked LSTM using both hist of pixel(16bin) and 
          hist. of color(10 bin) as feature set.
          Best Model : Hist. of color- 10 bins 
          File Name : Stacked_LSTM.ipynb


#############################################################################################

Comparison of different models,parameters and graphs 

[I] File Name : Finding_Best_Models.ipynb
    This file compares the Mean Absolute Errors of models using different featureset
    as shown in the above 6 scenarios.
    
    Best Model : Hist. of pixel (16 bins) with MAE of 0.89



[II] File Name : Finding_Best_Optimizers.ipynb
    This file compares the Mean Absolute Errors of models using different optimizers
    sgd,rmsprop,adam.
    
    Best Optimizer : sgd



[III] File Name : Finding_Best_Activation.ipynb
    This file compares the Mean Absolute Errors of models using different activation
    functions.
    
    Best Activation function : tanh,sigmoid,hard sigmoid


#############################################################################################

File Name : Visualization_Best_Model.ipynb

This file shows the following details considering the best model:

(a) The predictions with the model on both training and test set,
    MAE,RMSE and ground truth,actual predicted value.

(b) Success Cases and Failure Cases 
    (ground truth - predicted) < 0.8  Success 
    (ground truth - predicted) >= 0.8  Failure

(c) Map visualization using Bokeh
    i. ground truth of training data
   ii. predictions on training data
  iii. ground truth on test data
   iv. prediction on test data


#############################################################################################

  Environment Setup 

 * Jupyter Ipython Notebook
 * Python sci-kit package
 * Matplotlib
 * Pandas
 * Numpy
 * Keras with Tensorflow library
 * OpenCV
 * Bokeh with GoogleMaps API

##################################################################################################
