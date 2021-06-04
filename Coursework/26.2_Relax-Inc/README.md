<h2>Future User Adoption - <i>Take Home Challenge I</i>
  <a href="https://nbviewer.jupyter.org/github/Williamdst/Springboard-DSC/blob/master/Coursework/26.2_Relax-Inc/Relax-Take-Home-Challenge.ipynb">
    <img align='center' src="https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" width='53' />
  </a>
</h2>
In this case study I had to use the tools learned in the course to identify which factors predict future user adoption, where an "adopted user" is one who logs into the product three separate days in a least one seven-day period. There were two datasets, one that had the information about users and another that had a row for every instance a user logged in to the platform. <br> </br>

The model that I selected had an F1-score of 0.96 and was a Logistic Regression model using StratifiedKFolding to manage the class imbalance present in the dataset. The factors that were most positively related to user adoption were:
<ol>
  <li> How old the user is (in days on the platform). </li>
  <li> How quickly the user logs in after creating their account. </li>
  <li> How many visits they make in their first month. </li>
</ol>

and the factors that were most negatively related to user adoption were:
<ol>
  <li> How long since the user's last session. </li>
  <li> The median time between all of the user's sessions (<i>The longer the time the less likely the user will be adopted</i>). </li>
</ol>

<h2>Reflection </h2>
<ol>
  <li> I think exploring your data is the most important step in the machine learning process. Exploring your data and playing around with it guides you through the more advanced stages of the process such as feature engineering and model selection. For example, in the user login dataset the system counts the account creation as a login, so a feautre I crafted was first_login_after_creation.
</ol>
