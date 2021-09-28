# Toxic_text_classification
 Here I  have performed text classification on the Kaggle Toxic Comments Challenge data. After EDA and data cleaning, I  used Glove word embeddings and a Bi-LSTM followed by a fully connected layer for the model. After 5 epochs of training I obtained a validation AUC of 0.984.  The different steps taken are as follows:
 
 * Removed punctuations and performed EDA to understand the  nature of the problem as a classification problem with multiple possible labels for any particular comment. Plotted the types and relative proportions of different kinds of toxicity. 
 * Created prepare_data function for cleaning data. The steps involved being removing newline characters, converting to lower case, removing stopwords and lemmatizing.
 * Performed train, test split and used Keras Tokenizer to tokenize the comment texts. The tokenized texts  where appropriately padded to make them of uniform length. 
 * Used downloaded Glove file to create the  embedding layer of the model.
 * The final model was chosen to be a bi-LSTM followed by a fully connected layer with sigmoid activation. The latter was chosen to take care of multi-label classification nature of the problem. Droputs were added for regularization. 
 * Model was trained and validated using AUC as metric and the Adam optimizer.
 
 
