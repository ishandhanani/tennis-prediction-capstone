# Pre-Match Data Tennis Prediction Model

For my M.S capstone project, I decided to take a Machine Learning Approach to predicting tennis matches. A large thanks to Jeff Sackmann for hosting an open-source tennis dataset and Nick Devin for his intricate pandas wizardry when it came to building some of the metrics.

For more information on the project, visit the final_report folder to view the paper and presentation. I recieved a 94/100 overall on the project. Overall, this project was an excellent way to understand the practical nuances that come with applying complex non-parametric models to real world data. I'm excited to continue tweaking with this algorithm and adding as time goes on. 

# The repository

This repository contains a copy of ATP match data from the Jeff Sackman dataset from the years 2000 to 2019. This is directly used in the `data_preprocessing` notebook.

The `processed_data` folder contains three different csv files. The `sortedh2h.csv` file is the first checkpoint before any feature engineering happens. It's a combination of all the individual csv files and has all irrelevant columns dropped and/or cleaned. The nonsparse.csv metric uses a confidence metric designed by Nick Devin and is defined by overall win % + log(1-(overall win %) + (last 6 months win %)). The `nonsparsetheta.csv` is a metric that I designed to compare against Nick's. It is defined as overall win % + (last 3 months win %) ^ theta. I used various values of theta to test and found that 0.09 works best. 

The ml_workflow noteboook is the different models that I used to create the prediction algorithm. Due to training limitations, I was not able to tune the Random Forest, XGBoost, or ANN for optimal performance. This was also my first attempt at training models on the Texas A&M Cloud Clusters. 
