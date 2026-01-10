

# 🎬 Netflix Recommendation system

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/42a72ee6-1dc2-4f4f-87e4-72acb35bebea" />

A machine learning based movie recommendation system built using collaborative filtering. This project uses the Netflix Prize dataset and Singular Value Decomposition (SVD) to predict user ratings and recommend movies based on user preferences.

 # 📌 Project Overview
Recommender systems play a key role in modern platforms like Netflix, Amazon, and Spotify. They help users discover relevant content from massive datasets.

This project focuses on:

Understanding user movie rating behavior

Building a collaborative filtering model

Predicting unseen movie ratings for users

Generating personalized recommendations

 # 🧠 Recommendation Approach
This project uses Collaborative Filtering with Matrix Factorization (SVD).

Why SVD?

Works well with sparse user–item matrices

Scales efficiently for large datasets

Produces accurate rating predictions

The implementation is done using the Surprise library.

 # 📂 Dataset
Source: Netflix Prize Dataset

Data Used:  https://drive.google.com/drive/u/0/folders/1NlfC1jAMmdUIt8DcJOitCYtpo7d6vvFD

Customer ID

Movie ID

Ratings (1–5)

Due to size constraints, only a subset of the dataset is used for training and evaluation.

⚠️ Dataset is not included in the repository. You must download it manually.

 # ⚙️ Tech Stack
Programming & Libraries
Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-Surprise

Environment
Google Colab

Jupyter Notebook

 # 🔧 Model Building Steps
Load and preprocess Netflix rating data

Handle missing values and data formatting

Convert dataset into Surprise compatible format

Train SVD model

Evaluate model using RMSE

Predict ratings for unseen movies

Recommend top movies for a specific user

 # 📊 Model Evaluation
Metric Used: RMSE (Root Mean Square Error)

Validation: 3-Fold Cross Validation

This helps measure how close predicted ratings are to actual user ratings.

 # 🎯 Recommendations
The system:

Takes a user ID

Predicts ratings for movies the user has not watched

Ranks movies based on estimated scores

Outputs personalized recommendations

Example:

model.predict(user_id, movie_id).est

 # 🚀 How to Run the Project
Clone the repository

git clone https://github.com/yugal0708/netflix-recommendation-system.git
Open the notebook in Google Colab or Jupyter

Install required libraries

pip install scikit-surprise
Upload Netflix dataset to your environment

Run cells step by step

 # 📈 Future Improvements
Add content-based filtering

Hybrid recommendation system

Deploy using Streamlit or Flask

Improve performance with hyperparameter tuning

Use full Netflix dataset

 # 👨‍💻 Author
Yugal Bilawane
BSc Data Science 
AI & Data Science Certification – iHub IIT Roorkee
