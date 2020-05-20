# Analyse de sentiments 

Les réseaux sociaux c'est une puissante source de communication entre les gens pour partager leurs sentiments sous la forme d'opinion et de points de vue sur n'importe quel sujet ou article, ce qui entraîne une énorme quantité d'informations non structurées. Pour analyser ces sentiments, diverses approches d'apprentissage automatique et basées sur le traitement du langage naturel ont été utilisées dans le passé. Cependant, les méthodes d'apprentissage profond deviennent très populaires en raison de leurs performances élevées ces derniers temps j'utilise colab notebook.

## DataSet 
 

 > Télécharger depuis Kaggel.com
 
## Model | Keras
 
 J'ai utilise le model Sequential avec Embedding et LSTM voici l'architecture du model 
 
 ```
 model = Sequential()
model.add(Embedding(max_fatures, embed_dim,input_length = X.shape[1]))
model.add(SpatialDropout1D(0.4))
model.add(LSTM(lstm_out, dropout=0.2, recurrent_dropout=0.2))
model.add(Dense(2,activation='softmax'))
model.compile(optimizer = 'adam',loss = 'binary_crossentropy', metrics=['accuracy'])
print(model.summary())

_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
embedding_12 (Embedding)     (None, 28, 128)           256000    
_________________________________________________________________
spatial_dropout1d_8 (Spatial (None, 28, 128)           0         
_________________________________________________________________
lstm_12 (LSTM)               (None, 196)               254800    
_________________________________________________________________
dense_12 (Dense)             (None, 2)                 394       
=================================================================
Total params: 511,194
Trainable params: 511,194
Non-trainable params: 0
_________________________________________________________________
 ```
 
 ## Inspirations
 
 > https://keras.io
 > https://towardsdatascience.com/deep-learning-for-sentiment-analysis-7da8006bf6c1
 > https://towardsdatascience.com/sentiment-analysis-for-text-with-deep-learning-2f0a0c6472b5
 > https://academy.dataiku.com/latest/tutorial/machine-learning/deep-learning-text.html

