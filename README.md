# Removing-noise-using-CNN


Gaussian Noise:
mean=0 and Std=0.5

Autoencoder:

Accuracy achieved - 81.12%
Loss              - 0.149

Model: "autoencoder"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
input_6 (InputLayer)         (None, 28, 28, 1)         0         
_________________________________________________________________
conv2d_24 (Conv2D)           (None, 14, 14, 16)        160       
_________________________________________________________________
conv2d_25 (Conv2D)           (None, 7, 7, 32)          4640      
_________________________________________________________________
flatten_22 (Flatten)         (None, 1568)              0         
_________________________________________________________________
dense_44 (Dense)             (None, 16)                25104     
_________________________________________________________________
dense_45 (Dense)             (None, 1568)              26656     
_________________________________________________________________
reshape_12 (Reshape)         (None, 7, 7, 32)          0         
_________________________________________________________________
conv2d_transpose_31 (Conv2DT (None, 14, 14, 32)        9248      
_________________________________________________________________
conv2d_transpose_32 (Conv2DT (None, 28, 28, 16)        4624      
_________________________________________________________________
conv2d_transpose_33 (Conv2DT (None, 28, 28, 1)         145       
_________________________________________________________________
decoder_output (Activation)  (None, 28, 28, 1)         0         
=================================================================
Total params: 70,577
Trainable params: 70,577
Non-trainable params: 0





Classifier:
Accuracy achieved - 95.15%
Loss              - 0.1881


Model: "classifier"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
autoencoder (InputLayer)     (None, 28, 28, 1)         0         
_________________________________________________________________
conv2d_18 (Conv2D)           (None, 14, 14, 16)        160       
_________________________________________________________________
conv2d_19 (Conv2D)           (None, 7, 7, 32)          4640      
_________________________________________________________________
flatten_9 (Flatten)          (None, 1568)              0         
_________________________________________________________________
dense_14 (Dense)             (None, 16)                25104     
_________________________________________________________________
dense_15 (Dense)             (None, 1568)              26656     
_________________________________________________________________
reshape_9 (Reshape)          (None, 7, 7, 32)          0         
_________________________________________________________________
conv2d_transpose_25 (Conv2DT (None, 14, 14, 32)        9248      
_________________________________________________________________
conv2d_transpose_26 (Conv2DT (None, 28, 28, 16)        4624      
_________________________________________________________________
conv2d_transpose_27 (Conv2DT (None, 28, 28, 1)         145       
_________________________________________________________________
decoder_output (Activation)  (None, 28, 28, 1)         0         
_________________________________________________________________
flatten_19 (Flatten)         (None, 784)               0         
_________________________________________________________________
dense_37 (Dense)             (None, 512)               401920    
_________________________________________________________________
dropout_9 (Dropout)          (None, 512)               0         
_________________________________________________________________
dense_38 (Dense)             (None, 512)               262656    
_________________________________________________________________
dropout_10 (Dropout)         (None, 512)               0         
_________________________________________________________________
dense_39 (Dense)             (None, 10)                5130      
=================================================================
Total params: 740,283
Trainable params: 669,706
Non-trainable params: 70,577


