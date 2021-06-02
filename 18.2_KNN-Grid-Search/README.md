<h2> Pima Indian Diabetes Dataset - <i>Model Optimization I: Grid Search Optimization - KNN</i> </h2>
In this case study I used the Pima Indian Diabetes dataset with the aim of predicting the onset of diabetes. The goal of this exercise was to use Grid Search Optimzation to identify the best parameters for the K Nearest Neighbors (KNN) model. <br> </br>

It is common practice to use a grid search method for all adjustable parameters in any type of machine learning algorithm. First, you define the grid — aka the range of values — to test in the parameter being optimized, and then compare the model outcome performance based on the different values in the grid. In the case of the K nearest neighbors algorithm, the K parameter is one of the most important parameters affecting the model performance. 
  
  
  <h2>Reflection</h2>
  <ol>
    <li> Although using grid search is better than writing loops to optimize parameters it can quickly become expensive. Tuning two hyperparameters with 5 choices would require 25 runs. Adding cross validation on top of that will increase the number of runs as well. 
  </ol>
