# New York City Restaurant Inspections Analysis

Welcome to Our Repo!

### Business Problem

We have been hired by the NYS DOH to analize the current status of Restaurant Inspections in New York City. They are interested in automating and improving the process of Inspections to some degree and we have been tasked with:
   * Analizing the data to obtain relevant information.
   * Finding patterns that will help us understand how this is possible.
   * Finding a viable solution to our problem.

### The Data

* The dataset contains every sustained or not yet adjudicated violation citation from every inspection conducted.
* Only restaurants in an active status as of the RECORD DATE (11/04/2020) are included in the dataset.
* When an inspection results in more than one violation, values for associated fields are repeated for each additional violation record.

### EDA 

* How many eateries are chain owned or a franchise?
* Top 10 Most Common Violations
* Top 10 Chain Establishments with the most Violations
* Critical Flags
* ANOVA Test 2019: Average number of Violations by Grading

### Modeling

* We have no numerical features. 
* We transformed all of them in order to make them readable by ML models.
* 4 models were built for our case problem:

     * #### Logistic Regression 
     * #### Decision Trees:
         * SelectKBest 
         * Vanilla 
     * #### Random Forest
* Surprisingly a Vanilla Decision Tree was the best performer.


### Conclusions

* Considering that only about 11.2% of restaurants in our train set are chain owned or franchises, the amount of total violations they make up for is very high.
* Establishments with 45+ violations on record are Chain Restaurants.
* About half of all recorded violations are Critical Flags. This is dangerous since it is an indicator for how likely it is for a customer to get ill after eating at establishments who have critical violations.
* Adding an intercept did not improve our model.
* In real life, it is very unlikely for an eatery to have no violations at all during service. It is virtually impossible.
* The important thing is to differentiate which of these violations could cause eaters to get sick.
* For our problem, we want to keep False Negatives as low as possible, since we never want to predict a True Critical Flag as Non-Critical.
* Our best model predicted 20.55% of violations as False Negatives.
* Based on the Inspection Type and Grade an establishment gets, we can predict the likelihood of Critical violations.

### Future Work

* Explore new methods to tune and improve our model.
* This dataset offers a lot of opportunity for analysis.
