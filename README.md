# Name: Umesh Dhakal
# Course: MSCS634
# Professor: Dr. Satish Penmatsa
# February 13, 2026
# Lab 2: KNN vs Radius Neighbors Classification

# Purpose of the Lab
The purpose of this lab is to understand and compare two distance-based classification algorithms:K-Nearest Neighbors (KNN) and Radius Neighbors (RNN). Using the Wine dataset, I trained and tested both models to see how their accuracy changes with different parameter values. This lab helped me better understand how distance, neighbors, and parameter tuning affect classification performance.

## Key Insights and Observations
Based on the output results, KNN showed more consistent and stable accuracy across different values of k. Even when the value of k changed from small to larger values, the accuracy stayed relatively high. This happens because KNN always looks at a fixed number of nearest neighbors before making a decision, so every test data point always gets classified. When k is very small, the model can be sensitive to noise, but as k increases, the prediction becomes more balanced and less affected by individual data points.
Radius Neighbors behaved differently compared to KNN. The accuracy values for RNN depended heavily on the chosen radius. With smaller radius values, some data points did not have enough neighbors within the radius, which can reduce accuracy. As the radius increased, more neighbors were included, and accuracy improved, but after a certain point, increasing the radius did not help much because the model started using too many distant neighbors. This reduces the advantage of local decision making.
From the output results it show that KNN is more reliable and easier to control using the k parameter, while RNN requires careful selection of the radius value. This explains why KNN performed more consistently in this lab, while RNN was more sensitive to parameter changes.

## Challenges and Decisions
One challenge in this lab was handling cases in Radius Neighbors where no neighbors were found within the given radius. To avoid errors and ensure predictions, I used the most common training class as a fallback label.
