
# Spam Mail Detection

Spam - whether in the form of emails, messages, etc. - is a nuisance. Thanks to deep learning algorithms, the problem is now well under control. Here I show with a Recurrent Neural Network (RNN) model how fast and uncomplicated a model can be calculated that can distinguish spam from non-spam.


## Data Preprocessing

 - Cleaning the text 
 - changing the text format to lower cases
 - stemming 
 - Lemmatization
 - stopwords
## Vectorization


1. one_hot_encoding
2. Bag_of_words
3. TF_IDF
4. Word_Embeddings

     a . word_2_vec
     b . Glove 
## Built Data loaders

So far, data is processed and prepared as vectorized form. Now, it is turn to build data loaders that will feed the batches of datasets into our model.
To do so,

A custom data loader class was built 3 data loaders were instantiated : for train, validation, and test
## Custom Data Loader

Sequence here means a vectorized list of words in an email. As we prepared 6,000 e-mails, we have 6,000 sequences.
As sequences have different lengths, it is required to pass the length of each sequence into our model not to train our model on dummy numbers ( 0s for padding).

Consequently, we need custom data loaders that return lengths of each sequence along with sequences and labels.

Plus, The data loader should sort the batch by each sequence's length and returns the longest one first in the batch to use torch's pack_padded_sequence() (you will see this function in model code)



Using SVM = Train Accuracy_score = 0.9820877084620135 Test Accuracy_score = 0.921865154379332



![App Screenshot](https://raw.githubusercontent.com/Anil0205/Spam-Mail-Detection/main/Images/2.png)




Using Naive Bayes = Train Accuracy_score = 0.9163063619518221 Test Accuracy_score = 0.8216761184625079



![App Screenshot](https://raw.githubusercontent.com/Anil0205/Spam-Mail-Detection/main/Images/3.png)




Using Logistic Regression = Train Accuracy_score = 0.9879555281037677 Test Accuracy_score = 0.9464398235664776



![App Screenshot](https://raw.githubusercontent.com/Anil0205/Spam-Mail-Detection/main/Images/download.jpeg)


Using Random Forest = Train Accuracy_score = 0.9984558369363805 Test Accuracy_score = 0.926591052299937



![App Screenshot](https://raw.githubusercontent.com/Anil0205/Spam-Mail-Detection/main/Images/5.png)


Using Decision Tree = Train Accuracy_score = 0.9984558369363805 Test Accuracy_score = 0.9117832388153749



![App Screenshot](https://raw.githubusercontent.com/Anil0205/Spam-Mail-Detection/main/Images/6.PNG)


## Complete Code


- [Source](https://github.com/Anil0205/Spam-Mail-Detection/blob/main/sms-spam-ham-classification-using-nlp.ipynb) 
 
 
## Data set

- [Data Set](https://github.com/Anil0205/Spam-Mail-Detection/blob/main/spam.csv)

## Support

For support, email anil.aa0514@gmail.com or join our Slack channel.

