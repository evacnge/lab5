# lab5
Comparison of top_k Values

In this experiment, building on the work done in Lab 5, we evaluated the impact of different values of top_k (3, 5, and 6) in reducing the cardinality of the Item_Name feature.

The results were as follows:

top_k = 3 → Accuracy = 0.3906
top_k = 5 → Accuracy = 0.3852
top_k = 6 → Accuracy = 0.3918

The results show that increasing top_k does not consistently improve model performance. While top_k = 6 achieved the highest accuracy, the improvement was minimal. This suggests that the Item_Name feature has a limited impact on the model.

Feature Importance Comparison

We analyzed the top feature importances across different values of top_k. The most important features remained consistent in all experiments.

The top important features included:

Delivery_Distance_km (~0.0849)
Driver_Lat (~0.0834)
Driver_Lon (~0.0831)
Customer_Lon (~0.0830)
Restaurant_Lon (~0.0828)
price_per_item (~0.0827)
Total_Price (~0.0808)

In contrast, the Item_Name_reduced feature had very low importance (e.g., ~0.013), indicating that it contributes very little to the model’s predictions.

This explains why changing top_k had only a minor effect on accuracy, as the model relies more on numerical and location-based features.

Additional Feature Engineering

We introduced new features to enhance the model’s performance, extending the feature engineering process from Lab 5:

is_large_order: Indicates whether the order quantity is greater than 3
is_expensive: Indicates whether the order price is above the median

These features help capture ordering behavior and improve the model’s ability to learn patterns from the data.

Conclusion

Overall, the model performance is mainly influenced by distance, location, and price-related features. Adjusting top_k had only a minor effect, and the Item_Name feature played a limited role in prediction.

Student Information

Name: Jafi Fahad
Student ID: 2240004698
