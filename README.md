# DDB_RP_Implementation
Fragment Summarization

# Proposed Work :
Paper mention fragment summarization technique and pseudo code for generate fragment summary.
By using sorted value of attribute we decide pattern range and generate patterns.
We Implemented the algorithm to generate data fragment summaries from the generated patterns and improve query performance.
We also try to get and improve QET of aggregate query 

# Proposed Technique Flow:
![image](https://user-images.githubusercontent.com/45670873/184528749-ca03d7fd-178e-4601-84bd-46268ed18b34.png)

# Data Structure:
![image](https://user-images.githubusercontent.com/45670873/184528783-e9058ffb-79a0-48b7-ad62-053aee9a7f75.png)

# Experiments: 
Dataset : Citypulse-Pollution data set is a public data set from the UCI machine learning repository
Number of Tuples : 7.8 M
Number of Attributes: 8

For experiments, We have chosen ozone attribute for generating patterns,
Good AQI <= 49
Average > 50 and <= 149
Poor > 149
Evaluation Parameters: 
Ozone AQI classes Summarization
Full scan vs. Fragment summaries QET
Data Scaling

# Experimental Runs:
![image](https://user-images.githubusercontent.com/45670873/184528847-0d53dcf4-fc03-4ac7-b71c-133f356a3640.png)

# Full Scan Vs Fragment Summaries QET :
![image](https://user-images.githubusercontent.com/45670873/184528883-d00775d8-abc9-4c84-ae9d-11d987038eb6.png)

#Conclusion:
We have introduced a method for generating patterns and fragment summaries AQI Class summarization analysis

We got 824 good patterns, 1489 average patterns, and 664 poor patterns by keeping timestamp as constant on level 1 patterns. While for other attributes like CO, SO2, and NO2, we got more than 50k  patterns for 1L data tuples, Which is entirely irrelevant. For fragments, summarization chooses those patterns which give an optimized answer.

Scaling Experiment
55% and 42.4% gain on 2x scaled data for cold and hot run respectively.
62.5% and 54.3% gain on 5x scaled data for cold and hot run respectively.

Query Execution time analysis
39% and 42.2% gain on 1x scaled data for cold and hot run respectively. Overall 49.25% 
The extension of this study is on how to make application that the original query directly converted for fragment summaries.


# References :
1. Exploring and Comparing Table Fragments With Fragment Summaries by Fatma-Zohra Hannou, Bernd Amann,Mohamed-Amine Baazizi.

2. Aggregate Query Result Correctness using Pattern Tables by Nitish Yadav, Ayushi Malhotra, Sakshee Patel, and Minal Bhise.

