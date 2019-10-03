# 20_News_group_Data_Advance_Text_Analytics

### Problem Statement
“20 Newsgroup” dataset contains documents which are mapped to 20 different topics. The task is to train a classifier which is able to map new incoming documents to their topic.

### Dataset Description
This is preloaded dataset available in scikit-learn library in well-defined train and test sets. So, we directly loaded our data using scikit library. 
 
#### Number of Documents 
- Train Data: 11314 
- Test Data: 7532 
#### Distinct Number of Document Classes: 20 
alt.atheism 
comp.graphics 
comp.os.ms-windows.misc 
comp.sys.ibm.pc.hardware 
comp.sys.mac.hardware 
comp.windows.x 
misc.forsale 
rec.autos 
rec.motorcycles 
rec.sport.baseball 
rec.sport.hockey 
sci.crypt 
sci.electronics 
sci.med 
sci.space 
soc.religion.christian 
talk.politics.guns 
talk.politics.mideast 
talk.politics.misc 
talk.religion.misc

### Data Cleaning and Preprocessing

After a good understanding of dataset, we moved on to cleaning and preprocessing text data and get it in a good shape which can be passed to models. 
We performed following data cleaning and data preprocessing operations: 
 
- Filtering only English documents and skipping documents of other languages
- Replacing multiple spaces with single space
- Lowering the case of each character
- Lemmatizing the text
- Removing the stop words 
- Filtering sentences of length less than 3 
 
 ### Model Building and Evaluation
After getting clean, tokenized and transformed data, next step is to build ML models. We tried following models and evaluated their performance on train and test dataset. 
 
- Naïve Bayes 
- SVM 
- XGB 
We tried above mentioned three models for each choice of data transformation techniques and evaluated their performance of train and test dataset. Following are the results: 
![model_results](https://github.com/singhankit16/20_News_group_Data_Advance_Text_Analytics/blob/master/model_results.PNG)

### Challenges
- Header and Footer caused very messy form of data
- Removing them from documents helped to achieve better accuracy
- Initially we didn’t remove stop words while vectorizing data, which was causing lower accuracy
- Removing stop words helped to achieve better results
- Computation on XGB classifier was a challenge in local machine, so we use Google Colab to run XGB model which gave us better computation resources and throughput 
