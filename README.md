# DS4D Project

We will use this space to keep our work on DS4D project. You can take out the relevant files from the `/data` folder and start working in the folder with your name.

# Documentation

This space also houses the strategy we have used to come up with our analysis. The structure of functions, the input arguments and the expected results are defined here. The dataframe structure that we are using is also mentioned in this document.

## Dataframe Example

| id | filename | path | country | network | date | tokenFreq | text |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 1 | file1.txt | /all/gulf/qatar/file1.txt | country | AlJazeera | 20200606 | 3 | Entire text here |
| 2 | file2.txt | /all/gulf/qatar/file2.txt | country | AlJazeera | 20200606 | 5 | Entire text here |

## Key Algorithms

1. Cleaning and Normalization
2. Stemming and Lemmatization / Collocation in python
3. TF-IDF
4. Topic Modeling
5. Subjectivity Analysis

### 1. Cleaning/Normalization Function

Expected Inputs: Raw TXT files for Euro-Atlantic countries, Gulf countries and New Global Media Players.
\
Expected Outputs: Filtered files in a separate folder and a dataframe with file name, path, date, country, broadcasting network, frequency of the word `humanitarian*`, article texts
\
\
Steps for cleaning:

1. Remove the HTML characters: HTML tags like `&apos;`, `&amp;`, `&lt;` etc can be found in the text files. Consider removing them using HTMLParser or regular expressions.
2. Remove URLs. I don't think we need URLs. Let's remove them using regular expressions i.e. `re`.
3. Replace Contractions: The text data might contain apostrophes `'` used for contractions. For example, didn't, couldn't. We should make them did not and could not. Consider making a dictionary and replacing them all at once.
4. Remove Punctuations

*Note:* This is not an exhaustive list.
\
\
For normalization, take a look at this article: https://towardsdatascience.com/text-normalization-7ecc8e084e31

### 2. Stemming and Lemmatization / Co-location in python

Example with explanation: https://towardsdatascience.com/stemming-vs-lemmatization-2daddabcb221
\
\
Expected Inputs: Dataframe with all news article texts in the `text` column
\
Expected Outputs: Cleaned Dataframe (same format)

### 3. TF-IDF

Reference: https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfVectorizer.html
\
Example: https://towardsdatascience.com/natural-language-processing-feature-engineering-using-tf-idf-e8b9d00e7e76
\
\
Expected Inputs: Dataframe with all news article texts in the `text` column
\
Expected Outputs: Visualization for inverse frequencies

### 4. Topic Modeling

Example: https://towardsdatascience.com/end-to-end-topic-modeling-in-python-latent-dirichlet-allocation-lda-35ce4ed6b3e0
\
\
Expected Inputs: Dataframe with all news article texts in the `text` column
\
Expected Outputs: Visualization for prominent topics

### 5. Subjectivity Analysis using TextBlob

Reference: https://textblob.readthedocs.io/en/dev/quickstart.html
\
\
Expected Inputs: Dataframe with all news article texts in the `text` column
\
Expected Outputs: Visualization for subjectivity

## Download link for clean dataframe
https://drive.google.com/file/d/1n8NPQKxFGbcIeFaUVTD0ANkNIazpUkR-/view?usp=sharing
