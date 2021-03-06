# Project1 Credit Card Churn Analysis

### Group: 3 (No pun indented)


## Introduction

We will be analyzing a data set of customer information from a bank that is concerned about the high churn rate. Credit Card churning is the practice of repeatedly opening and closing credit card accounts to continually receive the incentives that are given to those who open new credit card accounts. We will be performing exploratory data analysis on this dataset, to see if we can gain any insight into which customers are more likely to churn and if there is anyway of decreasing that number.

## How will we be doing this?

Using a dataset of over 10,000 customers, we will be looking at the relationship between a number of variables and the attrition status of a customer, to determine if there are any trends that can help identify those customers more likely to churn. The dataset consists of the following:

CLIENTNUM: Client number, unique identifier to the client

Attrition_Flag: Shows whether customer is existing or attrited

Customer_Age: Shows customers age in years

Gender: Shows customer gender

Dependent_count: Shows number of dependents

Education_Level: Shows educational qualification of the account holder

Marital_Status: Marital status of the account holder(Married, Divorced, Single or Unknown)

Income_Category: Annual income category of the account holder (< 40𝐾, 40K - 60K,  60𝐾− 80K,  80𝐾− 120K)

Card_Category: Type of Credit Card (Blue, Silver, Gold, Platinum)

Months_on_book: Period of relationship with the bank

Total_Relationship_Count: Total number of products held by the customer

Months_Inactive_12_mon: Number of months inactive in the past 12 months

Contacts_Count_12_mon: Number of contacts in the last 12 months

Credit_Limit: Credit limit on the Credit Card

Total_Revolving_Bal: Total revolving balance on the Credit Card

Avg_Open_To_Buy: Open to Buy Credit Line (Average of last 12 months)

Total_Amt_Chng_Q4_Q1: Change in transaction amount (Quarter 4 over Quarter 1)

Total_Trans_Amt: Total transaction amount (Over last 12 months)

Total_Trans_Ct: Total transaction count (Over last 12 months)

Total_Ct_Chng_Q4_Q1: Change in transaction count (Quarter 4 over Quarter 1)

Avg_Utilization_Ratio: Average Card utilisation ratio

## What questions are we trying to answer?

Q1: Can we compare gender and age to the attrition status of customers, to identify any trends?

Q2: How does the familial situation affect the attrition status of customers? Can we use gender, age, marital status and dependents to identify any correlation between familial situation and attrition status?

Q3: Does how long the customer has been inactive give any indication to whether a customer may leave? Using months inactive and months on book, can we recognize what may be a trigger point for customers leaving?

