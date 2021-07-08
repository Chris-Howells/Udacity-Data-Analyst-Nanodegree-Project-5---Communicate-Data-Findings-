
# Dataset Exploration Title: Udacity Data Analyst Project 5 - Analyse and Visualise Prosper Loans Data

## by Christopher Howells


## Dataset: Prosper Loans

This dataset looks at loans from 'Prosper', which contains information related to the loan itself (such as amount, term length, expected return) and data on the borrower (such as their credit score limit, prospers rating of them and whether they are a homeowner or employed).
There are 113937 rows and 81 columns for the variables which gives us a rich dataset to examine.

To clean the data, I deleted the duplicate loans of which there were 889 discovered by having the same unique identifer (ListingKey), and dropped columns with more than 10% null values as this may affect the results of our analysis.

## Summary of Findings

Univeriate Analysis:

I have found that most loans on the book (56k) are currently in progress and around 38k loans in the dataset are completed. 5k have defaulted defaulted (failed to pay back) and 12k are 'Chargedoff' (a charge-off or chargeoff is a declaration by a creditor that an amount of debt is unlikely to be collected). Therefore around 15.3% of the total loans have either defaulted or paid less than the total value of the loan, with this number expected to increase, as the majority of loans are still 'current' so have the potential to not pay in full.

And that for those past due, the majority(at 800) are only between 1-15 days, then there is a large reduction between this and the other Past Due dates, suggesting that most people who fall behind get out of it (either by paying or defaulting or being charged-off).

Borrower APR for Prosper laons, is normally distributed roughly following a bell curve shape with a peak around 20%, which must be standard for the most common customer Prosper credit score. This is confirmed with both the mean and median being very close to this value (21.9% and 21.0%).

Biveriate Analysis:

Lender Yeild Vs Borrower APR: There is a positive linear relationship between Lender Yeild Vs Borrower APR, which I would expect as more interest means more income for the bank, and we can see that it is not offset by higher service fees for this lender.

There is a somewhat linear relationship with estimated losses and Borrower APR. I would expect the higher APR loans to be given to higher risk customers which could give a bigger overall loss if the higher profit from the higher rate of those performing loans, so a slight linear relationship makes sense here.
There is no linear relationship with Estimated Return a Borrower's APR. This is likely because as those with a higher APR are more risky so default losses wipe out the higher profit from the Interest Rate, and the safer loans which do not defaault as much, this is factored in with a lower Interest Rate which wipes out the return from that. So overall the loans will be valued based on their risk which stops those with higher/lower interest rates having a higher/lower return.

Multivariate Exploration:

We can see a significant relationship between the Numeric Prosper Rating which is negative with the borrows APR, so the higher the Rating, the lower the APR. This makes sense as the rating is essentially an internal credit rating of how good the borrower is. And so borrows that are more risky with a lower Prosper Rating are given higher Interest rates/APR's to compensate for taking on that risk.

There is a positive correlation with the customers upper credit score range and the Prosper Rating of 0.55 too, showing they are positively correlated suggesting that credit score could play an important role in a customers Prosper Rating. We can see that the 'loan original amount' is also 0.43 correlated with the Prosper Rating, so perhaps customers with a higher rating are able to borrow more.

Surprsingly Stated Income was barely related suggesting Prosper doesn't consider it relevant or could expect custoerms to be dishonest in supplying that information.

Borrower APR has a negative correlation with Upper Credit Score again likely as these people are higher risk and so are charged more to borrow by banks.

When looking at the Prosper Ratings interacting with the Borrower APR and Employment Status,'Self Employed', 'Part-time' and 'Retired' are always the higher APR for each Prosper Rating, which makes sense as these would be more risky than people in more stable full-time employment with a regular source of income.

When looking at how employment status, loan amount, and stated income interact with each other, if found that employed people all across the Loan amount, in the higher sections such as from $25,000 onwards it is almost entirely employed people, so perhaps unemployed/retired/part-time only people are blocked from getting higher amounts, or it counts significantly in the decision to give someone a loan, which we would expect as full-time employment is considered more reliable/safe.

When looking at how Borrower APR, IsHomeOwner and Prosper Rating interact, we can see that a higher portion of the highest Prosper Ratigns are Homeowners which makes sense as we would explect them to be the safest customers with higher incomes and less debt. however throughout the rest of the scale, particularly in the middle sections it is not so clear so the other factors (e.g. emplyoemtn status, credit score etc.) are more important. We can also see the interaction between Borrower APR decreasing with Prosper Rating as the customer is considered less risky.<

## Key Insights for Presentation


For the presentation, I think the main points I will focus on are what the Prosper Loans Score is influenced by. In this case we can see from the correlation matrix and heatmap that the Prosper Loans Score is largely based on credit score, but only 0.55 correlated, with little correlation with Stated Income which usually makes up a larger portion of bank loans. We also see that the 'loan original amount' is also 0.43 correlated with the numeric Prosper Rating, so perhaps customers with a higher rating are able to borrow more.
We can also see that a higher portion of the highest Prosper Rated customers on 6 and 7 are Homeowners which makes sense as we would explect them to be the safest customers with higher incomes and less debt. And the lowest rated customers at 1 and 2 have the opposite. However throughout the rest of the numeric rating scale, particularly in the middle sections there is not a clear trend of decreasing/increasing with home ownership so the other factors. We can see that for each Prosper Rating,'Self Employed', 'Part-time' and 'Retired' are always the higher, which makes sense as these would be more risky than people in more stable full-time employment with a regular source of income.

I will also examine how Borrower APR affects profit indicators. We can see that the higher the Borrower APR is, the higher the lender yeild is, suggesting that any rise in service fee is compensated for by the higher interest. There is a less linear relationship with estimated losses and Borrower APR, however it does look like there is some trend as we would expect the higher APR loans to be given to higher risk customers which would give a bigger overall loss (but this could have just as easily lead to more profit from the higher rate of those performing loans).Finally, there is no linear relationship with Estimated Return a Borrower's APR. This should be expected as those with a higher APR are more risky so default losses wipe out the higher profit from the Interest Rate, and the safer loans which do not defaault as much, this is factored in with a lower Interest Rate which wipes out the return from that. So overall the loans will be valued based on their risk which stops those with higher/lower interest rates having a higher/lower return.
