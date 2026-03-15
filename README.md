# M542 Cryptology - AES Side-Channel Attack Using Neural Networks  
**Institution:** Gisma University of Applied Sciences 

**Department:** Computer and Data Sciences

**Module:** M542 Cryptology | Semester: Winter 2026

**Author:** Anandhu Chandran | GitHub: anandhuchandran16-bit

## Project Overview
This project analyses and demonstrates a neural network-based side-channel attack on AES encryption as part of the M542 Cryptology individual project assessment.
The following attack is studied, implemented, and analysed:
AttackTargetLeakage ModelRiskPower Analysis (SCA)AES SubBytesHamming Weight🔴 Critical

## Repository Structure
aes-sidechannel-attack/

├── aes_sidechannel_attack.py             
# Neural network side-channel attack 
implementation
└── README.md

 ## Tools Used
ToolPurposePython 3Main programming languageNumPyTrace simulation and numerical operationsScikit-learn (MLP)Neural network training and key recovery

## How to Reproduce
1. Install dependencies
pip install numpy scikit-learn
2. Run the attack
python aes_sidechannel_attack.py

## Results Summary
MetricValueTotal Traces5,000Training Set4,000Test Set1,000Neural NetworkMLP (128-64 neurons, ReLU)Classification Accuracy55.90%Random Baseline~11%True Key0x2BKey Recovery✅ SUCCESSCorrect Key Rank#1 out of 256Match Score0.9040

## How It Works

Simulates 5,000 power traces during AES SubBytes operation
Each trace is linked to the Hamming weight of the S-Box output
A Multi-Layer Perceptron (MLP) neural network is trained on 4,000 traces
The model is tested on 1,000 unseen traces achieving 55.90% accuracy
A key recovery attack is run over all 256 possible key byte candidates
The correct key byte (0x2B) is successfully ranked #1 out of 256

 ## References

Kocher, P., Jaffe, J. and Jun, B. (1999) Differential Power Analysis — CRYPTO '99
Mangard, S., Oswald, E. and Popp, T. (2007) Power Analysis Attacks: Revealing the Secrets of Smart Cards
Lerman, L., Bontempi, G. and Markowitch, O. (2018) Power analysis attack: An approach based on machine learning
Zaid, G., Bossuet, L., Habrard, A. and Venelli, A. (2020) Methodology for Efficient CNN Architectures in Profiling Attacks
National Institute of Standards and Technology (2001) Advanced Encryption Standard (AES) — FIPS PUB 197


https://github.com/anandhuchandran16-bit/aes-sidechannel-attack

