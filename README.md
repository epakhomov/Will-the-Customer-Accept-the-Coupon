# Will the customer accept the coupon?

## Introduction

This readme file provides a summary of findings for Practical Application Assignment 5.1: Will the Customer Accept the Coupon? 

## The objective and the data

The **objective of the study** is to highlight the differences between customers who did and did not accept the coupons. The information about the data is provided in [the Jupyter book that can be found here](src/prompt.ipynb).

## The summary

The summary consists of two parts. The first part was scoped in the assignment and the second one was a free investigation. The summary will not discuss the data preparation steps. Please refer to the [Jupyter book](src/prompt.ipynb)Jupyter book for that.

### The data

The data describes five different types of coupons: less expensive restaurants (under $20), coffee houses, carry out & take away, bar, and more expensive restaurants ($20 - $50). As well as the attributes of the drivers like gender, age, income, etc. and also contextual attributes. Please find the full list of attributes in the [Jupyter book](src/prompt.ipynb).

### Part 1

One of the first suggested tasks was to visualize the variety of coupons that the data has (Fig.1).

<img src="/images/01.png" alt="Fig.1" class="center" style="width:600px;height:auto;">

As we can clearly see that the most common coupon is "Coffee House" as well as the most accepted one.
We also calculated the proportion of the total observations that chose to accept the coupons to be **57%**.

According to the next assignment, we looked closer at the data that contained observations for the "Bar" coupon only.

We calculated the proportion of the total observations that chose to accept the "Bar" coupons to be **41%**.

#### Groups

Then we were given the following groups of observation for the analysis of which group will more likely accept the coupon.

**Group 1A**: Drivers who went to a bar 3 or fewer times a month.<br />
**Group 1B**: Drivers who went to a bar more than 3 times a month.

**Group 2A**: Drivers who go to a bar more than once a month and are over the age of 25.<br />
**Group 2B**: All other drivers (that is who go to a bar less once a month and are under the age of 25).

**Group 3A**: Drivers who go to bars more than once a month and had passengers that were not a kid and had occupations other than farming, fishing, or forestry.<br />
**Group 3B**: All other drivers that do not fall into Group 3A.

**Group 4A**: Drivers that go to bars more than once a month, had passengers that were not a kid, and were not widowed.<br /> 
**Group 4B**: Drivers that go to bars more than once a month and are under the age of 30. <br />
**Group** 4C: Drivers that go to cheap restaurants more than 4 times a month and income is less than 50K. 

#### Acceptance rates

|                    |Group 1A|Group 1B|Group 2A|Group 2B|Group 3A|Group 3B|Group 4A|Group 4B|Group 4C|
|--------------------|--------|--------|--------|--------|--------|--------|--------|--------|--------|
|**Acceptance rate** |  0.37  |  0.77  |  0.7   |  0.33  |  0.71  |  0.3   |  0.71  |  0.72  |  0.46  |

### Discussion

Based on these observations, we can hypothesize the following about the drivers who accepted the bar coupons. The drivers are more likely to accept the coupons if they are:

- Go to a bar often, at least once a month
- Are over the age of 25 and older
- Have passengers that were not a kid
- Not involved in farming, fishing, or forestry industry

### Part 2

Businesses are interested in customers with high income, because they likely to spend more money and increase the revenue. The **objective of this part** is to understand attributes of drivers with high income who would likely accept a coupon.

Let's create a new group 5A for drivers with income 87500−99999 USD and 100000 USD or more.
Now let's visualize the variety of coupons for this group (Fig.2).

<img src="/images/02.png" alt="Fig.2" class="center" style="width:600px;height:auto;">

As we can see, three coupon types stand out: "Restaurant(<20)", "Carry out & Take away" and "Coffee house". It's interesting also to note that drivers with high income were less likely to accept "Bar" and "Restaurant(20-50)" coupons. So with this data in mind, let's take even closer look at drivers with high income who likely to accept "Restaurant(<20)", "Carry out & Take away" and "Coffee House".

<img src="/images/03_2.png" alt="Fig.3" class="center" style="width:900px;height:auto;">

Looking at these plots, we notice the following attributes stand out stronger than the most: weather, expiration, marital status, destination. With that in mind, let's verify this observation by calculating an acceptance rate between single drivers observed in sunny weather with no urgent place to go and that were given coupons expiring in one day. Let's compare this acceptance rate with an acceptance rate for everybody else and Group 5A.

#### Groups

**Group 5B**: Single drivers observed in sunny weather with no urgent place to go and that were given coupons expiring in one day.
**Group 5C**: All other drivers that do not fall into Group 5B.

#### Acceptance rates

|                    |Group 5B|Group 5C|
|--------------------|--------|--------|
|**Acceptance rate** |  0.81  |  0.6   |

### Discussion

Both Groups have good acceptance rates which proves that any driver with high income is likely to accept "Restaurant(<20)", "Carry out & Take away" and "Coffee house" coupons. However, out of all drivers with high income, the biggest acceptance rate was detected in the group of single drivers observed in sunny weather with no urgent place to go and that were given coupons expiring in one day.

Thus, business with the modest budget for coupon promotions should target this group of drivers first. Some social media companies, like Meta for example, can target users with these specific attributes. 

## Next steps and recommendations

- For users with high income, we can even further research specific attributes like occupation, direction, education, children, etc.
- We can also conduct the similar analysis for business involved in only one segment, like Bars only as we did in the Part 1. We could similarly research other segments (Cheap restaurants, coffee houses, et.).
- Given the technical means that allow businesses to target any attributes of drivers, it would be great to develop a system that would automatically calculate coupon acceptance rates given the input about target audience. 