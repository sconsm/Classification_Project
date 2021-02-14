# Classification_Project
Chicago Restaurant Inspections

## **"Making The Cut"**

## Predicting Inspection Results for Chicago Based Restaurants

------

### Objectives:

The overall intent of this project is to better predict the outcome of a restaurant in the City of Chicago passing or failing inspection, which could then help improve the quality of restaurants throughout the area, and also help prevent the spread of foodborne diseases. Using machine learning classification modeling to help us make these predictions, we will look at specfic parameters and features to see which are influential to the target. 

------

### Features and Target Variables:


##### Target : Results 

  - Pass or Fail Inspection

##### Features : 

- License #
- Inspection Type
- Latitude
- Longitude
- Risk

------

### Data Used:

Chicago Open Source Data Portal

  *refer to Food-Inspections CSV*

------

### Tools Used:

- Seaborn

- Pandas

- Matplotlib

- Tableau

- Numpy

- Sklearn

------

### Possible Impacts and Practical Applications:

After looking at a specfic evaluation metrics -- including confusion matrices, accuracy, precisons, recall and F1 scores, as well as ROC AUC. Ultimately, we decided on the F1 Score as our decision metric for evaluating the classification models. This gives us a best model: **KKN Classification.** We can use this to then perform different variations of modeling in order to make better predictions of our target. 

- KNN Classification Modeling can be used to predict restaurant inspection results before they happen
    - This will keep businesses up and running 
    - Help keep people safe
    - Save Public Health Resources

This modeling can help restaurant owners better place their businesses based on geographical features where they are more likely to pass inspection
This is good for the restaurant owners, the Department of Public Health and Food Protection Services, and consumers...like you! 

Based on feature engineering and looking at the average results with location features, we can better predict areas with inpsections to have a higher likelihood of passing if they are closer inland, as opposed to near the lake. Looking at specific examples of restaurant type, cuisine, and median household income will help add depth to the data and improve our prediction metric.

### Future Work:

It will be very interesting to see if income plays a major role in restaurants passing or failing inspection. Only initial steps have been taken to look into this, but it is a great starting point for future work. Comparing zip code locations across median household incomes would perhaps be a good indicator for our target Results prediction.

Another component that would be extremely beneficial to this model, would be to to connect to a Chicago data portal API to incorporate this model to the data on a real-time basis. Since the data is regularly updated, having a model that regularly updates with it, would be ideal.

