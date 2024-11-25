# BH-PCMLAI Practical Assignment01 - Dan Trezise

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


    