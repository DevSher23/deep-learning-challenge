# deep-learning-challenge

Overview of the Analysis: 

The purpose of this analysis was to use deep elarning techniques to create a binary classifier that can predict whether applications of ALphabet Soup would be succesful if funded, and which organizations are worth investing in to ensure the best possible outcome for the investor.

Results: 

Data Processing: 

The target variable for this model is "IS_SUCCESSFUL" which determines if the funding in fact was successful or not. The Features for the model include all of the other variables except for "EIN" and "NAME" which were dropped and not targets nor features. 

Compiling, Training, and Evaluating the Model:

  I opted for a model architecture with two hidden layers with the aim of capturing more complex patterns in the data. The first hidden layer had 8 neurons, using the rectified linear unit (ReLU) activation function which can help to accelerate the model's training. The second hidden layer had 5 neurons, which added another level of complexity to the model.  The sigmoid activation function was used in this layer to transform the weighted sum of the previous layer into a probability value between 0 and 1. Thia activation function can help interpret if the organization will be succesful based on input features. 

Optimization:

  To improve the model's performance from 72.8% to 75.4%, I experimented with different feature combinations. First, I removed EIN, then AFFILIATION and SPECIAL CONSIDERATIONS, which resulted in an increase in accuracy. However, further iterations by removing STATUS, ORGANIZATION, and APPLICATION_TYPE did not improve the accuracy score. I also made changes to the model architecture by keeping two hidden layers, but I increased the number of neurons to 20 for the first hidden layer and 10 neurons for the second hidden layer. This adjustment was more appropriate for the data, considering the number of features involved.

Summary:

The deep learning model fell short of the target accuracy score of 75%, achieving only 72.85%. While optimization strategies were successful in achieving a 3% improvement, additional improvement could be sought by experimenting with different model architectures and hyperparameters. Alternatively, a different classification model such as a random forest classifier could be explored as an alternative solution. This model could be better equipped to handle missing data or outliers. The use of a random forest algorithm may provide better results for this particular problem.


