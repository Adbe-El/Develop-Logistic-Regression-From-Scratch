# Developing Logistic Regression Algorithm From Scratch

Here i show Logistic Regression can be developed from scratch. Firstly Logistic regression is a generalized linear model that we can use to model or predict cases where the target variable is categorical by type. So simply put Logistic Regression Models are Classification models. They are used to predict the category or class an element or entity falls into. For the case where we have to classify a set of variables into two classes we call that Binary Classification Problem. For binary classification case the model(in this case Logistic Regression) predict the target variable by producing outputs of 0 when it belongs to a class and 1 when it belongs to the other class.

## Approximations
Logistic Regression function is derived from the transformation of a Linear Regression function using what is known as a sigmoid function.            
           
### 1. Generating the Logistic Regression from Linear Regression
First the linear regression is given below as:

![image1 showing Linear Regression](

where **w represents the weights, x represents the matrix of features or the input vector and b represents the bias**

Recall that inorder to transform the above function we make use of the sigmoid function. The sigmoid function is shown below: 

![image2 showing sigmoid function]

Its graphical represented as:

![image3 showing the graphical representation of the sigmoid function]

The purpose of the sigmoid function is to transform the above linear regression into generating output values as in form probabilities of that fall between 0 and 1. 
Even after this tranformation the outputs do not yet reflect what the typical classification output should look like. So, we set a threshold is set at x = 0.5, such that all values greater than and equal to 0.5 are approximated as 1 and others less than this threshold are rounded down as 0.

Substituting linear regression equation into the sigmoid function, satisfying the above conditions for x= 0.5 as the threshold. We have

![image4 showing the transformed linear regression]

on substituting, x from the sigmoid function equals (wx + b) from the linear regression fumction
where     h(x) is the transformed linear regression function, which is the logistic regression function 
          y_hat is the predicted value of the target varible


### 2. Cost Function
The cost function we use here is the Cross Entropy Cost Function. It is shown mathematically as:

![image5 showing the Cross Entropy Cost Function]

What is a COST FUNCTION
The cost function measures how poorly a model does in terms of its ability to estimate the relationship between the independent variable(X) and the dependent variable (y). The goal therefore in this case is minimise or reduce the cost function. In reducing the Cost function what we are doin in essence is reducing the weights or finding what value of weights and biases would minimise the cost function and in turn optimise our Machine Learning model. 
To minimise the cost function by applying something called a **Gradient descent** on the cost function. The gradient descent is simply a partial differentation applied of the cost function with respect to the weights and biases.

![image6 showing the Gradient Descent on the weight]

![image7 showing the difference between a big learning rate versus small learning rate]

On applying gradient descent the updated weights, biases and cost function becomes:

![image8 showing updated weights, biases and cost functions]





