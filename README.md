# Reviews sentiment analysis

The initial dataset consists of 190,000 reviews on Russian (about 180,000) and Kazakh (10,000 reviews) collected from popular online store.

## Results

### **Classical models**

#### without lemmatization



|                     |  tf-idf  |       | bag of words |       |
|:-------------------:|:--------:|:-----:|:------------:|:-----:|
|                     | Accuracy |   F1  |   Accuracy   |   F1  |
| Logistic regression |   0.693  | 0.684 |     0.689    | 0.680 |
|         SVM         |   0.694  | 0.683 |     0.680    | 0.660 |
|    Random Forest    |   0.592  | 0.491 |     0.599    | 0.512 |
|    MultinomialNB    |   0.681  | 0.675 |     0.671    | 0.663 |


#### with lemmatization

|                     |  tf-idf  |       | bag of words |       |
|:-------------------:|:--------:|:-----:|:------------:|:-----:|
|                     | Accuracy |   F1  |   Accuracy   |   F1  |
| Logistic regression |   0.685  | 0.677 |     0.688    | 0.677 |
|         SVM         |   0.691  | 0.681 |     0.676    | 0.658 |
|    Random Forest    |   0.588  | 0.505 |     0.610    | 0.547 |
|    MultinomialNB    |   0.674  | 0.671 |     0.660    | 0.655 |


### **CNN and RNN architectures**



|                 | without pre-trained embeddings |       | with pre-trained embeddings |       |
|-----------------|--------------------------------|-------|-----------------------------|-------|
|                 | Accuracy                       | F1    | Accuracy                    | F1    |
| CNN(MaxPooling) | 0.643                          | 0.625 | 0.658                       | 0.632 |
| CNN(AvgPooling) | 0.649                          | 0.636 | 0.655                       | 0.655 |
| RNN             | 0.368                          | 0.182 | 0.365                       | 0.217 |
| GRU             | 0.548                          | 0.516 | 0.561                       | 0.545 |



