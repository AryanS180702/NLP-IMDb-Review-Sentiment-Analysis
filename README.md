# IMDb Movie Review Sentiment Analysis

## Dataset

The dataset used for this project is available on Google Sheets:  
🔗 [IMDb Review Dataset](https://docs.google.com/spreadsheets/d/106x15uz8ccQ6Wvpc8-sYjXisBN8vewS435I7z3wd4sw/edit?usp=sharing)

It contains:
- **Total reviews**: 50,000
- **Target variable**: `Sentiment` (positive / negative)

Each entry includes a full-text movie review and its corresponding sentiment label.

## Steps Taken

1. **Data Exploration**  
   - Analyzed the class distribution to check for imbalance

2. **Data Preprocessing**  
   - Removed HTML tags, punctuation, digits  
   - Converted text to lowercase  
   - Tokenized text  
   - Removed stopwords  
   - Applied lemmatization

3. **Feature Engineering**  
   - Train-test split  
   - TF-IDF vectorization of text  
   - Extracted additional textual features like word count, character count, and average word length  
   - Scaled the numerical features for consistency

4. **Model Development**  
   - Trained multiple classification models:
     - Logistic Regression
     - Support Vector Machine (SVM)
     - Decision Tree
   - Performed hyperparameter tuning to improve performance

5. **Model Evaluation**  
   - Used classification report and confusion matrix heatmap  
   - Visualized model comparison using bar charts  
   - Created word clouds for positive and negative reviews to understand common themes

6. **Model Selection**  
   - **Logistic Regression** was selected for deployment due to its best accuracy and F1 score across the board

7. **Prediction Pipeline**  
   - Built a reusable prediction class that:
     - Takes raw movie review text as input  
     - Performs all preprocessing and feature extraction  
     - Returns the predicted sentiment (positive/negative)


## Results

After evaluating all the models, **Logistic Regression** was selected due to its strong overall performance. It achieved:

- **Accuracy**: 0.81  
- **F1 Score**: 0.81

These results indicate that the model performs consistently well in predicting both positive and negative sentiments, making it a reliable solution for text-based sentiment classification tasks.  
