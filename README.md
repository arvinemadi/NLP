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
