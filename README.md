# Music-Generation
Generate Music Through RNN -
One of the intriguing uses of deep learning is the creation of music. Since music is composed of sequential data, it can be modelled using a recurrent neural network or another sequential machine learning model.

### Requirements
This programme was created in Python 3 and needs the Keras deep learning package (https://keras.io).

### Description
* Three LSTM layers, each with 256 units.
* Three dropout layers, each with a probability of 0.2.
* One layer of embedding on top of the LSTM to embed each character as a dense neuron.
* To create long-term dependencies in each and every character, set stateful=True in the LSTM. Nottingham Music Database, dataset

**Model Detail**
```markdown
Layer (type)                 Output Shape              Param #   
=================================================================
embedding_1 (Embedding)      (16, 64, 512)             44032     
_________________________________________________________________
lstm_1 (LSTM)                (16, 64, 256)             787456    
_________________________________________________________________
dropout_1 (Dropout)          (16, 64, 256)             0         
_________________________________________________________________
lstm_2 (LSTM)                (16, 64, 256)             525312    
_________________________________________________________________
dropout_2 (Dropout)          (16, 64, 256)             0         
_________________________________________________________________
lstm_3 (LSTM)                (16, 64, 256)             525312    
_________________________________________________________________
dropout_3 (Dropout)          (16, 64, 256)             0         
_________________________________________________________________
time_distributed_1 (TimeDist (16, 64, 86)              22102     
_________________________________________________________________
activation_1 (Activation)    (16, 64, 86)              0         
=================================================================
Total params: 1,904,214
Trainable params: 1,904,214
Non-trainable params: 0
_________________________________________________________________
```
A simplified type of musical notation is ABC notation. Basic notation uses the letters A through G to represent the given notes, with other features such as sharps, flats, note lengths, keys, and ornamentation being utilised to give them additional meaning.
Visit https://en.wikipedia.org/wiki/ABC notation to learn more about char ABC Notation.

A Char-RNN-based generator, which learns about the pattern of characters that appear in the char ABC notation in music, is used in the text creation process.
Once it has been trained, it will be able to produce music using the abc notation, which appears to be a novel way for the network to make music.






