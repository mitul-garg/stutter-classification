# Stutter Classification

Throughout this project, an approach to identify and classify speech dysfluencies is being formed. The approach used describes the use of **MFCC audio features** amalgamated with **Decision Tree** and **K-Nearest Neighbors** for accomplishing this task. After working on several approaches, it can be concluded that the [SEP-28k Dataset](https://www.kaggle.com/datasets/bschuss02/sep28k "SEP-28k Dataset") can be successfully used for classifying Speech Dysfluencies separately into Word Repetition, Sound Repetition and Prolongation. It was also discovered that not all rows are useful from the [SEP-28k Dataset](https://www.kaggle.com/datasets/bschuss02/sep28k "SEP-28k Dataset") for every dysfluency and thus the appropriate amount of rows/data required were pointed out successfully and uploaded to Kaggle : [SEP-28k MFCC](https://www.kaggle.com/datasets/mitulgargsam/sep28kmfcc "SEP-28k MFCC").

## Results :

After using various methods to train the models, the following accuracies were achieved :

| SoundRep                        | WordRep                         | Prolongation                     |
| ------------------------------- | ------------------------------- | -------------------------------- |
| **89.53 - Decision Tree** | **86.11 - Decision Tree** | **66.83 - K-Nearest Neighbors** |

## Approach Used :

After using various approaches including [Sampling](https://machinelearningmastery.com/data-sampling-methods-for-imbalanced-classification/ "Sampling Techniques") techniques, the following steps need to be followed for training Stutter Recognition and Detection systems using SEP-28k Dataset :

* Remove empty audio files and their corresponding entires from the dataset
* Remove rows with Poor Audio Quality, Background Music and which are in general difficult to understand
* Remove other rows with even one clinician labelling it as some other dysfluency
* Considering labels 1, 2 and 3 as 1, so as to convert the multi-class classification into binary classification
* Input files to be split into small clips of 3 seconds each, then running model on each clip and analysing the percentage of clips with a particular dysfluency

## Features and Benefits :

* Detection and classification of speech dysfluencies like Word Repetitions, Sound Repetitions and Prolongations
* Preprocessed dataset along with the corresponding MFCC features is uploaded to Kaggle : [SEP-28k MFCC](https://www.kaggle.com/datasets/mitulgargsam/sep28kmfcc "SEP-28k MFCC"). Hence, there is no need to preprocess the dataset while using it.
* Severity of stuttering is to be judged on the basis of the number of clips with stuttering instead of the number of clinicians labelling the clip as a particular dysfluency
* Anyone can use the models trained for classifying speech dysfluencies.
* The models use Binary Classification, which makes it easy to understand for anyone that the input has a particular dysfluency or not.
