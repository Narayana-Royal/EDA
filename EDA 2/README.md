# Black Friday Sales : EDA 2

## Exploratory Data Analysis on various Datasets

## Table of Contents

1. Problem Statement
2. Dataset along with features .
3. Approach Used to solve the Problem
4. Explanation along with the Code 
5. Results with Screenshots

**1. PROBLEM STATEMENT**: 
> ABC Company records all the Passengers details who are traveling from one place to another by the mode of flight transport. They use different airlines in order to fly.All the airlines are given and passenger details like date of journey , from where they are traveling which is basically the source , the destination. The route they followed. Departure time and Arrival time, Duration and rest other details. So,ABC Comapny wants to make predictions of price for each individual. So to make this happen, The company requires data to be cleaned and make it ready for fitting in a model that can predict the price.

**2. DATASET**: 
> https://www.kaggle.com/datasets/nikhilmittal/flight-fare-prediction-mh (Downloaded the zip file which has both train and test data files separately)

> Features: Airline, Date_of_Journey,	Source,	Destination,	Route	Dep_Time,	Arrival_Time,	Duration,	Total_Stops,	Additional_Info,	Price

**3. APPROACH USED to solve the Problem**: 

* *As our problem statement shows that we have to do the feature engineering for this dataset.The following steps are done to achieve this.* 

> Cleaning of data is done by changing categorical values to numerical

> Using various techniques such as STRING.SPLIT() to split the column cells values and making new column by concatenating to the previous one.

> Using the mapping function(.MAP({"COLUMN1_CellVALUES":INTEGER})) to map the values of categorical values to numerical integers.

> Using the LABELENCODER function from sklearn library to change categorical cell values to numerical.

> Finally changing the datatypes of all the column transformed values to integer or float for the model to better understand the datatype.








**4. Explanation along with the Code**:

> Importing the necessary libraries to perform dataset operations which are numpy,pandas,matplotlib,seaborn

> Reading the data of both train.csv and test.csv files using PANDAS READ method and CONCAT both the test data and test data as single dataframe.

> checking the general information of data by using methods called INFO(),DESCRIBE()

> Using string split function(STR.SPLIT("")) to split the data and add it in a column and concatenate this column to the main dataframe. Column values which are used to split are Date_of_Journey.

> Applying the same string split function to the next columns which are Arrival Time, Dept Time, Duration.

> Changing the datatypes of column values using (.ASTYPE()) function.

> After adding the new columns which are created from the spliiting of data columns. We drop the original column(by using DROP("COLUMN1",AXIS=1))     after splitting. Columns where this drop function applied are Date_of_Journey, Arrival Time, Dept Time, Duration.

> Using the map function (.MAP({"COLUMN1_CellVALUES":INTEGER})) in column Total_Stops.
  
> LABELENCODER is used to assign integer values to the categorical oness. Columns where this drop function applied are 	Airline,	Source,	Destination,	Additional_Info.

> Now it is ready to train the model.










**5. Results with Screenshots**: 

> 1. Reading data

<img width="1201" alt="Screenshot 2023-04-29 at 1 03 13 PM" src="https://user-images.githubusercontent.com/88378136/235290128-bacc6085-32f6-4c49-97f0-0aa2e068b00d.png">

> 2. Changing categorical values to numerical using string split

<img width="1201" alt="Screenshot 2023-04-29 at 1 03 34 PM" src="https://user-images.githubusercontent.com/88378136/235290137-65fc1d10-b0c8-4c71-9277-ef7fe97f9fb3.png">

> 3. Changing categorical values to numerical using map function

<img width="1201" alt="Screenshot 2023-04-29 at 1 04 14 PM" src="https://user-images.githubusercontent.com/88378136/235290146-f070370c-d6bf-4a57-9634-7dd18c7fe5f6.png">

> 4. Changing categorical values to numerical using LabelENCODER.

<img width="1201" alt="Screenshot 2023-04-29 at 1 04 33 PM" src="https://user-images.githubusercontent.com/88378136/235290153-fa48efbb-ea32-4dd1-b324-eab4eed474cb.png">



