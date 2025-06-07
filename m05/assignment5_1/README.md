# Coupon Acceptance Analysis Project

## Introduction

This project analyzes a dataset about coupon offers to drivers and their acceptance rates. The data comes from a survey on Amazon Mechanical Turk, providing information about factors that may influence a driver's decision to accept a coupon.

The dataset includes:
- Driver demographics (age, marital status, etc.)
- Driving context (destination, weather, time of day)
- Passenger information
- Coupon details (type, expiration time)
- Driver's decision (accept or reject the coupon)

The main goal is to identify differences between those who accepted coupons and those who didn't. This analysis could provide insights into consumer behavior and potentially improve coupon distribution strategies.

## Data Preparation and Cleaning

Before analysis, I prepared and cleaned the data:

1. Loaded the data using pandas and explored it with `data.info()` and `data.head()`.
2. Addressed missing values:
   - Dropped the 'car' column (99.1% missing data).
   - Filled other missing values with 0, interpreting them as 'never' for frequency-related columns.
3. Corrected the typo 'passanger' to 'passenger'.
4. Created 'time_24hr' column to convert time to 24-hour format.

## Overall Coupon Acceptance Rate

The overall acceptance rate for coupons was 56.84%. This means that more than half of the offered coupons were accepted.

## Coupon Acceptance by Type

Acceptance rates varied across different types of coupons:

1. Carry out & Take away: 73.55%
2. Restaurant(<20): 70.71%
3. Coffee House: 49.92%
4. Restaurant(20-50): 44.10%
5. Bar: 41.00%

Coupons for quick, convenient food options were most popular, while bar coupons were least likely to be accepted.

## Factors Influencing Coupon Acceptance

### Weather

Weather conditions impacted coupon acceptance rates:

- Sunny: 59.48%
- Snowy: 47.05%
- Rainy: 46.28%

### Time of Day

Acceptance rates varied by time:

1. 2PM: 66.15%
2. 10AM: 60.84%
3. 6PM: 58.45%
4. 10PM: 50.85%
5. 7AM: 50.22%

### Destination

The driver's destination influenced acceptance rates:

- No Urgent Place: 63.38%
- Home: 50.63%
- Work: 50.22%

### Passenger

The type of passenger affected coupon acceptance:

- Friend(s): 67.34%
- Partner: 59.53%
- Alone: 52.58%
- Kid(s): 50.50%

### Demographics

Several demographic factors showed interesting patterns:

1. Age: Younger people (below 21) had the highest acceptance rate (63.44%), decreasing with age.
2. Gender: Males had a slightly higher acceptance rate (59.08%) compared to females (54.72%).
3. Marital Status: Single individuals had the highest acceptance rate (60.59%), widowed the lowest (47.69%).
4. Education: Those with some high school education had the highest acceptance rate (71.59%), decreasing with higher education levels.
5. Income: Middle-income brackets ($50,000 - $62,499 and $25,000 - $37,499) showed slightly higher acceptance rates.

## Bar Coupon Analysis

Given the lower acceptance rate for bar coupons, I conducted a more detailed analysis of this category.

### Overall Bar Coupon Acceptance Rate

The overall acceptance rate for bar coupons was 41.00%, lower than the average for all coupon types.

### Frequency of Bar Visits

There was a strong correlation between the frequency of bar visits and coupon acceptance:

- 3 or fewer visits per month: 37.07% acceptance (90.1% of sample)
- More than 3 visits per month: 76.88% acceptance (9.9% of sample)

### Age and Bar Visit Frequency

When considering both age and visit frequency:

- Drivers over 25 who visit bars more than once a month: 69.52% acceptance
- Others: 33.50% acceptance

### Passenger Type and Occupation

For drivers who frequently visit bars, have non-child passengers, and work outside farming, fishing, or forestry:

- This specific group: 68.79% acceptance
- Others: 41.45% acceptance

### Comparative Group Analysis

I compared three specific groups:

