AES Side-Channel Attack Using Neural Networks
Overview
This project implements a neural network-based side-channel attack on AES encryption.
A Multi-Layer Perceptron (MLP) is trained on simulated power traces to recover
the secret AES key byte using the Hamming weight leakage model.

This implementation was developed as part of the M542 Cryptology module at
Gisma University of Applied Sciences, March 2026.

How It Works
Simulates 5,000 power traces during AES SubBytes operation
Each trace is linked to the Hamming weight of the S-Box output
A neural network is trained on 4,000 traces and tested on 1,000
A key recovery attack is performed over all 256 possible key candidates
The correct key byte is successfully identified as Rank 1
Results
Test Accuracy: 55.90%
True Key: 0x2B
Key Recovery: SUCCESS
Correct key ranked #1 out of 256 candidates
Requirements
Python 3.x
numpy
scikit-learn
Installation
pip install numpy scikit-learn

Usage
python aes_sidechannel_attack.py

References
Kocher, P., Jaffe, J. and Jun, B., 1999. Differential Power Analysis.
Mangard, S., Oswald, E. and Popp, T., 2007. Power Analysis Attacks.
Lerman, L., Bontempi, G. and Markowitch, O., 2018. Power analysis attack: An approach based on machine learning.
