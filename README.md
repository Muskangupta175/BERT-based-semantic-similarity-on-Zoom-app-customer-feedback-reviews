# Text-similarity-classification
Description:
  Given a  dataset consisting of Text-Reason pairs along with labels consisting 1s and 0s. 1 denotes the Text-Reason pair as similar and 0 denotes that the Text-Reason     pair is dissimilar.
  
  
# Files:
  1.  Evaluation.xlsx - Test data
  2.  Dataset1.xlsx - Dataset consisting of similar text pairs. Dissimilar text pairs are created by randomly inserting few words in between the sentences of similar text pairs.
  3.  Dataset2.xlsx - Dataset consisting of similar text pairs. Dissimilar text pairs are created by randomly deleting few words from the similar pairs.


# Approach:
Cleaned the data for any special characters. With the help of BERT pre-trained models, leveraged from HuggingFace library, converted the sentences into sentence embeddings. By calculating the cosine similarity between the embeddings of each sentence pair, we can calculate the semantic similarity between them. These cosine similarity scores are between 0 and 1, 0 being completely dissimilar pairs and 1 being similar pairs. By analyzing the cosine similarity values of test data, a threshold value is decided to classify the sentence pairs of test data as similar or dissimilar. 

# Code files:

   Assignment_code2 file uses sentence-transformer library with model- ‘bert-base-nli-mean-tokens’ to predict semantic similarity. 

   Assignment_code3 file has two cases,
   Case 1 uses ‘bert-base-uncased’ model and fine-tuned it using two Natural language inference datasets i.e. - Stanford Natural Language Inference (SNLI) and Multi-Genre NLI (MNLI). It is fine-tuned using multiple negatives ranking (MNR) loss. 
   Case2- using the same model- ‘bert-base-uncased’ and training it on NLI datasets, our training data- i.e. Dataset1.xlsx.
