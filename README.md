# Stock Prediction using Time Series Analysis
	Closing Price prediction of Yahoo stocks from 2010 - 2016 using Gated Recurrant Units 

#### DATA
	INPUT_DATA
	date             open      close        low       high                                      
	2010-01-04  16.940001  17.100000  16.879999  17.200001
	2010-01-05  17.219999  17.230000  17.000000  17.230000
	2010-01-06  17.170000  17.170000  17.070000  17.299999
	2010-01-07  16.809999  16.700001  16.570000  16.900000
	2010-01-08  16.680000  16.700001  16.620001  16.760000

	LABEL_DATA
	date			  close
	2010-01-04    17.230000
	2010-01-05    17.170000
	2010-01-06    16.700001
	2010-01-07    16.700001
	2010-01-08    16.740000

#### MODEL
Layer (type)                 Output Shape              Param #   
_________________________________________________________________
gru_1 (GRU)                  (None, 1, 512)            794112    
_________________________________________________________________
dropout_1 (Dropout)          (None, 1, 512)            0         
_________________________________________________________________
gru_2 (GRU)                  (None, 256)               590592    
_________________________________________________________________
dropout_2 (Dropout)          (None, 256)               0         
_________________________________________________________________
dense_1 (Dense)              (None, 1)                 257       
_________________________________________________________________
Total params: 1,384,961
Trainable params: 1,384,961
Non-trainable params: 0
_________________________________________________________________

#### TRAINING
	Final Epoch
	 250/1061 [======>.......................] - ETA: 2s - loss: 6.0397e-04
	1000/1061 [===========================>..] - ETA: 0s - loss: 6.2159e-04
	1061/1061 [==============================] - 1s 886us/step - loss: 6.1279e-04 - val_loss: 6.1362e-04

#### RESULTS
    33% of Data used for Testing 
![alt text](https://github.com/jha-prateek/Stock-Prediction-RNN/blob/master/predicted_test.JPG)
