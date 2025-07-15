# Lab 6: Association Rule Mining – MSCS 634

## Purpose  
The purpose of this task is to conduct an analysis that demonstrates market basket analysis using the Apriori and FP-Growth algorithms. We will train the model using a subset of the Instacart dataset since the dataset was too big for the model to be able to handle the entire dataset successfully. The dataset consists of different CSV files, each holding different data about the customers and products they purchased. For this analysis, we used `orders`, `products`, and `order_products__prior` datasets. 

## Key Insights  
- The first insight we gain from the analysis is that the most frequent items are **bananas** and **organic fruits**, since they were top sellers.  
- We also found that a number of item pairs had strong **lift** and **confidence**, which is an indication of co-purchases and hence strong rules.  
  - For example, `[bag of organic banana and organic hass avocado]` and `[banana and organic strawberries]` are co-purchased most, followed by `[organic baby spinach and banana]`.  
- We have used **data visualization** to communicate the insights gained from the analysis.  
  - Most of the charts are bar charts, but there is also a **scatter plot** showing the relationship between confidence and lift, which is used to show the valuable association patterns in the dataset.  

## Challenges  
- The main challenge faced was due to **memory constraints** because the machine being used did not have enough resources (such as RAM) to process the entire dataset.  
- Therefore, we used a **sample of 10 products** and **limited transactions**.  
- Lastly, we used `TransactionEncoder` for one-hot encoding and filtered association rules by **confidence ≥ 0.03**, because no rules were generated when the threshold was higher.
