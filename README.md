Report on the Neural Network Model for Predicting Charity Success

Introduction

The objective of this analysis was to build and optimize a deep learning model that predicts the success of organizations funded by Alphabet Soup. The goal was to create a binary classification model capable of determining whether a given organization will be successful based on a set of features extracted from the provided dataset.

Purpose of the Analysis

The purpose of this analysis was to leverage a neural network model to identify patterns and relationships within the data that could predict the success of charitable organizations. By doing so, Alphabet Soup can make more informed decisions about which organizations to fund, thereby maximizing the impact of their contributions. The analysis involved preprocessing the dataset, building and training a neural network model, and optimizing it to achieve the best possible predictive accuracy.

Data Preprocessing

Target and Feature Variables

	•	Target Variable:
	•	The target variable for this analysis was IS_SUCCESSFUL, which indicates whether a charity was successful (1) or not (0).
	•	Feature Variables:
	•	The features used for model training included all other columns in the dataset, excluding EIN, NAME, and IS_SUCCESSFUL. The selected features were primarily categorical and were transformed into a numerical format using one-hot encoding.

Removed Variables

	•	EIN and NAME Columns:
	•	The EIN and NAME columns were removed from the dataset as they were non-beneficial for the model’s predictive capabilities. These columns were deemed irrelevant to the prediction of charity success and could introduce noise or unnecessary complexity.

Handling Categorical Variables

	•	Combining Rare Categories:
	•	In the APPLICATION_TYPE and CLASSIFICATION columns, rare categories with fewer than a selected threshold of occurrences were combined into a new category labeled “Other”. This process helped reduce the complexity of the model by limiting the number of unique categories.
	•	Encoding Categorical Variables:
	•	After combining rare categories, the categorical variables were converted into numerical values using one-hot encoding. This transformation was essential for feeding the data into the neural network model.

Data Splitting and Scaling

	•	Splitting Data:
	•	The dataset was split into feature arrays X and target arrays y. Subsequently, the data was divided into training and testing datasets using an 80/20 split ratio.
	•	Feature Scaling:
	•	To ensure that the model could converge efficiently, the feature data was scaled using StandardScaler from scikit-learn. This scaling process standardized the feature data, ensuring that all input features had a similar scale, which is crucial for the performance of the neural network.

Compiling, Training, and Evaluating the Model

Neural Network Architecture

	•	Input Layer:
	•	The input layer corresponded to the number of features after preprocessing.
	•	Hidden Layers:
	•	The model consisted of two hidden layers:
	•	First Hidden Layer: 80 neurons with a relu activation function.
	•	Second Hidden Layer: 30 neurons with a relu activation function.
	•	Output Layer:
	•	The output layer contained a single neuron with a sigmoid activation function, suitable for binary classification tasks.

Model Performance

	•	Model Accuracy:
	•	The initial neural network model achieved an accuracy of approximately 72% on the test dataset. This accuracy was a reasonable starting point, though below the desired threshold of 75%.

Optimization Attempts

	•	Neurons and Layers Adjustment:
	•	To improve the model’s performance, attempts were made to increase the number of neurons and add additional hidden layers. These changes aimed to enhance the model’s ability to capture complex patterns in the data.
	•	Activation Functions and Epochs:
	•	Different activation functions were tested, and the number of epochs was adjusted to provide the model with more training opportunities. Despite these efforts, the model’s accuracy remained close to 72%.

Summary of Results

The neural network model developed for predicting the success of Alphabet Soup-funded organizations provided a moderate level of accuracy, approximately 72%. While this result indicates that the model was able to capture some of the underlying patterns in the data, it did not meet the target accuracy of 75%. The model’s performance suggests that while deep learning is a viable approach, further optimization or alternative modeling strategies could yield better results.

