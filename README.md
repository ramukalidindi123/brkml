#  Predicting Coupon Acceptance

## Context

Imagine you’re driving through town and receive a coupon on your phone for a nearby business. Would you take a short detour to use it, save it for later, or ignore it entirely? Factors such as the type of coupon (restaurant, bar, or coffee house), who’s in the car, the weather, and even the time of day could influence your decision.

This project focuses on identifying patterns and factors that determine whether a driver accepts a coupon once it’s delivered. By analyzing these variables, we aim to predict coupon acceptance and provide actionable insights.

## Objective

The goal is to leverage data visualization and probability analysis to distinguish between customers who accepted a driving coupon versus those who did not. We aim to evaluate the factors that contribute to coupon acceptance and test various hypotheses for different types of coupons.

## Data Overview

The dataset originates from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/index.php) and was collected through surveys conducted on Amazon Mechanical Turk. It describes various driving scenarios, such as destination, time, weather, and passengers, alongside whether the driver accepted the coupon. Acceptance is classified as:
- 'Y' = 1`: Accepted (used immediately or saved for later use).
- 'Y' = 0`: Not accepted.

The dataset includes five coupon types:
- Less expensive restaurants (under $20).
- Coffee houses.
- Takeaway or carry-out food.
- Bars.
- More expensive restaurants ($20–$50).

### Attributes in the Dataset

### User Attributes:
- **Demographics**: Gender, age, marital status, education, and income.
- **Behavior**: Frequency of visits to bars, coffee houses, and restaurants.
- **Family context**: Number of children.

### Contextual Attributes:
- **Driving Destination**: Work, home, or no urgent place.
- **Weather Conditions**: Sunny, rainy, or snowy.
- **Time of Day**: 10 AM, 2 PM, or 6 PM.
- **Passenger Types**: Alone, partner, kids, or friends.
- **Proximity**: Distance and geographical relationship between the user, venue, and destination.

### Coupon Attributes:
- **Expiration**: Valid for 2 hours or 1 day.

---

## Solution

### Tools & Libraries
- **Platform**: Jupyter Notebook
- **Libraries**: 
  - `matplotlib.pyplot` for visualization.
  - `seaborn` for advanced plotting.
  - `pandas` for data manipulation.
  - `numpy` for numerical operations.

---
## Data Cleansing 
   - Missing values where identified and overall missing percentage was determined
   - Any items that are less than 2% threshold where dropped as statistically do not make much of a diffrence for the overall obkectove

## Hypotheses

### Bar Coupons
1. **Overall Acceptance Probability**:
   - 41% of drivers are likely to accept a bar coupon.

2. **Driver Behavior**:
   - Drivers who visit bars more than 3 times a month have a **76% acceptance probability**, the highest among all categories.
   - Drivers under 30 years old who have visited a bar at least once have a **71% acceptance probability**, the second highest.
   - Drivers who visit bars less than 3 times a month have a **37% acceptance probability**, the lowest among the categories.

---

### Coffee House Coupons
1. **Destination Impact**:
   - "No Urgent Place" destinations yield the highest acceptance for coffee house coupons.
   - However, for the same destination, coupons for "Restaurant (<$20)" show a **20% higher acceptance rate** compared to coffee house coupons.

2. **Demographic Factors**:
   - Males under 21 years old are **83% likely** to accept coffee house coupons.
   - Income levels show no significant influence, with acceptance rates centered around the mean within ±3 standard deviations.

3. **Education**:
   - Individuals with "Some high school education" display the highest acceptance for coffee house coupons.

---

## Conclusion

This analysis utilizes data from diverse scenarios to evaluate the factors influencing coupon acceptance. Visualizations and probability distributions reveal some patterns in customer behavior
