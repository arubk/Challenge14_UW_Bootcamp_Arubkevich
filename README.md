# Machine Learning Trading Bot

This repository contains the code for a Jupyter notebook that combine new algorithmic trading skills with existing skills in financial Python programming and machine learning to create an algorithmic trading bot that learns and adapts to new data and evolving markets.


## Technologies

This program utilizes Python 3.7 with the following packages:

*pandas - 1.3.4

*matplotlib - 3.4.3

*sklearn - 1.0.2

*numpy - 1.20.3

## Installation Guide
Download the repository code through GitHub and unpack the archive. Run the following commands to install all the dependencies:

$ pip install -U scikit-learn

PLease refer to Jupyter Notebook installation guide: https://jupyter.org/install.

## Establish a Baseline, SVC classifier, DecisionTreeClassifier Performances

1. Baseline is the first trading strategy that didn't use machine learning algorithms and simply generated a buy signal when the prior return was positive and a sell signal when the prior return was negative. This strategy proved to provide negative results. That was the worst performing strategy.


![baseline](https://user-images.githubusercontent.com/94565094/158863208-48ead1cb-7552-4fc9-978b-7be477011c92.PNG)


2. SVC classifier model (SVM - SKLearn's support vector machine) determines whether two input parameters can provide accurate buy and sell signals. The two input parameters used is a 4 day and 100 day moving average, which appeared to work the best for positive performance. As the chart demonstrates thas strategy outperformed the Actual Returns and was very affective at identifying positive returning days as seen with the 0.98 recall. This model was also tuned initially by increasing the size of the training set from 3 months to 6 months. This change provided a positive increase in performance as the previous recall for buy days using 3 months of training data was 0.96.

![chart1](https://user-images.githubusercontent.com/94565094/158863828-045f5f57-641c-4bbe-892b-5846d4b80342.PNG)

![report1](https://user-images.githubusercontent.com/94565094/158863940-4f738058-d29e-4b76-a662-5a13843529af.PNG)


3. New classifier, such as AdaBoost, DecisionTreeClassifier, or LogisticRegression checks if the reuslts could be improved upon. After running the same data through the Decision Tree classifier, results were not as great, indicating that this strategy would not be affective at identifying days to buy or sell. This model performed better than the baseline but worse than the SVC model. This model also used the same SMAs and training set size as the SVC model.

![chart2](https://user-images.githubusercontent.com/94565094/158864016-f8ccb666-1b97-46f0-b755-4de1df8e960e.PNG)

![report2](https://user-images.githubusercontent.com/94565094/158864077-aeed310d-b300-496f-ad87-1c28613c5e5d.PNG)


The SVC model would be the best model to use for this strategy.

## Usage
In the command line go to the folder containing the jupyter notebook. Run jupyter notebook to start the jupyter notebook. Alternatively, open Anaconda Navigator, click on "Launch Jupyter Notebook" to start the jupyter notebook.

## Contributors
Project author : A.Rubkevich

Contact information : anastasiyarubkevich@github.com

## License
MIT License
