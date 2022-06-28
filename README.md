# Cascaded-ST-System
Cascaded ST System using Pytorch and Huggingface python libraries. 

This work contains the following general contributions:
1. building a multi-modal, attention-based semi-supervised punctuation prediction model that fuses the acoustic and lexical information to predict punctuation.
2. evaluating the performance of the cascaded ST system with and without disfluency removal and punctuation prediction.

# Model Architecture
## Punctuation prediction model
![alt text](https://github.com/MichaelTito1/Cascaded-ST-System/blob/main/presentation%20images/fusion.JPG?raw=true)
architecture & illustration by Sunkara et. al (2021)

## Cascaded ST pipeline
![alt text](https://github.com/MichaelTito1/Cascaded-ST-System/blob/main/presentation%20images/model%20illustration.png?raw=true)

# Results
The evaluation metric for our system is SacreBLEU, which is the most widely used metric in the literature to evaluate the accuracy of the translations. We used SacreBLEU
after applying smoothing and conversion to lowercase. We test four variations of our cascaded ST system: one variation without neither punctuation prediction nor disfluency removal; another one using disfluency removal only; another variation using punctuation prediction only; and the last variation uses both punctuation prediction and disfluency removal. This is to observe the effect that each component has on the overall performance of the system.

Cascaded System's Components (in order) | BLEU score
--- | ---
ASR - Translation | 43.29
ASR - Disfluency removal - Translation | 42.65  
ASR - Punctuation prediction - Translation | 49.72
ASR - Disfluency removal - Punctuation prediction - Translation | 49.81

From the results table, we can see that the addition of punctuation prediction caused a 6-point increase in the BLEU score, which is considered a significant improvement. The availability of both the transcript and its corresponding audio provided the punctuation prediction model with more information to be utilized in producing better punctuation. The addition of punctuation marks to the input sequence to the translation model improved the result since the translation model was originally trained on reference text.
