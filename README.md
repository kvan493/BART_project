# BART_project
The purpose of the project is to predict the traffic flow of Northern California's public transit system, Bay Area Rapid Transit (BART), using data from 2016 and 2017.
Using the provided data from 2016 and 2017, we will be observing the traffic throughput between every single station in the system at every hour of theday to address 
operation-related questions as well as building the predictive model. Diving into the given data, we are presented with 3 csv files: 1) station information, 2) throughput 
data from2016, and 3) throughput data from 2017.

The datasets for this project can be found on Kaggle's Bay Area Rapid Transit Ridership: https://www.kaggle.com/saulfuh/bart-ridership. This project was assigned by The
DevMasters to address the following data analytic questions to address staffing and operations:
  1) Which is the busiest BART station?
  2) Which is the least busy BART station?
  3) When is the best time to travel from Berkeley to San Francisco if the traveler wants to find a seat?
  4) Which day of the week is the BART busiest?
  5) How many people take the BART late at night?
  6) Calculate the straight line distance between any two stations.

To answer these questions, I had to do additional research to understand more details about the BART system so I searched for the following:
  1) How many cars are in each train and how many seats are in each cars? https://www.bart.gov/about/history/cars
      ANS: There are anywhere from 3 to 10 cars per trains. There are 4 types of cars that can exist on a train: 
           -A2 and B2 cars have 60 seats
           -C1 and C@ cars have 56 seats
           -All cars can carry over 200 people in a crush load
  2) Are the trains running all of the time or is there a time frame where trains are not operating? Trains need to be maintenanced, right?! https://www.bart.gov/guide/faq#late_night
      ANS: There is a 2-3 hour time frame where trains are not operating for maintenancing and to transport the staff to their sites. 
      
Through data extraction and manipulation, these questions were answered and led to a regression-based model to predict the traffic flow of the BART system. For the model, I 
trained the model using Random Forest Regressor, Gradient Boosting Regressor, and XGBoost Regressor algorithms where Gradient Boosting performing the best with a Root Mean
Squared Error = 23.85 and R^2 = 0.50. *Due to the large dataset (over 23 million data points), my personal computing capacity and timeline of the project did not allow for 
GridSearch to determine the best parameters, which would improve my model.
