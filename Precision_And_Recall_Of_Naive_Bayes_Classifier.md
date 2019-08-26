# Precision_And_Recall_Of_Naive_Bayes_Classifier
This project evaluates the effectiveness of Naive Bayes classifier with Precision, Recall and F-measure metrics on movie reviews dataset. 

#### **CLASSIFIER PRECISION**

Precision measures the exactness of a classifier. A higher precision means less false positives, while a lower precision means more false positives. This is often at odds with recall, as an easy way to improve precision is to decrease recall.

![img](https://lh3.googleusercontent.com/yQzQyotqwlDYSZxztqU7QthzDCDpcerdXepPyOWqUFNXRnJE2TvBVo7u4i1wEytDAYY6xOxrxU2kQzRsvQrteqlAY34Jl3APa8MRYehvQcQtz1Co59gDtatnv7KHm1kh-4I4x7pxHwrgV4SJrg)





#### **CLASSIFIER RECALL**

Recall measures the completeness, or sensitivity, of a classifier. Higher recall means less false negatives, while lower recall means more false negatives. Improving recall can often decrease precision because it gets increasingly harder to be precise as the sample space increases.

![img](https://lh5.googleusercontent.com/y6sZvQ1e8M8DisyTRUn7wb1JnO68vjgf7raCKlQOjApxtBPDYTVlgdB3w4izxjsRxqis3H-HavnKZcUiB71cTusl1caaiF6Oh8nhkd8IAVDVRlLRrpbW1eE0dqcPzgf_UaEDQ1kQMDfGjp2gdA)



#### **F-MEASURE METRIC**

Precision and recall can be combined to produce a single metric known as F-measure, which is the weighted harmonic mean of precision and recall. I find F-measure to be about as useful as accuracy. Or in other words, compared to precision & recall, F-measure is mostly useless, as you’ll see below.

![img](https://lh5.googleusercontent.com/3lTuIic149QCvc0j3PdG-4BZSoysv_GSVIh_LN_GV5yPgCD4BzeyJbwj3n2ZwzSSb_0EWh1CnRMZ6oIBZmXtqrKO1_aBsXoO24G8uXjM1wPL8zwh2BdvUJCUzzZ4CaoCuS2s6OWqSmY_vL_EOg)



#### **CHI-SQUARED DISTRIBUTION**

The chi-squared distribution is used primarily in hypothesis testing. Chi-square distribution, showing X2 on the x-axis and P-value on the y-axis. A chi-squared test, also referred to as a test (or chi-square test), is any statistical hypothesis test wherein the sampling distribution of the test statistic is a chi-square distribution when the null hypothesis is true. Chi-square is a statistical test commonly used to compare observed data with data we would expect to obtain according to a specific hypothesis.

![img](https://lh4.googleusercontent.com/P6ENoG5JLNqiRwvFYhfeo0LRHe9Wjhhs-gyHcs5fITTOP157K7LTrcAZl-rUUJ_VpFWHGQ6EzBYwM7RTvqIgikJuRsf10E4nAFDwu91M0Wo-MA3CbRRDMcnmHy7gKcG1MRAnYLQAJ9KF3qTc-g)



![img](https://lh5.googleusercontent.com/7voyh35fMyV9qSW2PLcD1vDBCYxa8_c8ypi6sqf7ZiL1f8_MAiE-xEljSCJjn4FG5l2lpMEHBOdctl9WLzOJD4PNQTVmjXrW1obQ3ETYNaiCMsu3jJ9YdVv0Z3gluYThC3lD9xOEg0yfeNyraw)



#### **PROCEDURE**

One of the best metrics for information gain is chi square. NLTK includes this in the BigramAssocMeasures class in the metrics package. To use it, first we need to calculate a few frequencies for each word: its overall frequency and its frequency within each class. This is done with a FreqDist for overall frequency of words, and a  ConditionalFreqDist where the conditions are the class labels. Once we have those numbers, we can score words with the BigramAssocMeasures. Chi_sq function, then sort the words by score and take the top 10000. We then put these words into a set, and use a set membership test in our feature selection function to select only those words that appear in the set. Now each file is classified based on the presence of these high information words.