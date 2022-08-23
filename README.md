# 21-Deep-Learning-Challenge

## **1. Overview** 
### Purpose of the Analysis
The purpose of this analysis is to predict whether a company/nonprofit will be successful if funded by Alphabet Soup. The dataset provided by the team includes attributes about the organization and whether the funded money was used effectively. Using deep learning algorthims/neural networks, I created a binary classifier to predict any company's success.

## 2. **Results** 
### Brief description of the Model's Results:

  * **Data Preprocessing**
    * What variable(s) are the target(s) for your model?- 
        * The target variable in the model is 'IS_SUCCESSFUL'
    * What variable(s) are the features for your model?-
        * The features of the model include:
            * APPLICATION_TYPE
            * AFFILIATION
            * CLASSIFICATION
            * USE_CASE 
            * ORGANIZATION
            * STATUS
            * INCOME_AMT
            * SPECIAL_CONSIDERATIONS
            * ASK_AMT 
    * What variable(s) should be removed from the input data because they are neither targets nor features?
        * The two variables that should be removed from the input data are 'EIN' and 'NAME' as they are neither targets nor features and will not help our neural network model predict a specfic outcome. 

  * **Compiling, Training, and Evaluating the Model**
    * How many neurons, layers, and activation functions did you select for your neural network model, and why?
        * My first neural network model had 110 neurons, two hidden layers where the activation functions were both relu and one output layer where the activation function was sigmoid. I initially chose relu as the activation functions for both hidden layers since it learns fast and produces a relatively simple output. I chose sigmoid as the activation function for the output layer as it normalizes the dataset values to 0 and 1, which is ideal for this binary classification.
    * Were you able to achieve the target model performance?
        * Unfortunately, after several tries altering the number of neurons and layers and applying different activation functions to the model, I was still unable to achieve the target model performance of 75% or higher. My model stayed in the 72-73% accuracy range.
    * What steps did you take in your attempts to increase model performance?
        * In my first attempt to increase the model's performance, I increased the number of neurons in each hidden layer, starting with the most nerons in the first layer as the output from one layer becomes additional hidden layers of neurons in the next. Additionally, I tried to make only small changes to the number of neurons as this is the only way to boost performance. Perhaps I need to make this increment smaller in the future. 
        * In my second attempt to increase the model's performance, I added a third hidden layer to the model and made the activation function relu. Adding a third hidden layer would increase the model's training iterations and ideally increase accuracy. Unfortunately, my model still only performed at about 72% accuracy. 
        * In my third-fifth attempts to increase the model's performance, I trial and errored with different activation functions, sigmoid and tanh, in different hidden layers, to see if I could find one that made sense for my dataset and it's complexity. My model still only performed at about 72% accuracy. In the future, I would like to better understand the difference between these activation functions to then know which function should be used in which layer to boost performance. 

## 3. **Summary**
### Final Results and Recommendation for Future Analysis/Model Optimization
* Overall, the deep learning/neural network model created above is only about 72-73% accurate at predicting whether a company funded by Alphabet Soup will be successful. Moving forward, I would recommend using an unsupervised learning algorithm such as t-SNE and K-means together, to find patterns or clusters in the data. Then I would apply a logistic regression or other supervised learning algorithm on these clusters to predict a value (yes or no, 0 or 1) for the target dimension- IS_SUCCESSFUL.