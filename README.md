# Enhancing_ECommerce_Experience_through_Sentiment_Analysis

Following are the detailed instructions to successfully execute our program.

Pre-work:
1. Programming Language: Python
2. Working Environment: PyCharm IDE
3. Download links:
For PyCharm CE: https://www.jetbrains.com/pycharm/download/?section=mac)
For Python: https://www.python.org/downloads/
Dataset: https://www.kaggle.com/datasets/niraliivaghani/flipkart-product-customer-
reviews-dataset/
4. Installation commands for required python libraries:
(Run the following commands on PyCharm Terminal)
To install pandas: pip install pandas
To install matplotlib: pip install matplotlib
To install sklearn: pip install scikit-learn
To install imblearn: pip install imblearn
To install webbrowser: pip install webbrowser

After laying all the groundwork like installing necessary software and toolkits, we need to focus on
the actual code implementation.

Actual code implementation:

• First import all the necessary libraries using “import” keyword.

• Import the dataset into our working environment and remove all null values.

• Perform EDA, by visualizing the data using bar plots from “matplotlib” library.

• Split the data into training and testing sets using “train_test_split()” method.

• Transform the text data into vectors using TF-IDF Vectorization method.

• As the instances of “positive” class label are very high, we might get inappropriate results, so we need to handle this issue by sampling down the instances using various down sampling techniques. Here we have used 3 different sampling techniques namely Random Under Sampling, Tomek Links and combination of Random Under Sampling and SMOTE (Here SMOTE is an over sampling technique which is used to increase the instances of “neutral” class label as they are less in size).

• After preparing the data, we need to train our Classifiers. Here we have used 3 different classifiers namely SVM, Random Forest, and Gradient Boosting Machine.

• We decided to evaluate the performance of our models using F1 and Recall score metrics.

• We have added an “interaction section” to demonstrate the actual working of our project.

• After defining all the functions, run the program. If there are no errors, we can observe the output on the terminal. Follow the instructions on the terminal to completely
understand what our program does.
