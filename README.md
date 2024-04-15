# Arabic Text Modration 
## https://arxiv.org/pdf/2201.06723.pdf


## Fine-Grained Hate Speech Detection on Arabic Twitter
- OFF or NOT_OFF: offensive language is any text that contains Vulgar or impolite words


- HS or NOT_HS: Hate speech is defined as a kind of offensive language but is more nuanced that targets a person or a group of people based on common characteristics such as ethnicity, nationality, religion, politics, disability, social class, gender, and gender.



Hate Speech types in our dataset are:

HS1 (race/ethnicity/nationality).
HS2 (religion/belief)
HS3 (ideology)
HS4 (disability/disease)
HS5 (social class)
HS6 (gender)



The corpus contains ~13K tweets in total: 35% are offensive and 11% are hate speech. Vulgar and violent tweets represent 1.5% and 0.7% of the whole corpus.

Percentages of offensive language and hate speech in the corpus are the highest among other corpora without using pre-specified keywords or selecting a specific domain.




We will have 3 shared subtasks:


Subtask A: Detect whether a tweet is offensive or not.

Labels for this task are: OFF (Offensive) or NOT_OFF (Not Offensive)

Example: الله يلعنه على هالسؤال (May God curse him for this question! )



Subtask B: Detect whether a tweet has hate speech or not.

Labels are: HS (Hate Speech) or NOT_HS (Not Hate Speech).

Subtask B is more challenging than Subtask A as 11% only of the tweets are labeled as hate speech.

Example: أنتم شعب متخلف (You are a retarded people)



## Dataset
Download training data from: https://alt.qcri.org/resources/OSACT2022/OSACT2022-sharedTask-train.txt

Download development data from: https://alt.qcri.org/resources/OSACT2022/OSACT2022-sharedTask-dev.txt

## Preprocessing 
we clean data set from any emotions and any labels like HS/NotHs tags and other tags 
##
We convert HS/Not HS to 0/1 number in dataset labels
##
We convert OFF/Not OFF tags to 0/1 number in dataset labels 
##
you can find the Preprocessing File in 
## Model 
we used MaraBert and is Deep Bidirectional Transofrmers For Arabic  from HuggingFace 

> https://huggingface.co/UBC-NLP/MARBERT
**MARBERT** is one of three models described in our **ACL 2021 paper** 
![Arabic-BERT-model-architecture](https://user-images.githubusercontent.com/95087747/168382695-77575676-ac0b-405b-abdd-84cc59dfcf32.png)
## Preformance Evaluation 
### Evaluate Task A
![FinalOFF](https://user-images.githubusercontent.com/95087747/168401678-ad7ada22-f1bc-4cc6-8263-ff4c2ffe748d.PNG)

F1-score of Task A 88%

### Evaluate Task B 
![FinalHS](https://user-images.githubusercontent.com/95087747/168401713-cbbdcd3a-a1fe-45f2-a6e7-a7f2d722faa1.PNG)

F1-score of Task B 92%
