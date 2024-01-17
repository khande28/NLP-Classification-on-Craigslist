# Improving categorization on Craigslist
  1. Introduction
  2. Objective
  3. Methodology
  4. Data Sources
  5. Data Dictionary
  6. Data Pre-processing
  7. Feature Engineering
  8. Model Development
  9. Result
  10. Limitations

# Introduction
  1. Craigslist is a classified advertisement site with sections for community, housing, jobs, sales, and services.
  2. Often there is misclassification of products across sections, especially in the Computers category.
  3. This can lead to a discouraging user experience and engagement on the website.
  4. There lies an opporunity for enhancing customer satisfaction and business performance.
  5. Intention is to solve the issue by employing advanced modeling techniques to quickly identify and accurately recategorize misclassified products, improving browsing experience.

# Objective
 1. Even though Craigslist is one of the biggest adverstising website, there are potential problems faced by users. One such problem is to find appropriate product on the computer section. Certain product that should be under computer parts section are present under the computer section.
 2. The motivation is to use the unstructured data and recategorize the product into pre-defined existing categories.

# Methodology
![image](https://github.com/khande28/NLP-Classification-on-Craigslist/assets/140965175/ab201ca6-12a7-4261-b733-0f86ac2b8849)

# Data Sources
 1. The data has been scraped from existing computer section on the Craigslist website.
 2. This was done for 2 cities (San Francisco and Chicago).
 3. Dataset: 4 columns and 2143 rows.

# Data Dictionary
 1. Label: Assigned by the yser whether the given product is a computer or not.
 2. Product_URL: Link for the product on the craigslist website.
 3. Content: The intext material for each of the URL.
 4. Header: Header for each of the listing.
 5. Extracted_URL: Part of original Product_URL used.
 6. Flag: To indicate whether a product is a computer or not.
 7. Cleaned_URL: Final URL which is processed.
 8. Below is the image for the first five records of the final dataset.
    ![image](https://github.com/khande28/NLP-Classification-on-Craigslist/assets/140965175/794b70dd-d36c-410b-ae61-0d3e765202f5)

# Data Pre-processing
 1. The Product_URL contains a specific part that should be used in the process to have a good model, so we took the substring from it to create a new variable as Extracted_URL.
 2. Label encoding is done for the Label Column to create a new variable Flag.
 3. The data needs to be cleaned further so below mentioned pre-processing steps were carried out.
    * Tokenization: Each of the element has been tokenized into words.
    * Lemmatization: Each of the tokenized element is converted to its root word.
    * Stopwords: Removal of frequently used words is done for the above lemmatized elements.
 4. The cleaned words are again merged to create the sentences and are stored in dataframe which is later merged with the original dataset.

# Feature Engineering
 1. **Tfidf Vectorizer**
    * Tfidf is a method to converts text documents into a matrix of TF-IDF features.
    * In this method, the words which are repeated in less frequency are given higher weights as compared to others.
    * With min_df, the number of dimensions are further reduced by removing words which are very low in frequency.
    * n_gram can help include the order to n words as a phrase. However, it will tend to higher dimensionality.

# Model Development
 1. Once the data is pre-processed and ready to use, they are passed onto different models and the accuracy score are reported.
 2. To enhance the predictablity of the models, techniques such as GridSearchCV to identify the best parameters to be used in the model.

# Results

Below is the accuracy result for all the models that were ran in the process. We can see that **Naive Bayes and CatBoost** performs slightly better than rest of the models.


![Screenshot 2024-01-16 204605](https://github.com/khande28/NLP-Classification-on-Craigslist/assets/140965175/0a8c0c6e-b73d-49f8-8e5d-37e96ac9add4)

# Limitations
 1. Manual labelling of input data is a cumbersome process.
 2. To enhance the predictability of the model, more input data can be used.
 3. The process is limited to text analysis but can be extended to image-processing as well.
 4. Hypertuning can be done to all the models.




