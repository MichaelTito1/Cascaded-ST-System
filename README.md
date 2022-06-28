# Cascaded-ST-System
Cascaded ST System using Pytorch and Huggingface python libraries. 

This work contains the following general contributions:
1. building a multi-modal, attention-based semi-supervised punctuation prediction model that fuses the acoustic and lexical information to predict punctuation.
2. evaluating the performance of the cascaded ST system with and without disfluency removal and punctuation prediction.

# Model Architecture
## Punctuation prediction model
![alt text](https://github.com/MichaelTito1/Cascaded-ST-System/blob/main/presentation%20images/fusion.JPG?raw=true)

## Cascaded ST pipeline
![alt text](https://github.com/MichaelTito1/Cascaded-ST-System/blob/main/presentation%20images/model%20illustration.png?raw=true)

# Results

Class | Count | Percentage
--- | --- | ---
No punctuation | 5,216,171 | 93.29
Comma (,) | 321,102 | 5.74
Full stop (.) | 45,927 | 0.82
Question mark (?) | 8,240 | 0.15