1. Frequent bar-goers, non-child passengers, not widowed: 68.79% acceptance (29.55% of sample)
2. Frequent bar-goers under 30: 72.17% acceptance (17.10% of sample)
3. Frequent cheap restaurant-goers, income < 50K: 45.35% acceptance (17.06% of sample)

Group 2 showed the highest acceptance rate, reinforcing the importance of age and bar visit frequency.

## Coffee House Coupon Analysis

I also conducted a detailed analysis of coffee house coupons.

### Overall Coffee House Coupon Acceptance Rate

The overall acceptance rate for coffee house coupons was 49.92%.

### Visit Frequency

There was a clear trend relating visit frequency to coupon acceptance:

- 4-8 visits: 68.59% acceptance (highest)
- More than 8 visits: 65.79%
- 1-3 visits: 64.78%
- Less than 1 visit: 48.19%
- Never: 18.88% (lowest)

### Age and Gender

The analysis revealed interesting patterns:

- Males below 21 had the highest acceptance rate (83%)
- Younger age groups showed higher acceptance rates
- Males tended to have slightly higher acceptance rates than females across most age groups

### Income and Education

The relationship between income, education, and coffee house coupon acceptance was complex:

- The highest acceptance rate (92%) was for those with graduate degrees earning less than $12,500
- There was no clear linear trend

### Time and Weather

Time of day and weather conditions showed interesting interactions:

- Highest acceptance rate (72%) at 7AM during snowy weather
- Sunny weather at 10AM and 2PM also showed high acceptance rates (68% and 64% respectively)
- Lowest acceptance rate (18%) at 10PM during snowy weather

### Passenger Type and Expiration

- Coupons with 1-day expiration generally had higher acceptance rates
- Highest acceptance rate (65%) for passengers with kid(s) and 1-day expiration
- Partners showed higher acceptance rates for 2-hour expiration coupons (59%)

## Key Insights and Recommendations

Based on the analysis, here are some key insights and recommendations:

1. Coupon Type: Quick and less expensive food options are most popular. Businesses in these categories should leverage coupons as a marketing tool.

2. Context Matters: Factors like weather, time of day, and the driver's destination influence coupon acceptance. Sunny weather, early afternoon hours, and drivers with no urgent destination are prime conditions for coupon acceptance.

3. Social Influence: Drivers with friends as passengers are more likely to accept coupons. Coupons for social activities or group discounts could be effective.

4. Age and Gender: Younger adults, particularly males, are more receptive to coupons. Marketing strategies could be tailored to appeal to this demographic.

5. Frequency: For both bar and coffee house coupons, frequent visitors are much more likely to accept coupons. Loyalty programs or targeted marketing to regular customers could be effective.

6. Bar Coupons: To improve bar coupon acceptance rates, focus on frequent bar-goers over the age of 25. Consider targeting coupons to times and contexts where drinking is more socially acceptable.

7. Coffee House Coupons: Early morning coupons, especially during inclement weather, could be particularly effective. Also, consider longer expiration times for coupons targeted at drivers with children.

8. Education and Income: The relationship between these factors and coupon acceptance is complex. More detailed analysis could help refine targeting strategies.

9. Expiration Time: Generally, coupons with longer expiration times (1 day vs. 2 hours) had higher acceptance rates. This suggests that giving customers more flexibility could increase coupon use.

## Conclusion

This project provided insights into factors influencing coupon acceptance in a driving context. By analyzing variables including coupon types, contextual factors, and driver demographics, I uncovered patterns that could inform more effective coupon distribution strategies.

The findings highlight the complexity of consumer behavior and the many factors that can influence coupon acceptance. From the type of coupon and weather conditions to the driver's age and frequency of visits to an establishment, each factor plays a role in the likelihood of coupon acceptance.

This analysis demonstrates how data science techniques can be applied to extract meaningful insights from complex datasets. While this is a student project and not based on real-world data, it provides a framework for how such analysis could be conducted in a business setting to improve marketing strategies and increase customer engagement.