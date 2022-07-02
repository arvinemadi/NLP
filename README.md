# Natural Language Processing concepts. Examples would be added here with some explanation.

## Bayes based Auto-Correct
In this notebook a wrongly spelled word is corrected based on the probabability of its one edit and two edit options in a corpus of the text. In this model, the context is not considered and is a very simple, but useful before looking into attention based models that calculate the probability of each word based on the context (other words in the text).

## Parts-of-speech tagging using Hidden Markov Model (HMM) and Viterbi algorithm
Part of speech tagging has applications in speech recognition, name entitities, information retrieval and so on. The dataset used is one of the most common in the literature and is referenced in the notebook. The same dataset has been the subject of research for tagging using more advanced techniques using LSTM, BERT, and other techniques. HMM model only considers one previous state/tag for predicting the tag of each word, whereas for example LSTM and attention models can look back more and could also be bi-directional. However, at the test dataset, the HMM model with viterbi algorithm results in 95.5% accuracy, compared to 97-98% accuracy of more sophisticated models. 
