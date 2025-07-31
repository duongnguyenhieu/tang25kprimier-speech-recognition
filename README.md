# tang25kprimier-speech-recognition
The system was designed so as to recognize the digit (1 or 0) being spoken into the microphone of laptop then transferred into FPGA(tang25kprimier) over UART.

Frontend (MATLAB) :
The front end is built into matlab due to the ease of doing DSP on it using builtin functions for training and obtaining a mean signal and the other for real time operation



Backend (Tang primier 25k) :
Due to the lack of ADC in Tang primier 25k I'm transmitting the data from the computer’s microphone using USB to TTL module over the uart protocol, the received data of length (1000) samples are compared then with the saved vectors from the training with matlab, the euclidean distances are calculated and the vector with more probability to be the right one is given a bigger weight, weights are then compared then displaying the final results on 2 LEDs.
