# Sentiment-Analysis-e-commerce
During my internship with the Microsoft Technology Associate (MTA) Program, I made this as my Major Project.

## Gathering Data:
I was provided the data by the intrnship mentors. It was from an E-commerce website and all the reviews were for female clothing items.

## Data Cleaning :
The Columns I had in the data were : 
* **Age** : Age of the Reviewer
* **Title** : Title they gave to their review
* **Review_Text** : Review description 
* **Recommended_IND** : 1/0 , It's whether they will recommend the same item to someone else or not?.
* **Pos_Feedback_Count** : It's the number of positive reviews given to different items by a certain buyer.
* **Division_Name , Department_Name, Class_name** : All these Columns differentiate between different items and give us the category to which they belong.
* **Rating_Class** : Good/Bad. A column that I added which was to be predicted.

I deleted all the entries with **null** values of *Review_Text* as our analysis totally depends on that.

##### Text Pre-Processing :
  The next step was to do text pre-processing. So I followed the following steps :
  1. **Lowercasing** : As same words might be differentiated because of the formating that they are in.(UpperCase/LowerCase).
  1. **Removing Punctuation** : As Punctuation have no role in Sentiment Analysis. And they also add complexities to the implementation of the model.
  1. **Removing Stop Words** : Stopwords are the English words which does not add much meaning to a sentence. They can safely be ignored without sacrificing the meaning of the sentence. For example, the words like the, he, have etc.
  1. **Removing Commonly Occuring words** : As they wont help us in making the model any better. Also it will decrease the processing to be done by the model. It is quite helpful while working with huge datasets.
  1. **Removing Rarely Occuring words** : As they wont help us as it is very rare if the users will use those words in future.
  1. **Tokenization** : It is breaking the sentence into small tokens making the implementation of model very easy.
  1. **Lemmatization** : It usually refers to doing things properly with the use of a vocabulary and morphological analysis of words, normally aiming to remove inflectional endings only and to return the base or dictionary form of a word, which is known as the lemma .
  1. **Removing Words without Meaning** : Words like "Soooooo", "veryyyy", etc, were to be removed as even a change in a single "o" can make it a new word for the model and thus they have gotta be removed or spell-checked. Spell-checking is very resource intensive process and takes a lot of time. So I chose to remove those words.

## Exploratory Data Analysis :

![Words Used in Positive Reviews](https://github.com/Siddharthm10/Sentiment-Analysis-e-commerce/blob/master/Images/Positive.png)



![Words Used in Negative Reviews](https://github.com/Siddharthm10/Sentiment-Analysis-e-commerce/blob/master/Images/Negative.png)
