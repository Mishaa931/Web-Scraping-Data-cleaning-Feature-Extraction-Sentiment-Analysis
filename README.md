# Web Scraping-Data cleaning-Feature Extraction-Sentiment Analysis
# Web scraping using BeautifulSoup
# Step 01: Import Libraries
The most important libraries for web scraping and data preprocessing are as follows ;
- Pandas
-	NumPy
-	Request
-	BeautifulSoup
-	Nltk
-	String
# Step 02: Extracting sublinks (Pages) from the main URL
While extracting articles from the URL, we will also get the links of other pages on the main link. This process follows the following steps:
1.	Accessing the link using get() function from request library
2.	Parse the data
3.	Then find all the href tags and save them in a list using loop.
# Step 03: Extracting and Storing Data 
1.	The extracted URLs are now accessed one by one in a loop using BeautifulSoup. 
2.	After accessing the URLs, get_text() function will extract articles from each URL.
3.	Store the data in a DataFrame using Pandas.
# Step 04: Data Preprocessing
- #Text Cleaning:
For a data to be processed in any Machine Learning Model, it must have cleaned the
- extra spaces
- punctuation marks
- characters
- word lemmatization
- stop words

- Lower case all text using lower()
# Step 05: Feature Extraction
Feature extraction refers to the process of transforming raw data into numerical features that can be processed while preserving the information in the original data set. It yields better results than applying machine learning directly to the raw data.
For this purpose, we will tokenize the text using TF-IDF vectorizer and then fit.transform() function will be used on tokenized data.
Now we can apply get_feature_names() to get all the features of each article. These new reduced set of features should then be able to summarize most of the information contained in the original set of features.
For further clarity, we have find the frequency distribution of each feature.

# Step 06: Sentiment Analysis 
Sentiment analysis is basically the process of determining the attitude or the emotion of the writer, i.e., whether it is positive or negative or neutral.
The sentiment function of textblob returns two properties, polarity, and subjectivity.
Polarity is float which lies in the range of [-1,1] where 1 means positive statement and -1 means a negative statement. Subjective sentences generally refer to personal opinion, emotion or judgment whereas objective refers to factual information. Subjectivity is also a float which lies in the range of [0,1].

For our scrapped articles, we have values for negative, positive, neutral and compound sentiments. Each value defines the scope of each article.

