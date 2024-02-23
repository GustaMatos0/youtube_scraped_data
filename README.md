# YouTube Views Predictor

## Overview
The "YouTube Views Predictor" project aims to forecast the number of views a YouTube video will receive based on various textual features such as title, description, and keywords, along with other metadata like channel information, video duration, and publication date.

## Data Collection
The dataset used in this project was obtained through web scraping, extracting information from YouTube videos. To replicate the data collection process, refer to the `youtube_scrap` notebook. Note that due to the large volume of data, the scraping process can be time-consuming.

## Data Preparation and Modeling
Once the dataset is collected, it undergoes extensive preprocessing and feature engineering. This includes tokenization using Word2Vec for capturing word meanings within a context, TF-IDF vectorization to measure word importance, and embedding techniques like GloVe and FastText (for experimentation). Additionally, numerical features such as video duration and publication date are converted into a usable format.

### Modeling Approach
Several regression models are trained and evaluated to predict the number of views. These models include:
- Ridge Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost Regressor
- LightGBM Regressor

## Conclusion
The best performing model was found to be the Random Forest Regressor, achieving an R² score of approximately 0.65. Ensemble models, such as Random Forest and Gradient Boosting, demonstrated superior performance, indicating their effectiveness in this context. However, there is potential for further improvement, particularly with the inclusion of more data and fine-tuning of models.

## Repository Contents
- `youtube_scrap.ipynb`: Notebook for web scraping YouTube data.
- `youtube_predict.ipynb`: Notebook for data preprocessing, modeling, and evaluation.

For more detailed insights and code implementation, refer to the `youtube_predict` notebook.
