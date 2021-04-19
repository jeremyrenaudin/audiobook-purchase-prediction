# **Audiobook Purchase Prediction**
## **Project description**

The given data comes from an Audiobook app. Each customer in the database has made a purchase at least once, that's why he/she is in the database. We want to create an algorithm based on our available data that can predict if a customer will buy again from the Audiobook company.

The main idea is that if a customer has a low probability of coming back, there is no reason to spend any money on advertizing to him/her. If we can focus our efforts ONLY on customers that are likely to convert again, we can make great savings. Moreover, this model can identify the most important metrics for a customer to come back again. Identifying new customers creates value and growth opportunities.

the data is summarized in a .csv file.

### **Variables:**

*   Customer ID
*   Book length in mins_avg (average of all purchases)
*   Book length in minutes_sum (sum of all purchases. If equal to Book length in mins_avg, thus customers made 1 purchase only.)
*   Price Paid_avg (average of all purchases)
*   Price paid_sum (sum of all purchases. If equal to Price Paid_avg, thus customers made 1 purchase only.)
*   Review (Boolean variable. 1 = Customer left a review)
*   Review (out of 10)
*   Total minutes listened
*   Completion (from 0 to 1) => Total minutes listened / Total lengths of books the person has purchased
*   Support requests (number)
*   Last visited minus purchase date (in days) => measures the difference between the last time a person interacted with the platform and the first purchase date. The bigger the difference, the bigger the engagement.

So these variables are going to be the inputs of our model (excluding customer ID, as it is completely arbitrary).

### **Targets:**

The targets are a Boolean variable (0 or 1). We are taking a period of 2 years in our inputs, and the next 6 months as targets.<br />
In fact, we are predicting if based on the last 2 years of activity and engagement, a customer will convert in the next 6 months. If they do not convert after 6 months, chances are they have gone to a competitor or di not like the Audiobook way of digesting information.

**This is a supervised classification problem with two classes: won't buy and will buy, represented by 0s and 1s.**