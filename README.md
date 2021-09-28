# Toxic_text_classification
 Here I  have performed text classification on the Kaggle Toxic Comments Challenge data. After EDA and data cleaning, I  used Glove word embeddings and a Bi-LSTM followed by a fully connected layer for the model. After 5 epochs of training I obtained a validation AUC of 0.984.  The different steps taken are as follows:
 
 * Removed punctuations and performed EDA to understand the  nature of the problem as a classification problem with multiple posssible labels for any particular comment. Plotted the types and relative proprotions of different kinds of toxicity. 
 * Created prepare_data function for cleaning data. The steps involved being removing newline characters, converting to lower case, removing stopwords and lemmatizing.
 * Performed train, test split and uses Keras Tokenizer to tokenize the comment texts. The tokenized texts  where appropriately padded to make them of uniform length. 
 * Used downloaded Glove embedding file to create the  embedding layer of the model.
 * The final model was chosen to be a bi-LSTM followed by a fully connected layer with sigmoid activation. The latter was chosen to take care of multi-label classification nature of the problem. 
 * Model was trained and validated using AUC as mteric and the Adam optimizer.
 
 
