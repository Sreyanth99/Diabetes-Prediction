# Diabetes-Prediction
We will be training 3 classifiers on a dataset to help us predict the presence of diabetes in a patient\
The three models are:
1) [Decision Tree](#decision-tree)
2) [K nearest neighbours](#k-nearest-neighbours)
3) [Naïve Bayes](#naïve-bayes)

   
And finally, a [comparison of the three models](#comparing-the-models)

This dataset consists of multiple feature variables and one target variable, ie. Outcome

![image](https://github.com/user-attachments/assets/4ed55925-2930-40b5-9dfe-74fa70fb2534)

For the purpose of training the model, we dropped the outcome column. \
Perform the train-test split with the size of 0.2 for the train set

# Decision Tree
A decision tree builds models in a tree structure. It splits down a data set into smaller and
smaller subsets. The final result of a model is a tree with decision nodes and leaf nodes. A
decision node has two or more branches. The leaf node represents a classification or decision.
The top decision node in a tree corresponds to the best predictor, called the root node. We can
use the Decision trees to handle both categorical and numerical data.
We built a decision tree model with default parameters and calculated the model's accuracy.

![image](https://github.com/user-attachments/assets/2521f35a-453f-47da-9cc1-f0a8fea2d925)

We vary the max_depts with different values, redefine the model, and plot the model's
accuracy with each max_depths value. We have received better accuracy with max_dept of 3
and min_samples_leaf value 2.

![image](https://github.com/user-attachments/assets/a50ab274-7104-41c9-8aaf-3424597e1575)

We examine the model with the better hyperparameters we received in the last step.
This time, we have received 78% accuracy!

![image](https://github.com/user-attachments/assets/48aecbe3-71d7-4813-a316-033c6d968cdf)

plotting the tree model, we can see that some nodes have fewer samples. So we decided
to improve the model again (plot shown below)

![image](https://github.com/user-attachments/assets/289406cf-082e-4092-9aa5-4cc71d08b617)

This time we decided to use the criterion hyperparameter as “entropy,” We found a better
accuracy, <b>79.8%</b> and the tree looks perfect. 

![image](https://github.com/user-attachments/assets/21ed878a-2621-4f81-ab84-172cb676469e)

# K-Nearest Neighbours
It is a simple algorithm based on the local minimum of the target function, and it is used to
learn an unknown function of desired precision and accuracy. The algorithm also finds the
neighbourhood of an unknown input, its range or distance from it, and other parameters. It’s
based on the principle of “information gain”—the algorithm finds the most suitable to predict
an unknown value.
Finding the better K-values with the range from 1 to 20 and plotting the result

![image](https://github.com/user-attachments/assets/a9d03f5f-2dc0-4e31-86a4-76e7c98d28ca)
As we can see, we have found better accuracy in the range of 15 to 18.

![image](https://github.com/user-attachments/assets/d7e5664c-7a6a-4491-8db8-056c83cdd170)

We predicted the accuracy again with the better K-value we found in the above steps, and we
got a better model accuracy of  <b>78.5%</b>.
![image](https://github.com/user-attachments/assets/d6bdf3d0-437c-466c-824d-0c3f4536bc7f)


# Naïve Bayes
Naive Bayes classifier assumes that the presence of a particular feature in a class is unrelated
to the presence of any other feature. It is easy and fast to predict the class of the test data set.
It also performs well in multi-class prediction.\
We got the accuracy of this model as <b>77.2%</b>.


![image](https://github.com/user-attachments/assets/2238bb13-b33b-4944-a0d4-abeebb030de5)


# Comparing the models 

Decision Tree took the most supervision and had the lowest amount of accuracy initially but responded very well to fine-tuning but it may not be suitable for more complex use cases. \
KNN achieved a relatively high score with little effort whereas the Naive Bayesian Classifier was simple but did not show much potential for improvement in our case(because of the diabetes prediction function). \
The below chart shows the different techniques used in this project to build and improve the
model and its accuracy


![image](https://github.com/user-attachments/assets/12706d22-08ab-40fb-b835-7f7236ef7637)








