# neural-network-challenge-2
Assignment for AI/ML Bootcamp Module 19 Challenge
---------------------------------------------------------------------

## Description

Our assignment was to create a neural network that HR can use to predict whether employees are likely to leave the company. Additionally, HR believes that some employees may be better suited to other departments, so we were also asked to predict the department that best fits each employee. These two columns should be predicted using a branched neural network.

This challenge consists of the following subsections:
- Part 1: Preprocessing the data for use in my neural network model
- Part 2: Create, Compile, and Train the Neural Network Model
- Part 3: Summary


## Getting Started

### Dependencies

- Google User Account
- Google Colaboratory:  Google Colaboratory, or Colab, is a cloud-based notebook space, which allows you to run code in the cloud, rather than locally on your computer. These cloud-based notebooks make it easy to install the tools we need and give us the power of cloud computing.


### Installing

- Clone this repo to your environment
- Setup Google Colaboratory
    - Navigate to [Google Colaboratory](https://colab.research.google.com/notebooks/welcome.ipynb "https://colab.research.google.com/notebooks/welcome.ipynb")
    - You will need a Google account to use Colab. Sign up for an account if you don't already have one. Reference [How to setup a Google account](https://support.google.com/accounts/answer/27441?hl=en "https://support.google.com/accounts/answer/27441?hl=en") for instructions.
    - Within your Google account, navigate to [Google Drive](https://www.google.com/drive/ "https://www.google.com/drive/") and select "Go to Google Drive".
    - After navigating to Google Drive, click the New button and select Folder to create a new folder called "dev".
    - Navigate to the new folder. Once in the folder, you’ll need to connect (download) the Google Colab application:
        1. Click New.
        2. Scroll down to More and expand the dropdown menu.
        3. At the bottom of the menu, click "Connect more apps."
        4. Type “colab” in the top-right search field, and then press Enter to search for the Colaboratory application.
        5. Click the Connect button to download the Colaboratory application.
- How to Create a Colab Notebook
    - Create a Colab notebook by clicking New, hovering over More, and then selecting Colaboratory.
    - A new tab will launch with a new notebook. Everything is hosted online, but the functionality is very similar to Jupyter Notebook.
- Upload notebook file, '**attrition.ipynb**', from your repo to Colab as follows:
    1. From the Colab notebook you just opened, click File and then "Upload notebook."
    2. Drag the notebook file into the box to upload.
**NOTE:  When you upload notebooks, Google Drive will save them by default to a folder called Colab Notebooks. These files can easily be moved to the dev folder created earlier.**


### Executing program

- Open '**attrition.ipynb**' in Colab
- Step through the notebook to see my data preparation and analysis by clicking the "Run" button.
- The results are displayed after each step.
---
**Part 1: Preprocessing the data for use in my neural network model**  
Using Pandas and scikit-learn’s StandardScaler(), LabelEncoder(), and OneHotEncoder(), preprocess the dataset so that it can be used to compile and evaluate the neural network model.

The notebook completes the following data preparation steps:

1. Import the data and view the first five rows.

2. Determine the number of unique values in each column.

3. Create y_df with the attrition and department columns.

4. Create a list of at least 10 column names to use as X data. You can choose any 10 columns you’d like EXCEPT the attrition and department columns.

5. Create X_df using your selected columns.

6. Show the data types for X_df.

7. Split the data into training and testing sets.

8. Convert your X data to numeric data types however you see fit. Add new code cells as necessary. Make sure to fit any encoders to the training data, and then transform both the training and testing data.

9. Create a StandardScaler, fit the scaler to the training data, and then transform both the training and testing data.

10. Create a OneHotEncoder for the department column, then fit the encoder to the training data and use it to transform both the training and testing data.

11. Create a OneHotEncoder for the attrition column, then fit the encoder to the training data and use it to transform both the training and testing data. 
---
**Part 2: Create, Compile, and Train the Neural Network Model**  

I completed the following steps:

1. Find the number of columns in the X training data.

2. Create the input layer. Did not use a sequential model, as there will be two branched output layers.

3. Create at least two shared layers.

4. Create a branch to predict the department target column. Use one hidden layer and one output layer.

5. Create a branch to predict the attrition target column. Use one hidden layer and one output layer.

6. Create the model.

7. Compile the model.

8. Summarize the model.

9. Train the model using the preprocessed data.

10. Evaluate the model with the testing data.

11. Print the accuracy for both department and attrition.
---
**Part 3: Summary**  

Briefly answer the following questions:

> ***Question 1: Is accuracy the best metric to use on this data? Why or why not?***
>
> **Answer:**  
>>**a) Accuracy is appropriate for measuring Department predictions because the data has some balance, R&D (65%), Sales (30%), and HR (4%).  The accuracy score of 80% seems manageable for predicting a department that may be a better fit for the employee.  Also, the cost of incorrectly predicting a new department is low because you can engage the employee in a career developemnt discussion to assess their interest in switching to a new department and establish the best approach for a potential career change.** 
>>
>>**b) Precision may be better for measuring Attrition predictions because the data is imbalanced, No (83%), Yes (17%).  This is a contributing factor to the high accuracy score of 87%.  Also, there may be a high cost to incorrectly predicting that an employee is going to stay, but they actually leave.  Companies make investments in their employees to build their knowledge and develop relevant skills.  They want to keep them if they can.**
>   
> ***Question 2: What activation functions did you choose for your output layers, and why?***
>
> **Answer:**  
>>**department_output:  The model predicts 3 departments.  I used Softmax because it is recommended for mulit-class classification.**
>>    
>>**attribution_output:  The model predicts a binary Yes/No attibution.  I used Sigmoid because it is recommended for binary classification.**  
>
> ***Question 3: Can you name a few ways that this model could be improved?***
>
> **Answer:**  
>>**a) Add or Reduce the number of inputs**  
>>
>>**b) Increase the number of layers**  
>>
>>**c) Increase the number of neurons**  
>>
>>**d) Increase the number of epochs**  
>>
>>**e) Consider splitting this into separate models to better focus models on predicting employee attrition and departments better suited for them.**  
> 
---
## Help

- Please execute all steps in the notebook.  The results of above steps are used in subsequent steps. 


## Authors

- Author:  Tom Clemons

## Version History

- 0.1
    - Initial Release

## Acknowledgments

- How to create Google account: https://support.google.com/accounts/answer/27441?hl=en
- Google Colaboratory:  https://colab.research.google.com/notebooks/welcome.ipynb"
- Google Drive:  https://www.google.com/drive/
