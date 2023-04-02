# Text-similarity-classification
Given a  dataset of consisting of Text-Reason pairs along with labels consisting 1s and 0s. 1s denote the Text-Reason pair are similar and 0 denotes that Text-Reason pair are dissimilar.

Using BERT pre-trained models and fine tuning on the dataset to predict the labels for the evaluation file.

Assignment_code2 file uses sentence-transformer library with model- ‘bert-base-nli-mean-tokens’ to predict semantic similarity. This library actually uses Hugging Face transformers.

Assignment_code3 file has two cases, case 1 uses ‘bert-base-uncased’ model and fine-tuned it using two Natural language inference datasets i.e. - Stanford Natural Language Inference (SNLI) and Multi-Genre NLI (MNLI).It is fine-tuned it using multiple negatives ranking (MNR) loss. 
In case2- using the same model- ‘bert-base-uncased’ and training it on NLI datasets, I have also fine-tuned the model with the training data- i.e. Dataset1.xlsx.
