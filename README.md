# Car-Price-Prediction-Using-Linear-Regression
### Overview

The pre-owned car market in India has seen a significant surge in demand, outpacing new car sales in recent years. While new car sales recorded 3.6 million units in 2018-19, the second-hand car market saw around 4 million transactions. This shift indicates that consumers are increasingly turning to used cars, even preferring them over new ones for replacements. The pre-owned car market's pricing dynamics differ vastly from the new car market, which is regulated by OEMs and dealership discounts. In contrast, used car pricing and supply are highly unpredictable, presenting both challenges and opportunities.

### The Challenge

As a data scientist in a tech start-up striving to establish itself in this competitive market, your goal is to develop a robust pricing model for used cars. This model should accurately predict car prices, enabling the business to implement effective differential pricing strategies. By understanding the market price, Cars4U can ensure they never sell below market value, maximizing profitability.

### Your Mission

1. **Analyze Market Trends**:
   - Study the market trends that influence used car pricing.
   - Identify key factors contributing to price fluctuations.

2. **Develop a Predictive Pricing Model**:
   - Utilize historical sales data and other relevant factors to build a predictive model.
   - Ensure the model accounts for the inherent uncertainties in the used car market.

3. **Implement Differential Pricing Strategies**:
   - Use the insights from your model to devise pricing strategies.
   - Help the business optimize its pricing to maintain competitiveness and profitability.

4. **Strategic Decision-Making**:
   - Leverage the model to make informed decisions about buying and selling used cars.
   - Ensure the business stays ahead in the rapidly evolving pre-owned car market.

By successfully developing and implementing this pricing model, Cars4U aims to navigate the complexities of the used car market, securing a foothold and driving growth in an increasingly competitive landscape.

### Data Dictionary of Dataset
S.No. : Serial Number

Name : Name of the car which includes Brand name and Model name

Location : The location in which the car is being sold or is available for purchase Cities

Year : Manufacturing year of the car

Kilometers_driven : The total kilometers driven in the car by the previous owner(s) in KM.

Fuel_Type : The type of fuel used by the car. (Petrol, Diesel, Electric, CNG, LPG)

Transmission : The type of transmission used by the car. (Automatic / Manual)

Owner : Type of ownership

Mileage : The standard mileage offered by the car company in kmpl or km/kg

Engine : The displacement volume of the engine in CC.

Power : The maximum power of the engine in bhp.

Seats : The number of seats in the car.

New_Price : The price of a new car of the same model in INR Lakhs.(1 Lakh = 100, 000)

Price : The price of the used car in INR Lakhs (1 Lakh = 100, 000)

## Feature Analysis:
**Univariate Analysis**
1. More than 50% of all the cars, are sold in Mumbai, Hyderabad, Kochi, Coimbatore, and Pune. Ahemdabad has least number of cars sold, followed by Banglore
2. More than 50% of all cars sold were diesal type
3. Almost 70% of the cars sold, are manual transmission type.
4. More than 80% of the car sold, were 1st time up for sale after brand new purchase
5. Most of cars sold, are of 5 seater type.
6. Maruti, Hyundai and Honda are Top 3 brand sold. Ambasdos, Hindustani, Lamborgini, smart and OpelCors are the least sold.

