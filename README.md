# Blackspots-Detection-with-Logistics-Regression

## 1.1. Business understandings and problem
Accident hotspots, also known as blackspots, is one of the biggest concerns for public safety. It is of interest of organizations, like the DOT, to study these spots and put in proper measures to improve road safety.

Assuming the position of a data consulting firm, CrashAnalytics, I can help the deparment learn more about blackspots via data analytics and provide insights into what constitute such areas.

## 1.2. Methodology

Using a dataset on traffic, I will use data analytics(for example, data aggregation and visualization, univariate, bivariate analysis)  to analyze and reveal hidden patterns and insights. Every aspect of an area will be analyzed and be observed in relationship with blackspots. Insights will be provided with each analysis.
Moreover, a classification model will also be developed to reveal hidden patterns in the data in conjunction with blackspots. Such model can also be used to process new data to determine the emergence of blackspots and allow preventive measurs to be taken before accidents can happen.

## 1.3. Outcomes and recommendations

The logistic model produced accuracy level of 0.9. Despite this number, its recall is low, 0.34. This means that the model is conserved in deeming areas as blackspots and it missed quite a handful of blackspots in the testing dataset. However, when it does make such conclusion, it is fairly reliable.

The classificatin model show a clear depiction of how the model make decisions. It can be found as below:

Blackspot=  -3.469 + 2.739 *Intersection + 4.314 *Lq_Licenses + 3.317 *CARS_ZERO_HH_PCNT + 1.088 *traffic_signal+ 1.321 *AGE_65YRS_OVER_PCNT

From the model formula, there are several things to note. To begin with, the number of liquor license plays one of the most important, if not the most important, roles in detecting a blackspot. With a overall intercept of -3.4 and coefficient of around 4.3, the existence of a single liquor license in the area already makes the place highly likely to be a blackspot. Granting a liquor license should be carefully considered and be accompanied by preventive measures to ensure safety in traffic.

Intersection is the next big factors in blackspot. Such part of a road is where there is heavy traffic that come from multiple directions and has a much higher chance for accidents. Traffic signals, though help regulate the traffic and ensure safety for all, can also be indicator of heavy traffic like intersection and thus, increase the chance of a road segment to be blackspot. It is highly recommend. Though these factors on their own do not make a place a blackspot, they do require more investigation into the areas’ safety level, especially when combined with other variables that positively correlated to blackspots like liquor license.

CARS_ZERO_HH_PCNT, though having a big coefficient value, is actually not affecting much to blackspot as the mean value of the variable is small (mean value is 0.06 for examples of blackspots). AGE_65YRS_OVER_PCNT has the same story as its mean value is only about 0.24  (counting only examples positive with blackspot).
In addition to the above recommendations, there are also a few points about the model itself. As mentioned above, one of the most important factors of the model performance is the choice of features or predictors. At the moment, the model uses only 5 variables as predictors as they are the most promising on paper. However, with domain knowledge and deeper understanding of blackspots, better set of predictors can be found and produce a better model. Furthermore, the current model is also under the influence of a heavy class imbalance. To be specific, the dataset given to train and test the model have much more non-blackspot examples than that of blackspot examples. This makes the model perform poorly in terms of true positive rate and might miss a lot of road segments that are supposed to be blackspots.The model, therefore, is likely to be substantially improved if given more examples of blackspot examples.
