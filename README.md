# Image-Caption-Generation
1) Image Feature Extraction
(CNN encoder)
Pre-trained CNN
VGG16, InceptionV3, ResNet
2) Text Processing
Captions:
Lowercase
Tokenized words
Vocabulary dictionary (word → integer)
Add tokens:
<start> (begin)
<end> (end)
All captions → padded integer sequences
3) Sequence Modeling
(LSTM decoder)
Generates text (word by word)
Inputs:
Image features
Previous words
Output:
Predict next word
4) Merging CNN and LSTM
(Injecting image features into LSTM)
(i) CNN feature vector → LSTM
CNN feature vector → Dense layer → initial LSTM input
LSTM generates captions sequentially
(ii) Encoder–Decoder style
CNN → Image encoder
LSTM → Decoder → Text generation
5) Model Training
Real previous word is fed into LSTM (instead of predicted word)
Loss function: Categorical cross-entropy
Optimizer: Adam
