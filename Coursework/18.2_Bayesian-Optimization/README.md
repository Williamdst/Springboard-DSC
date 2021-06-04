<h2>Flight Departures Dataset - <i>Model Optimization II: Bayesian Optimization - LightGBM</i> </h2>
In this case study I used the flight depatures dataset with the aim of predicting whether a flight depature is going to be delayed by 15 minutes based on the other attributes in our dataset. The goal of this exercise was to use Bayesian hyperparameter optimization to identify the best parameters for a LightGBM model. <br> </br>

In addition to the random search and the grid search methods for selecting optimal hyperparameters, Bayesian methods of probabilities to select the optimal hyperparameters for an algorithm. Bayesian optimization works by constructing a posterior distribution of functions (Gaussian process) that best describes the function you want to optimize. As the number of observations grows, the posterior distribution improves, and the algorithm becomes more certain of which regions in parameter space are worth exploring and which are not.


<h2>Reflection</h2>
<ol>
  <li> Bayesian Optimization seems to be a very eficient way of hyperparameter tuning models. Bayesian Optimization and LightGBM together are a pretty overpowered combination. Although they are powerful tools, as a Data Scientist it is still important to know when to use them versus other models and hyperparameter tuning methods. 
</ol>
