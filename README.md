# Transliterate a word written in English script to Hindi using Seq2Seq Additive Attention Model

To Download the dataset go to the website http://workshop.colips.org/news2018/dataset.html. On the website go to the “NEWS2018 DATASET_04” section, you will find Hindi mentioned. Register to get the download link. From the downloaded dataset use NEWS2018_M-EnHi_trn.xml for the training purposes.

### Reading the Dataset

Parse the XML file by traversing thru the elements and store each elements and its translisteration a list

### Preprocessing the Dataset

Convert the input and output word into a sequence of characters and append <sos> and <eos> at the begining and end of sequence. Vectorise the input and output sequence. 
 The length of the every input and output sequence should be standardised.
  
 ### Encoder-Decoder Attention Model
 
 Set hyperparameters like batch size, no of gru units, embedding dimension of input sequence, total number of training data points.
 
 Set the architecture of encoder, decoder and Attention layer.
  
 Declare the Loss function for classification model(categorical cross-entropy) and optimizer to apply the gradient descent.
  
 Set the folder for storing the model checkpoints. This is where model hyperparamets will be stored.
  
 ### Training and Evaluation of the Model
  
  Define the steps of the training process.
  
  Iterate through the training process for all the data points in batches and epochs.
  
  Take the input from user in a textbox and evaluate the model trained.
  
  Example : 
  1.   word = input('Type your input word: ')
       transliterate(list(word))

  
  Output : 
  
      Type your input word: algorithm
      Predicted transliteration: एल्गोरिथम
      'एल्गोरिथम'
  
  2.   word = input('Type your input word: ')
       transliterate(list(word))

  
  Output : 
  
      Type your input word: abhigyaan
      Predicted transliteration: अभिग्ञान
      'अभिग्ञान'
  
3.     word = input('Type your input word: ')
       transliterate(list(word))

  
  Output : 
  
      Type your input word: namaste
      Predicted transliteration: नमस्ते
      'नमस्ते'
  
  4.   word = input('Type your input word: ')
       transliterate(list(word))

  
  Output : 
  
      Type your input word: nonsense
      Predicted transliteration: नॉनसेंस
      'नॉनसेंस'


### References
 
https://medium.com/analytics-vidhya/neural-machine-translation-using-bahdanau-attention-mechanism-d496c9be30c3