**Bivariate Analysis**
1. Used Cars are costly in Coimbatore, Bangalore , Kochi and cheaper in Kolkata, Jaipur, Pune.
2. Most expesinve car brands are Lamborghini, followed by Bently, Porsches, Land Rover and Jaguar and least expenisnve car brands are Hindustan, followed by Smart, OpelCorsa, Ambassador
3. CNG and LPG fuel type cars tend to be manual and electric cars tend to be automatic. Automatic transmission type cars are more costlier than manual transmission type.
4. Price of car falls as it is transfred to owners mutiple times.
5. First owner of the car( car that is being purchsed freshly from agency and now it is up for sale) have highest price quoted value.Cars which are sold four and more number of times are cheaper.
6. Ownership of electric cars is generally being transferred only for one time.Prices of all fuel type cars falls with increase in number of instsances of ownership transfer.
7. CNG cars provides better mileage, followed by LPG and diesel. Electric cars do not provide good mileage comared to rest of the fuel type vehicles.
8. Most of the CNG and LPG cars have low price and high mileage range.Some petrol cars have low mileage range and low price,while most of the Diesel cars have low mileage range and High. Electric cars are of low mileage rnage and low price too.Few recods for fuel type petrol and diesel have high price and low mileage, which is generally true for luxury cars
9. Automatic cars mileage range is less than manual cars mileage range. For same milegae automatic cars tend to be expensive than manual cars.
10. Diesel engines tend to have higher volumne, followed by petrol and CNG & LPG.
11. Automatic cars are more expensive than manual transmission car even for same volume of engine.
12. Diesel and petrol fuel type cars can deliver higher power. Power delivered by CNG and LPG fuel type cars is almost same and lesser than diesel and petrol.Power delivered by electric cars is lowest among all categories.
13. Most of the manual cars have power less than 250 bhp, while automatic cars have higher power range.
14. Car with 2 seats are most expensive.Cars with 4 seats have higher price range but average price is as same as cars with 5 and 6 and 8 seats.

**Linear Regression Model Analsyis**
1. **R squared and adjusted R squared are very high for the model. This indicates that we have created a good model., which can explain variance in price of used cars for upto 93%.**
2. F -Stattistics for the modle shows that over all model is significant and there is no over fitting and under fitting of the model.
3. Satisfyies all test assumption of Linear Regression Assumptions: Mean of residuals should be 0, Linearity of variables, Normality of error terms.
4. Mean Squared Error for train and test datset is almot same and close to zero. This indicates that we did not overfit the train data.
5. **Error statistics:
   Mean Absolute Error (MAE): 0.17044271510882436
   Mean Squared Error (MSE): 0.05244233087785979
   Root Mean Squared Error (RMSE): 0.2290029058284191
   Mean Absolute Percentage Error (MAPE): 16.57%**

**Observation from the Model**
It is important to note here that the predicted values are log(price) and therefore coefficients have to be converted accordingly to understand their influence in price.
1. With our linear regression model we have been able to capture ~93 variation in depedndent variable using our data
2. The model indicates that the most significant predictors of price of used cars are -
      Mileage
      Seats
      Age of car
      Kilometers Driven
      Transmission Type : Automatic/Manual
      Brand of cars
      Location
      Fuel_Type
      Owner_Type
3. Newer cars sell for higher prices. 1 unit increase in age of the car leads to [ exp(0.1208) = 1.12 Lakh ] decrease in the price of the vehicle, when everything else is constant.
4. Choosing a car that is automatic insted to manual transmission type leads[ exp(0.1057) = 1.11 Lakh ] increase in price of the vehicle, when everything esle is constant.
5. Other Insights
      Mileage is inversely propotional to price. Higher Mileage cars are low budget cars.
      Kilometers Driven have a negative relationship with the price which is intuitive. A car that has been driven more will have more wear and tear and hence sell at a lower price

**Recommendation**
1. Chennai, Coimbatore, Hyderabad, Bangalore tending to have higher used car prices. We can focus more on these cities to grow the business more.
2. Jaipur, Mumbai, Delhi, Pune, Kochi cities have relatively riskier markets. It'd be beneficial to do market research to strategize growth in these cities.
3. Kolkata appears to be a very risky market for used cars. Careful investment is advised here.
4. With increasing Petrol price, Diesel cars are gaining popularity. Also, Electric cars are, although new, have a very good scope in the market. We should focus on acquiring more Diesel and Electric cars.
5. Number of owners depreciates the used car prices. Thus, we should not acquire cars that have traversed through too many owners. Best is to get cars from the first owner.
6. Auto transmission cars are sold for more price; we should concentrate on acquiring more auto-transmission cars.
7. Dealers can fill up their inventory with Maruti, Honda , Toyota and Hyundai brands
8. Considering the traffic in India these days, automatic cars may be best fit for many individuals. Dealers can acquire more automatic cars and market it accordingly to increase the sales
