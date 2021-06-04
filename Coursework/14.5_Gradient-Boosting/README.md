<h2> The Titanic Dataset - <i>Ensemble Methods II: Boosting - Gradient Boosting </i> </h2>
Boosting works in the same spirit as bagging in the sense that we build a family of models that are aggregated to obtain a strong learner. In boosting models are trained in sequence and each model in the sequence is fitted giving more importance to observation in the dataset that were badly handled by the previous models in the sequence. Each new model focuses its efforts on the most difficult observations to fit from previous models. Each time we run a decision tree, we extract the residuals. Then we run a new decision tree, using those residuals as the outcome to be predicted. After reaching a stopping point, we add together the predicted values from all of the decision trees to create the final gradient boosted prediction. <br> </br>

<p align='center'> <i> You shoot an arrow at a bullseye and the wind messes up the shot. However, depending on where the arrow lands you now know, approximately, how the wind is blowing and how it will mess up your shot. With this new knowledge you can adjust your next shot to better hit the target. </i> </p>

<ul>
  <li> Use <b>bagging</b> when the underlying classifier does well when making predictions on the training set, but there is a drastic change when making predicitons on the test set. Bagging helps solve overfitting (<i>Low Bias - High Variance</i>)
  <li> Use <b>boosting</b> when the underlying classifier does poorly on the training set, but is consistent in the test set. Boosting hleps solve underfitting (<i>High Bias - Low Variance</i>)
</ul>



<h2> Reflection </h2>
<ol>
  <li> Gradient boosting adds <b>ANOTHER</b> layer of hypertuning complexity. Not only are there the random forest parameters there is the gradient boosting parameters such as the learning rate and the number of estimators.</li>
</ol>