Q4: Is there a relationship between education and income levels - do higher education and income correlate? Are those with a higher income and higher education level more likely to stay with the bank? Are people with a lower income more likely to leave? (Does a high number of dependents and low income have any effect? 

Q5: What is the relationship between card cateogry and income? Are those with a higher income on a better card, and are those on better cards more likely to stay or leave?

Q6: Do customers on higher income have higher transaction levels? Is there any correlation between transaction amounts and how long customers have been inactive?

## What conclusions were drawn?

### Question 1 Analysis

The first figure shows us the overall make-up of the data regarding gender, with 52.9% female and 47.1% male.

![Q1 Pie1](https://user-images.githubusercontent.com/88689661/146591600-175cfea2-1fa0-44a8-b09d-0b976c0b2ad3.jpg)

The second figure shows us the overall make-up of the data regarding attrition flag, with 83.9% existing customers and 16.1% attrited customers.

![Q1 Pie2](https://user-images.githubusercontent.com/88689661/146591601-6c9034ce-7c74-463a-9b50-01f996e0b047.jpg)

The third figure allows us to compare between genders the number of existing and attrited customers. As can be seen in the bar plot, the number of females for both existing and attrited customers is larger, though this is to be expected given that the female gender makes up a slightly larger portion of the dataset.

![Q1 Graph3](https://user-images.githubusercontent.com/88689661/146591831-1831a8a3-a515-4de6-97e7-d5d3760d9736.jpg)


Following on from this, the customer ages were placed into groups(bins), allowing for easier analysis. This was then visualized in a pie plot, showing the different percentages of the age groups that make-up the dataset. The fifth figure allows us to compare between the age groups and the number of existing and attrited customers. The bar plot shows us that the age group with the largest number of existing and attrited customers is 40-49. This is supported by the fact that the most often occurring age within the dataset is 44.


![Q1 Graph4](https://user-images.githubusercontent.com/88689661/146593271-106dadfe-ab54-4a76-8e96-6143eb89460a.png)

![Q1 Graph5](https://user-images.githubusercontent.com/88689661/146593452-82b485c6-412d-4376-bdba-ed277472ad8a.png)



A high standard deviation of 8.02(rounded) shows us that while the 40-49 category is the most populous, the data within the customer ages is spread and varied.

Although the information from this data doesn't really identify an age group or gender that is more likely to churn. It does identify the most populous age group (40-49), which may allow the bank to target customers within that age group to ensure they stay with the bank.

### Question 2 Analysis

FAO MOSES

### Question 3 Analysis

The first figure shows us the percentage of customers and the months they have been inactive for. We can see from this pie chart that those that have been inactive for 3  months  make up the largest percentage of customers. This is then further confirmed in figures 2 and 3.

![Q3 Pie1](https://user-images.githubusercontent.com/88689661/146599914-5bfd0e0c-5a27-45a6-aaba-f2feb3f7fbaf.jpg)


When using .describe() on the data frame, we can see that the mean for months inactive is 2.34, the standard deviation is 1.01 and the variance is 1.02. These values indicate that the data for months inactive are closer to the mean and are not spread out over a wide range.

Figure 2 is a bar plot showing the number of months a customer was inactive before they left the bank. As can be seen on the plot, the number of customers increases until we reach 3 months, at this point there is a sharp drop off. Is 3 months without activity a trigger point? Perhaps the bank notifies the customer after 3 months of inactivity and this is what causes the customer to leave.

Figure 3 is a bar plot showing the number of months existing customers have been inactive. As in figure 2, there is an increase until we get to 3 months before the number of customers sharply drops off. This supports the idea that the bank may send out notifications after 3 months of activity, causing these customers to start using the credit card again. Figure 4 is a combination of figures 2 and 3, comparing the number of months inactive for both existing and attrited customers on the same plot.

![Q3 Graph1](https://user-images.githubusercontent.com/88689661/146600158-fc96698a-61bc-4391-b55d-c9b625666d6b.jpg)


Figure 5 is a stacked bar plot showing the number of months a customer has been with the bank for both existing and attrited customers. This plot shows us that for both existing and attrited customers, the highest number of customers were in the 30-39 months category. 

![Q3 Fig5](https://user-images.githubusercontent.com/88689661/146600358-23281bb8-4219-4c2f-8d10-e754f9080940.jpg)


This data could support one of two ideas, the first being that the bank does not have the high churn rate that it anticipates. The second idea is that the credit card may have a certain length of time it has to be had for. 3 years (36 months) is within the 30-39 months category, and this can be supported by the fact that the mean for months on the books is 35.9. It may be that for customers to benefit from the rewards scheme, that they must sign up to have the credit card for 3 years. However, both standard deviation and variance are quite high, so we may not be able to rely on this data.

This data indicates that 3 months inactive seems to be some kind of trigger point. The number of customers that are inactive following 3 months drops rapidly. If this is because the bank sends notifications out at 3 months of inactivity, perhaps the notification could be changed to include a further bonus or reward, to incentivize the customer to use their credit card again. 

### Question 4 Anaylsis

The first figure shows a line graph which considers the income level and the attrition of customers. From the graph we can see that the majority of the customer base of the bank that are using credit cards fall into the "lower" income category; with both Existing Customers and Attrited Customers showing a high number of customers with income levels 'Less than $40k' and '40K-60K'. Further Analysising the graph we can say that generally speaking the higher the income the less likely a customer is going to churn. However, this may be a skewed conclusion as the number of customers decreases as income rises, which would require further analysis to determine.

![](https://github.com/Emziicles/Project1-CreditCard/blob/main/Images/download%20(8).png)

Looking at the next figure; the horizontal bar chart shows the education level agains the number of customers. The chart shows which customers are 'Existing Customers' and which are 'Attrited Customers'. This further supports the statement made above with most customers of the bank being part of the "lower income categories - which can be seen in the high number of Existing and Attrited Customers which are only educated up until Graduate level in the American system. A well known general trend suggests that people with less education tend to earn less than people with 'Further Education' - this can also be seen in this dataset. Focusing on the Attrited Customers in the problem we are trying to solve, the 'Graduate' level education group shows the highest number of Attrited Customers closely followed by the 'High School' and 'Uneducated' level education groups. The "more" educated groups have significatnly fewer churned customers when comapred to the others.

![](https://github.com/Emziicles/Project1-CreditCard/blob/main/Images/download%20(9).png)

Finally, looking at the stacked bar chart which shows the number of dependents agaisnt the number of customers. The chart also shows the customers which are 'Existing Customers' and 'Attrited Customers'. We are able to determine that the customers with "smaller" families tend to be the customers which take out credit cards with the bank. However, they also make up the majority of the customer base which may skew the data. From the graph we can also see that customers with "medium" sized families tend to churn slightly more than the customers with no dependents or only 1 dependent but shoe a significantly fewer number of existing customers. The bank has no customers with more than 5 dependants, this suggest that taking out a credit card from the bank with a "large" family is very unlikely.

![](https://github.com/Emziicles/Project1-CreditCard/blob/main/Images/download%20(10).png)

To conclude, we believe the bank should target "low" earning customers with little to no education that have a "small" family when looking to provide a package which will keep them with the bank. This is because they show the highest number of attrition as well as the higest number of existing customers. This will allow the bank to offer better credit card packages to both existing and churned customers which solves the current problem they are facing. Alternatively, to imporve the amount of customers that stay with the bank packages can be tailored towards the "higher" earning, more educated and "large" family customers. However, this option is much higher risk as the customer base of the bank doesn not contain many customers which fall into these categories.
### Question 5 Analysis
FAO Khadiza

The first figure is a stacked horizontal bar chart showing the number of customers with each card (blue, silver, gold and platinum) per income category. It is evident that majority of the customers hold a blue card (93.2% of customers). The number of customers for each card category decreases as you go from blue to platinum. For the blue and silver card majority of the customers earn less than $40k. Whereas for the gold and platinum card most of the customers earn $60k-$80k. This might suggest that those with a lower income are less likely to hold a gold or platinum card, however 10% of the data contains unknown information regarding income. This may impact the results as the gold and platinum cards have a very low number of customers (116 and 20 respectively), therefore we are unable to make accurate conclusions.

![Income Vs Card](https://user-images.githubusercontent.com/92734124/146634828-3e696c08-ccd2-4944-88c7-a1dc0c793971.JPG)


In the next graph we compared the card categories againt the number of existing and attrited customers in a stacked bar chart. From the existing customers, 93.1% held a blue card, with the numbers decreasing as you go from blue to platinum (93.1%, 5.6%, 1.1% and 0.2% respectively). This trend was also apparent in the attrited customers where 93.4% held a blue card, 5% (silver), 1.3% (gold) and 0.3% (platinum). From this data we can assume that card category cannot indicate whether a customer is likely to churn as the pattern is very similar across existing and attrited customers.

![Card Vs Attrited](https://user-images.githubusercontent.com/92734124/146634832-3fdd18f0-67aa-4367-98be-a50b28e3c5b4.JPG)

To conclude, majority of the customers are likely to hold a blue card regardless of income, however those with a higher earning are more likely to hold a gold or platinum card. This suggests that the 'better' cards are less accessible to those who earn less than $60k. When comparing existing and attrited customers there is no clear correlation between card category and customer status, suggesting that card category would not be an ideal variable to focus on when trying to identify indicators of churning. There is no clear target to avoid churning.

### Question 6 Analysis

FAO Nawaz


