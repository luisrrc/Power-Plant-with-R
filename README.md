![R](https://img.shields.io/badge/R-green)
![XGBOOST](https://img.shields.io/badge/XGBOOST-orange)

Testing R in jupyter notebook

# Power-Plant-with-R

Power generation is a complex process, and understanding and predicting power output is an important element in managing a plant and its connection to the power grid. The operators of a regional power grid create predictions of power demand based on historical information and environmental factors (e.g., temperature). They then compare the predictions against available resources (e.g., coal, natural gas, nuclear, solar, wind, hydro power plants). Power generation technologies such as solar and wind are highly dependent on environmental conditions, and all generation technologies are subject to planned and unplanned maintenance.

## Business Problem

Because they supply power only occasionally, the power supplied by a peaker power plant commands a much higher price per kilowatt hour than power from a power grid’s base power plants. A peaker plant may operate many hours a day, or it may operate only a few hours per year, depending on the condition of the region’s electrical grid. Because of the cost of building an efficient power plant, if a peaker plant is only going to be run for a short or highly variable time it does not make economic sense to make it as efficient as a base load power plant. In addition, the equipment and fuels used in base load plants are often unsuitable for use in peaker plants because the fluctuating conditions would severely strain the equipment.

The power output of a peaker power plant varies depending on environmental conditions, so the business problem is predicting the power output of a peaker power plant as a function of the environmental conditions — since this would enable the grid operator to make economic tradeoffs about the number of peaker plants to turn on (or whether to buy expensive power from another grid).

Given this business problem, we need to first perform Exploratory Data Analysis to understand the data and then translate the business problem (predicting power output as a function of environmental conditions) into a Machine Learning task. In this instance, the ML task is a regression since the label (or target) we are trying to predict is numeric.

## Data

The real-world data we are using in this project consists of 9,568 data points, each with 4 environmental attributes collected from a Combined Cycle Power Plant over 6 years (2006-2011).

-AT = Atmospheric Temperature in C.

-V = Exhaust Vacuum Speed.

-AP = Atmospheric Pressure.

-RH = Relative Humidity.

-PE = Power Output. This is the value we are trying to predict given the measurements above.

## Result

After testing with 2 models, the model  with Extreme Gradient Boosting to predict power output had better results. We can see that it has better performance than linear model we tried in the first model. The RMSE with the test data decreased from more 4.5 to 3.1 and increase the R2 from 0.93 to 0.97.
