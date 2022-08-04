# Natural Language Processing concepts. Examples would be added here with some explanation.

## Bayes based Auto-Correct
In this notebook a wrongly spelled word is corrected based on the probabability of its one edit and two edit options in a corpus of the text. In this model, the context is not considered and is a very simple, but useful before looking into attention based models that calculate the probability of each word based on the context (other words in the text).

## Parts-of-speech tagging using Hidden Markov Model (HMM) and Viterbi algorithm
Part of speech tagging has applications in speech recognition, name entitities, information retrieval and so on. The dataset used is one of the most common in the literature and is referenced in the notebook. The same dataset has been the subject of research for tagging using more advanced techniques using LSTM, BERT, and other techniques. HMM model only considers one previous state/tag for predicting the tag of each word, whereas for example LSTM and attention models can look back more and could also be bi-directional. However, at the test dataset, the HMM model with viterbi algorithm results in 95.5% accuracy, compared to 97-98% accuracy of more sophisticated models. 

## Auto-Complete using n-gram language model.
N-gram language models have applications in speech recognition, auto-complete, spelling corrections, and augmentive communication. These models are probabilistic and calculate the probability of a next word in a sequence based on the number of times the word and the previous sequence occur in the training dataset. Although simple to implement, the memory consumption could be large for big datasets. Sequence language models solve this, but here an example of building n-gram models is shown and is applied for auto-completing a sentence (suggesting the next word).

## Word embedding calculations
The basic principle of using NNs to learn word embeddings is described. The notebook gives an example of using CBOW technique to learn word embeddings. The model is trained on Shakespeare's traing set that was used in another example.

## Sentiment prediction using BERT
This shows a simple multi-class classifier for sentiment prediction of tweets. The dataset is not so balanced and is small. There is another dataset on imdb reviews and I will try the same on that.

Dataset: [Data](https://figshare.com/articles/dataset/smile_annotations_final_csv/3187909/2)

## Named Entity Recognition using Keras
A simple model using Keras Sequential API and LSTM layers has been created. The word embedding are trained using an embedding layer and not loaded from a pre-trained model. Improvements could be trying with pre-trained embeddings and using bidirectional LSTM. This was a simple illustration.
During the model building noticed that if the model is not set up carefully it will converge to one single tag for all words. Since the padding tag of 'O' is more abundant that other tags, the model evaluation has be done carefully.

Dataset: [Data](https://www.kaggle.com/datasets/abhinavwalia95/entity-annotated-corpus)

## IMDB sentiment prediction using BERT transformers.
Similar to the previous sentiment analysis with BERT. This time dataset is larger and better. Data is available to load from torchdata and the reference is given in the notebook. The classification is binary this time.

## Starting to use HuggingFace models for complex tasks
I want to show step by step guide on how to use pre-trained HuggingFace models for more complex tasks and train/fine-tune them on new data.
This first notebook is just a simple example of loading a pre-trained question answering model. As a test two questions are asked from the model. In the next step we will show how to find tune the model on a well-known dataset.
Next goal is then to use this model or a similar model to design a question generator. This can be used for example by teachers to design exam questions!
