Project Brief
Problem Statement:
This bank wants to automate their loan approval process in order to make the process more efficient, save money and make their system generally easier. Unfortunately they do not know how to determine if a loan will be successful or not. Meaning, if the loan will be paid back in their agreed upon timeline. This can be achieved by creating a predictive model able to determine whether or not an individual loan holders will turn out favourable or unfavourable.

Current State:
The data that is available to us is the data from 682 loan accounts containing information on transactions, gender, dates, loan amounts, duration, payments, their district area and much more. Additionally, we have access to accounts at the bank that do not have loans as well totaling 4500 accounts.

Data Preparation:
The dataset was for the most part was error-free because the data frame was created from an SQL database and imported to pandas. There were some NaN values but for variables that were not essential for the predictive model. Before doing any more pre-processing of the data, exploratory data analysis was performed. From this EDA some interesting statistics that were found are as follows; 25% of all the loans were from accounts that had credit cards and 6.6% of the loans that either defaulted or were behind on payments had credit cards, 21% of the accounts were shared account ,meaning 2 clients, and 0 of those accounts had defaulted or were behind on payments. Additionally, one of the accounts was mislabeled as being paid back as $12,273 was still owed and several other accounts actually overpaid on their loans. Following that, in order to apply a predictive model, certain features still had to be created or manipulated. From the transaction data of each of the accounts, 3 features were created to show the minimum, maximum and average balance of the account before acquiring the loan. The reason for only taking the transaction before the loan is because the predictive model will be working with accounts that have not yet gotten a loan so this must stay consistent while building the model. The next feature that was created in order to potentially increase accuracy is the age of the account holder at the time of getting the loans. This was simply calculated by subtracting the loan date from their respective birth dates. Lastly, a number of the columns still need to be enumerated as their were categorical variables. And those were: status(Good or Bad), loan payment frequency, card type, disposition type(owner or disponent) and gender. There was no need to scale the data as a decision tree classifier was being used. However, the data still needed to be balanced because there were much more good loans(1) than bad loans(0). This was completed by using the resample method and the data was made even before modelling commenced.
Modeling: 
Many different predictive models were used on this data however the decision tree classifier was used because it performed the best on every metric. The metric that was most favored was the precision score as we were concerned more with reducing False Negative predictions rather than false positives. With that being said it still out performed the other models for accuracy and recall. The precision score was 96%, the accuracy score was 95% and the recall score was 93%. From the model, the features that were found to contribute most to a successful loan were having a high minimum and average balance as well as a credit card. The factors which contributed most to a bad loan were having higher monthly loan payments, higher loan amounts as well as having a high maximum balance. Additionally, after running the model back through all the accounts, the amount that would have been saved if this model was applied prior to approving the bad loans would have been $7,448,063 out of the $7,821,217.00 still owed. Which is 95% of the total outstanding from bad loans that could have been recovered.

Recommendations and Future Work:
In order to reduce losses to the bank as well as produce more income, this company should market loans to credit card holders as they were great indicators of successful loan holders, they should also market loans to shared accounts holders for the same reason and lastly, they should apply the decision tree model to vet future loan applicants as it has proved to be a valuable tool. In future it would be beneficial to apply a clustering model to all the accounts for customer segmentation in order to learn more about the bank’s clients. Additionally, tracking the transaction behaviour of accounts that are about to default or miss a payment may tell us more about what we can do to prevent bad loans from occurring. Thirdly, it would be interesting to see how the model will perform when applying it to all the accounts with the bank that do not have loans and seeing which clients are favourable loan holders. Lastly, more investigation is needed into why having a high maximum balance contributed to bad loans, determining why that is will help reduce losses further.

Output/Deliverable/Usage: 
The deliverable for this project was to produce a predictive model for the bank to use to automate the loan approval process going forward as well as provide any other actionable insights that would prove valuable to them.
Stakeholders:
Operations Team

Due Date:
July 26th 2019

Measures of Success:
The measure of success for this project will be based on the effectiveness of my predictive model. The current precision score is at 96% however that may change once implemented towards new potential loan holders. Additionally, the outcomes of the recommendations to market loans to accounts with credit cards as well as shared account holders would be a measure for the performance of this analysis.

Summary:
Total of $7,821,217.00 is owed from bad loans
Model can predict bad loans 96% of the time, should be used for approval process
Market loans to credit card holders 
Market loans to shared account holders

