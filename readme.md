Evolutive Linear Regression
==========================
This project is an implementation of a linear regression algorithm where the selection of the regressors is done by a genetic algorithm. The idea is to start from a set of possible regressors and let the genetic algorithm select which ones to use. Also to capture non linear relationships, the genetic algorithm can select non linear transformations of the regressors and combine multiple regressors. The genetic algorithm is implemented using the PYMOO library and specifically the NSGA2 algorithm. The NSGA2 algortihm is a multi-objective optimization that allows to optimize multiple objectives at the same time. In this case the objectives are the *R2* and the *shapiro-wilk* test of the residuals. The *R2* is a measure of how well the model fits the data and the *shapiro-wilk* test is a test of normality of the residuals. The idea is to select the regressors that maximize the *R2* and minimize the *shapiro-wilk* test. This in theory should give a model that not only fits the data well but also holds the assumptions of linear regression.

### Usage 
In the notebook `EvolutiveLinearRegression.ipynb` there is an example of how the algorithm can be used to fit a model on a non linear dataset.

### Requirements
The project requires the following libraries:
- numpy
- matplotlib
- scipy
- pymoo

### Improvements
The algorithm shown in the notebook is a very simple implementation of the idea, it uses just two metrics to evaluate the model. A real implementation should use more metrics to evaluate the model performance and how likely it is to hold the assumptions of linear regression. Also the algorithm could be improved by adding more trasnformations to the regressors and more complex combinations of regressors.