# NLP on Agatha Christie Novels

## Executive Summary:

Some fans and experts believe that Agatha Christie had undiagnosed dementia in her later years. A paper published in 2009 looked at 14 of Agatha Christie's novels and found an increase in repeated phrase types, increase in indefinite word usage, and decrease in unique word types in her works as she aged.  
The goal of this project is to first replicate the findings of the paper using all 66 of her detective novels instead of 14, and to dive deeper into analysis of her works.
Then, using the features of her texts that I engineer using NLP techniques, I will make a model that predicts the age at which she wrote a piece of text.

## Data:
Agatha Christie's novels were downloaded in the ePUB format from the internet archive. They were converted to TXT files using the program Calibre.  
The data was cleaned by removing forewords and introductions from the beginning of the novels and removing the advertisements at the end of the book. Punctuation and capitalization was also removed.

Parts of speech was tagged with NLTK and sentiment analysis on the text was also performed.

I did not include any of her short stories, and also excluded her thriller novel written in her late 70s.  
The authors of the original paper removed the book Passenger to Frankfurt, identifying it as an outlier because 

> "Passenger to Frankfurt has the largest vocabulary of all the works we analyzed ... it is a thriller, not a detective mystery, conceived, written, and researched in her early to mid 70s... it draws on books by political thinkers that she requested of her publishers ... Much of the vocabulary in Passenger to Frankfurt comes from her reliance on these sources."

I find this outlier extremely interesting because it demonstrates that, though Agatha Christie's vocabulary recall may have declined over the years, her ability to recognize and use a large vocabulary in her writing remained intact in her later years. 

## Findings:
I was able to replicate the paper's findings; usage of unique words decreased with age while frequency of repeated trigrams and indefinite words increased as well.  
In addition, I found that increase of usage of other vague words, ie. stuff, very, and lot, were correlated with age. With these increases in indefinite and vague words, I found a significant decrease in unique adjectives in her text as well. 

Flesch reading ease score, a measure of how easy a piece of text is to read and understand, was measured and I found that the Flesch reading ease was correlated with her age. Her books are known to be written in plain English and easy to read, but they do get "easier" as she aged.

I fit different regression models to the features I described above and found that the Lasso Regression model gave me the best training R^2 score of 0.72. This performed much better than the baseline, which predicted the average year of 1941 and had an R^2 score of 0. 

## Conclusions:
This model could be improved, but this proof of concept shows that a model could be made to monitor cognitive decline through writing. 

