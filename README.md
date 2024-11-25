# final_project_imp_25
# PROJECT TITLE 
Prediction of hotel cancellations

## NON-TECHNICAL EXPLANATION OF YOUR PROJECT

My project explores the factors influencing hotel booking cancellations. Using a detailed dataset, including guest details and booking methods, the project employs advanced machine learning techniques to predict whether a booking will be canceled. By leveraging the XGBoost model, which efficiently handles large datasets and missing values, we gain insights into key predictors of cancellations. The model's ability to highlight important features helps identify trends and inform hotel management strategies to reduce cancellation rates. This project aims to enhance decision-making for hotels, ultimately improving customer satisfaction and optimizing booking processes.


## DATA
A summary of the data you’re using, remembering to include where you got it and any relevant citations. 
The data is originally from the article Hotel Booking Demand Datasets, written by Nuno Antonio, Ana Almeida, and Luis Nunes for Data in Brief, Volume 22, February 2019. The data was downloaded and cleaned by Thomas Mock and Antoine Bichat for #TidyTuesday during the week of February 11th, 2020.
Hotel Booking Demand Datasets: Nuno Antonio, Ana Almeida, Luis Nunes, Data in Brief, 2019
Collection Methodology
Data was downloaded from: https://www.sciencedirect.com/science/article/pii/S2352340918315191 and cleaned by Thomas Mock and Antoine Bichat as part of #TidyTuesday: https://github.com/rfordatascience/tidytuesday/blob/master/data/2020/2020-02-11/readme.md
Link to the dataset: https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand/data

This data set contains a single file which compares various booking information between two hotels: a city hotel and a resort hotel.
This data set contains booking information for a city hotel and a resort hotel, and includes information such as when the booking was made, length of stay, the number of adults, children, and/or babies, and the number of available parking spaces, among other things.
All personally identifying information has been removed from the data.

## MODEL 
XGBoost, Liscence: Apache License 2.0

In this project, I utilized the XGBoost model to analyze a hotel booking dataset, focusing on whether bookings were canceled. The decision to use XGBoost was driven by several key factors:

Firstly, XGBoost excels in handling large datasets and processing them efficiently, delivering accurate results swiftly. This capability is crucial for scalability, allowing the model to accommodate additional data from multiple hotels and extended time periods without hindering performance.

Furthermore, XGBoost’s built-in functionality for handling missing values made it particularly suitable for real-world datasets, where such issues are common. It also integrates L1 and L2 regularization techniques, which are vital for mitigating overfitting by penalizing overly complex models and ensuring robust predictions.

Another advantage of using XGBoost is its ability to provide feature importances. This feature enhances our understanding of which variables significantly impact booking cancellations, offering valuable insights that can guide strategic decision-making. Overall, XGBoost's efficiency, scalability, and interpretability made it the ideal choice for this analysis.


## HYPERPARAMETER OPTIMSATION
Description of which hyperparameters you have and how you chose to optimise them:
The goal was to improve model accuracy while maintaining generalization across unseen data.  

- **`max_depth`:** Tested values [3, 4, 5]. Increasing up to 5 improved performance by capturing more complex patterns.  
- **`learning_rate`:** Explored [0.1, 0.01, 0.05]. Found 0.1 achieved the best accuracy, balancing learning speed and convergence.  
- **`gamma`:** Evaluated [0.05, 0.1, 0.2]. A gamma of 0.2 offered optimal regularization, enhancing accuracy with minor complexity increase.  
- **`subsample`:** Considered [0.7, 0.8, 1.0]. Setting at 0.8 balanced bias and variance, improving generalization without underfitting.  
This structured approach ensured a thorough coverage of potential configurations, allowing for an informed selection of optimal hyperparameters.  

## RESULTS
A summary of your results and what you can learn from your model 

You can include images of plots using the code below:
![Model_summary](Model_summary1.png)
![Model_summary](Model_summary2.png)
