# BH-PCMLAI Practical Assignment01 - Dan Trezise

# Jupiter Notebook

    https://github.com/dtrezise/PracticalAssignment01/blob/6c1fa9c8b0dc42b8ea2a20922405a6aaa4c17e3b/BH-PCMLAI_PracticalAssignment01_DanTrezise.ipynb

# Overview
Explore the coupons dataset and discover the relationships between types of coupons were accepted and by whom. Several scenerios will be explored and visualized. From these exercises I will be able to identify useful trends.

# DATA REVIEW
Looking at the the dataframe to identify any issues with the data using

# DATA CLEANING
### Data issues:

    - The "car" column has too many NaN values to be useful. The strategy is to delete the column from the dataframe.

    - The "direction_opp" column is redundant as the "direction_same" has the same data. Drop this column as well.

    - Several other columns have a few NaN values but not enough to be too concerned about, so the strategy is to drop the rows with NaN values.

    - Rename several columns and values for clarity ease of use.

# DATA OBSERVATIONS

    - The proportion of total coupons that Accepted
            Accepted   0.569335
            Rejected   0.430665
    
    - Plot of proportion of coupons for each destination
        see plots/plots/CouponsAccepted.png
            https://github.com/dtrezise/PracticalAssignment01/blob/6c1fa9c8b0dc42b8ea2a20922405a6aaa4c17e3b/plots/CouponsAccepted.png

         Interpretation: 
            The acceptance rate of the coupons varies by destination, with Cheap Restaurants and Carry Out having the highest accpetance rate. Both Bar and Expensive Restaurants have a higher rejection rate than acceptance. However, further investigation may show that this relationship may change based on demographic and other conditions.

    - Histogram of Temperature Affect on Coupon Count
        see plots/TempAffect.png
            https://github.com/dtrezise/PracticalAssignment01/blob/6c1fa9c8b0dc42b8ea2a20922405a6aaa4c17e3b/plots/TempAffect.png

        Interpretation: 
            At first glance the weather has a significant affect on the coupon count with the count increasing with the tempature.

# Investigating the Bar Coupons

    - Bar Plot of how often per month people visited the bar
        see plots/TimesPerMonthAccepted.png
            https://github.com/dtrezise/PracticalAssignment01/blob/6c1fa9c8b0dc42b8ea2a20922405a6aaa4c17e3b/plots/TimesPerMonthAccepted.png

        Interpretation: 
            There is a significant drop off in coupon count as visits per month increase. However this could be reflected in the fact that less drivers visit the bar more frequently so it would track that the coupon count would also proportionally fall off.

### Initial Findings:

    Proportions of visits to the bar per month:
            0 visits  0.408478
            1 visits  0.280984
            3 visits  0.196208
            6 visits  0.087259
            9 visits  0.027072

    Proportion of total accepted coupons for the bar:
            0.591522

    The acceptance rate of those that went to the bar less than 3 times:
            0.477192

    The acceptance rate of those that went to the bar more than 3 times:
            0.11432999999999999

    The ratio of coupons accepted less than 3 times a month to more than three times a month is roughly
            4.0 to 1.0
            (0.477192 to 0.114329 to be exact)

# Adults Visiting Bars More Than Once A Month
    Drivers with only adults in the vehicle and visit the bar more than once a month.

    - Count Plot 
        see plots/AdultBar01.png
            https://github.com/dtrezise/PracticalAssignment01/blob/6c1fa9c8b0dc42b8ea2a20922405a6aaa4c17e3b/plots/AdultBar01.png

        see plots/AdultBar02.png
            https://github.com/dtrezise/PracticalAssignment01/blob/6c1fa9c8b0dc42b8ea2a20922405a6aaa4c17e3b/plots/AdultBar02.png

    I   Interpretation: 
            Drivers were more likely to accept a coupon, but the likelihood decreases as visits increase.

# Non-Farming Adults Visiting Bars More Than Once A Month
    Drivers with only adults in the vehicle and visit the bar more than once a month and whose occupation was not 'Farming Fishing & Forestry'

    - Histogram Plot 
        see plots/NoFarmers.png
            https://github.com/dtrezise/PracticalAssignment01/blob/6c1fa9c8b0dc42b8ea2a20922405a6aaa4c17e3b/plots/NoFarmers.png

        Interpretation: 
            The results are similar to the previous test. Drivers were more likely to accept a coupon, The likelihood decreases as visits increase, but still tracking ahead of declines.

# Married Status Affect on Acceptance
    Drivers with only adults in the vehicle and are not widows who visit the bar more than once a month.

    - Count Plot 
        see plots/MarriedStatus.png
            https://github.com/dtrezise/PracticalAssignment01/blob/6c1fa9c8b0dc42b8ea2a20922405a6aaa4c17e3b/plots/MarriedStatus.png

        Interpretation: 
            Based on these observations, single drivers without kids are more likely to visit the Bar more than once a month than any other group. Interestingly, divorced drivers very infrequently visit the bar more than once a month.

# Independent Investigation
    Using the bar coupon example as motivation, you are to explore one of the other coupon groups and try to determine the characteristics of passengers who accept the coupons.

# Weather Affect on Coffee Houses
    What affect does the weather have on Drivers with no children in the vehicle and who visit a Coffee House at least once a month except when it is snowy.

    - Count Plot 
        see plots/CoffeHouseWeather.png
            https://github.com/dtrezise/PracticalAssignment01/blob/6c1fa9c8b0dc42b8ea2a20922405a6aaa4c17e3b/plots/CoffeHouseWeather.png

        Interpretation: 
            The plot clearly shows that the weather impacts the count drastically. Sunny days the count is very high and rainy days, it is extremely low.

# Conclusion:
    From the various observations it can be concluded that drivers will accept coupons for some destinations. It appears there are several determining features that can predict the acceptance rate.

# Next Steps
    - Further investigation of the data to identify the best features for predicting the acceptance rate for each destination and/or target demographic

    - Begin modeling with the data to find the best model for predicting coupon acceptance

    - Pass the results on to marketing teams to apply the findings to attrack more customers.

