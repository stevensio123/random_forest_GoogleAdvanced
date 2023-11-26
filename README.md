## Lab: Random Forest Modeling

In this lab, I will practice using one of the most popular statistical learning algorithms: Random Forest (RF). I will be given a business scenario and a dataset to explore and apply the Random Forest algorithm. Throughout the lab, I will perform basic Exploratory Data Analysis (EDA), data cleaning, and other manipulations to prepare the data for modeling. This lab builds upon the airlines project where I previously used decision trees. However, this time I will train, tune, and evaluate a Random Forest model.

## Dataset Description

This lab utilizes a dataset called [Invistico_Airline.csv](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction). The dataset represents customer feedback for Invistico Airlines (a fictional name).

The dataset contains:
- 129,880 rows – each row is a different customer response
- 23 columns

| Column name                    | Type | Description                                                                 |
|--------------------------------|------|-----------------------------------------------------------------------------|
| Satisfaction                   | str  | Customer’s overall assessment of airline, either “satisfied” or “dissatisfied” |
| Gender*                        | str  | For purposes of this dataset, “Male” or “Female” were the only two responses |
| Customer Type                  | str  | Customer’s loyalty, “Loyal Customer” or “Disloyal Customer”                   |
| Age                            | int  | Customer’s age                                                               |
| Type of Travel                 | str  | Customer’s reason for travel, “business” or “personal”                        |
| Class                          | str  | Customer’s purchased seat class, “Business,” “Eco,” or “Eco Plus”             |
| Flight Distance                | int  | How far the flight traveled                                                 |
| Seat comfort                   | int  | Customer’s rating of seat comfort                                           |
| Departure/Arrival time convenient | int | Customer’s rating of convenience for departure and arrival time              |
| Food and drink                 | int  | Customer’s rating of food and drink                                          |
| Gate location                  | int  | Customer’s rating of the convenience of the gate location                    |
| Inflight wifi service          | int  | Customer’s rating of the inflight wifi/Internet service                      |
| Inflight entertainment         | int  | Customer’s rating of inflight entertainment                                 |
| Online support                 | int  | Customer’s rating of online support services of the airline                  |
| Ease of online booking         | int  | Customer’s rating of the ease of booking tickets online                      |
| On-board service               | int  | Customer’s rating of service by airline personnel                            |
| Leg room service               | int  | Customer’s rating of amount of legroom                                       |
| Baggage handling               | int  | Customer’s rating of convenience or ease of baggage handling                 |
| Checkin service                | int  | Customer’s rating of checkin service by airline personnel                    |
| Cleanliness                    | int  | Customer’s rating of cleanliness of airplane                                 |
| Online boarding                | int  | Customer’s rating of online boarding process                                 |
| Departure Delay in Minutes     | int  | How long the departure delay was for the flight measured in minutes          |
| Arrival Delay in Minutes       | int  | How long the arrival delay was for the flight measured in minutes            |

*This data has been modified for the purposes of this exercise. Specifically, the Gender column was dropped. While acknowledgement of a gender spectrum varies across societies, many societies now understand that gender is not a binary and there is fluidity in the category across people and time, so creating categories that allow for that leads to more accurate data collection processes.

The dataset can be found on [Kaggle](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)
