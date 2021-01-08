# Time-dependen-TV-script-generation_RNN
Use recurrent neural network (embeding layer + LSTM hidden layer + fully connected layer) to train a model which takes previous 5 words as inputs and the 6th word as output. A TV script can be generated with one word as a start. 

## Summayr of the steps: 
- Load data

- Tokenize characters function:
  - dict{char : int}
  - dict{int : char}
  - dict{punctuation symbol : 'discription'}
  
- Preprocess data
  - lower case
  - split text into word list
  - tokenize words in text
  
- Batching into Dataloader
  - Inputs = [1,2,3,4,5] (eg. batch_size = 5)
  - target = [6]: the word after inputs
  
- RNN architecture
  - embeding layer (vocab_size --> embedding_dim)
  - LSTM layer (embedding_dim --> hidden_dim, n_layers)
  - fully connected layer (hidden_dim --> output_size)
  
- Define forward and backward pass

- Set hyperparameters: sequence_length/ batch_size/ num_epoch/ learning rate/ input_size/ output_size/ embeding_dim/ hidden_dim/ n_layers

- Training

- Test: Input one word, generate a paragraph.
