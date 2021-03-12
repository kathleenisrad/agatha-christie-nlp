# NLP on Agatha Christie Novels

## Executive Summary:

Some fans and experts believe that Agatha Christie had undiagnosed dementia in her later years. A paper published in 2009 looked at 14 of Agatha Christie's novels and found an increase in repeated phrase types, increase in indefinite word usage, and decrease in unique word types in her works as she aged.  
The goal of this project is to first replicate the findings of the paper using all 66 of her detective novels instead of 14, and to dive deeper into analysis of her works.
Then, using the features of her texts that I engineer using NLP techniques, I will make a model that predicts the age at which she wrote a piece of text.

## Data:
Agatha Christie's novels were downloaded in the ePUB format from the internet archive. They were converted to TXT files using the program Calibre.  

## Findings:
I was able to replicate the paper's findings.

I did not include any of her short stories, and also excluded her thriller novel written in her late 70s.  
The authors of the original paper removed the book Passenger to Frankfurt, identifying it as an outlier because 

> "Passenger to Frankfurt has the largest vocabulary of all the works we analyzed ... it is a thriller, not a detective mystery, conceived, written, and researched in her early to mid 70s... it draws on books by political thinkers that she requested of her publishers ... Much of the vocabulary in Passenger to Frankfurt comes from her reliance on these sources."

I find this outlier extremely interesting because it demonstrates that, though Agatha Christie's vocabulary recall may have declined over the years, her ability to recognize and use a large vocabulary in her writing remained intact in her later years. 
