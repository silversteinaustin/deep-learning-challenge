# Alphabet Soup Charity Funding Predictor

## Overview of the Analysis

The purpose of this analysis is to create a binary classifier capable of predicting the success of funding applications submitted to Alphabet Soup, a nonprofit foundation. The dataset contains over 34,000 past applications with a variety of features related to the organizations applying for funding. The project involves preprocessing the data, designing and training a neural network model, and optimizing the model to achieve a predictive accuracy higher than 75%. Despite various optimization attempts, the desired accuracy was not achieved.

## Results

### Data Preprocessing

- **Target Variable**: The target variable for the model is `IS_SUCCESSFUL`, indicating whether the funding was effectively used by the applicant.
- **Feature Variables**: The features for the model include all columns except for the identifiers `EIN`, `NAME`, and the target variable `IS_SUCCESSFUL`.
- **Variables Removed**: The `EIN` and `NAME` columns were removed from the dataset as they do not contribute to the predictive power of the model.

### Compiling, Training, and Evaluating the Model

- **Model Architecture**: The initial neural network model consisted of an input layer with 80 neurons, a hidden layer with 30 neurons, and an output layer with a single neuron. The activation function `relu` was used for the input and hidden layers, and `sigmoid` for the output layer to suit the binary classification task.
- **Model Performance**: The model achieved a training accuracy of 72.9% and a testing accuracy of 72.9%, falling short of the 75% accuracy target.

### Optimization Attempts

- **First Attempt**: Included the introduction of dropout layers and the adjustment of activation functions, leading to minor improvements in training accuracy but not in testing accuracy.
- **Second Attempt**: Involved hyperparameter tuning, including changes to the number of neurons and activation functions based on Keras tuner suggestions. The performance did not significantly improve.
- **Final Attempt**: Removed the `STATUS` column and adjusted the number of training epochs. Despite these changes, the model did not achieve the desired 75% accuracy.

## Summary

The project's neural network model shows potential in predicting the success of funding applications to Alphabet Soup, with the highest achieved accuracy around 73%. Although this is promising, it falls short of the project's 75% accuracy goal.

### Recommendation for Future Work

For future iterations, exploring alternative machine learning models like Gradient Boosting or Random Forest classifiers may provide better performance. These models excel in handling both categorical and numerical data and might offer improvements by capturing complex feature interactions more effectively. Additionally, further data preprocessing and feature engineering could enhance the model's predictive accuracy.
