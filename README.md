
# Netflix Recommendation System

<img width="1024" height="572" alt="image" src="https://github.com/user-attachments/assets/b71c10cc-6efe-4625-81a5-1858c48b7431" />


Overview
This project builds a movie recommendation system for Netflix using collaborative filtering techniques. It leverages matrix factorization (SVD) from the Surprise library to predict user ratings and recommend top movies. The system processes Netflix's historical rating data to generate personalized suggestions for users.

The notebook demonstrates:

Data loading and preprocessing from CSV and text files.
Building and training a recommendation model.
Generating predictions for specific users (e.g., User ID: 1331154).
Sorting and displaying top-rated movie recommendations based on estimated scores.
Key focus: Collaborative filtering to recommend movies unseen by the user, based on similar user preferences.

# Dataset:

https://drive.google.com/drive/u/0/folders/1NlfC1jAMmdUIt8DcJOitCYtpo7d6vvFD


# Technologies Used
Python: 3.x
Libraries:
pandas: For data manipulation and analysis.
surprise: For building and evaluating recommendation models (SVD algorithm).
numpy: For numerical operations.
Other: os, gc for file handling and memory management.
Environment: Jupyter Notebook (Colab compatible).
Installation
Clone the repository:
text
git clone https://github.com/yugal0708/netflix-recommendation-system.git
cd netflix-recommendation-system
Install dependencies:
text
pip install pandas surprise numpy
How to Run
Download the Netflix Prize dataset (e.g., from Kaggle or official sources) and place the files in the project directory.
Open the notebook: Netflix_Recommendation_system_by_Yugal.ipynb.
Run the cells sequentially in Jupyter or Google Colab.
Customize the user ID in the prediction section to generate recommendations for different users.
Example code snippet from the notebook:

Python
from surprise import SVD, Dataset, Reader
from surprise.model_selection import train_test_split

# Load data into Surprise format
reader = Reader(rating_scale=(1, 5))
data = Dataset.load_from_df(df[['Cust_Id', 'Movie_Id', 'Rating']], reader)

# Train SVD model
trainset, testset = train_test_split(data, test_size=0.25)
model = SVD()
model.fit(trainset)

# Predict for a user
predictions = [model.predict(user_id, movie_id) for movie_id in movie_ids]
Results
For a sample user (ID: 1331154), the system generates estimated ratings for unseen movies and recommends the top ones. Example output:

Movie_Id	Year	Name	Estimated_Score
3	1997	Character	3.912302
5	2004	The Rise and Fall of ECW	3.796595
6	1997	Sick	3.282034
8	2004	What the #$*! Do We Know!?	3.927108
16	1996	Screamers	3.155302
The model achieves reasonable accuracy on test data (e.g., RMSE evaluated in the notebook).

Limitations
Based on historical data (up to 2005); may not reflect current Netflix content.
Collaborative filtering only (no content-based features like genres).
Large dataset requires significant memory/processing time; consider sampling for quick runs.
Future Improvements
Incorporate hybrid methods (content + collaborative filtering).
Add genre filtering or user input for more personalized results.
Deploy as a web app using Flask/Streamlit.
Author
Yugal
GitHub: yourusername
Contact: your.email@example.com
If you find this project useful, give it a ⭐ on GitHub! Contributions and issues are welcome

Overview
This project builds a movie recommendation system for Netflix using collaborative filtering techniques. It leverages matrix factorization (SVD) from the Surprise library to predict user ratings and recommend top movies. The system processes Netflix's historical rating data to generate personalized suggestions for users.

The notebook demonstrates:

Data loading and preprocessing from CSV and text files.
Building and training a recommendation model.
Generating predictions for specific users (e.g., User ID: 1331154).
Sorting and displaying top-rated movie recommendations based on estimated scores.
Key focus: Collaborative filtering to recommend movies unseen by the user, based on similar user preferences.

Dataset
Source: Netflix Prize Dataset (publicly available for research).
Files Used:
movie_titles.csv: Contains movie IDs, release years, and titles.
combined_data_*.txt: User ratings data (e.g., combined_data_1.txt, etc.), with millions of ratings.
Size: Over 15,000 movies and sample user ratings (truncated in the notebook for demonstration).
Preprocessing: Merged ratings with movie titles, handled missing years, and prepared data for the Surprise library.
Note: The dataset is large; the notebook handles sampling or partial loading to avoid memory issues.

Technologies Used
Python: 3.x
Libraries:
pandas: For data manipulation and analysis.
surprise: For building and evaluating recommendation models (SVD algorithm).
numpy: For numerical operations.
Other: os, gc for file handling and memory management.
Environment: Jupyter Notebook (Colab compatible).
Installation
Clone the repository:
text
git clone https://github.com/yourusername/netflix-recommendation-system.git
cd netflix-recommendation-system
Install dependencies:
text
pip install pandas surprise numpy
How to Run
Download the Netflix Prize dataset (e.g., from Kaggle or official sources) and place the files in the project directory.
Open the notebook: Netflix_Recommendation_system_by_Yugal.ipynb.
Run the cells sequentially in Jupyter or Google Colab.
Customize the user ID in the prediction section to generate recommendations for different users.
Example code snippet from the notebook:

Python
from surprise import SVD, Dataset, Reader
from surprise.model_selection import train_test_split

# Load data into Surprise format
reader = Reader(rating_scale=(1, 5))
data = Dataset.load_from_df(df[['Cust_Id', 'Movie_Id', 'Rating']], reader)

# Train SVD model
trainset, testset = train_test_split(data, test_size=0.25)
model = SVD()
model.fit(trainset)

# Predict for a user
predictions = [model.predict(user_id, movie_id) for movie_id in movie_ids]
Results
For a sample user (ID: 1331154), the system generates estimated ratings for unseen movies and recommends the top ones. Example output:

Movie_Id	Year	Name	Estimated_Score
3	1997	Character	3.912302
5	2004	The Rise and Fall of ECW	3.796595
6	1997	Sick	3.282034
8	2004	What the #$*! Do We Know!?	3.927108
16	1996	Screamers	3.155302
The model achieves reasonable accuracy on test data (e.g., RMSE evaluated in the notebook).

Limitations
Based on historical data (up to 2005); may not reflect current Netflix content.
Collaborative filtering only (no content-based features like genres).
Large dataset requires significant memory/processing time; consider sampling for quick runs.
Future Improvements
Incorporate hybrid methods (content + collaborative filtering).
Add genre filtering or user input for more personalized results.
Deploy as a web app using Flask/Streamlit.
Author : Yugal
GitHub: Yugal0708
Contact: yugalbilawane0514@gmail.com
If you find this project useful, give it a ⭐ on GitHub! Contributions and issues are welcome
