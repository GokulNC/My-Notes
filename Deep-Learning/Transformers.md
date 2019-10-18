## Quick summary of Transformers and its variants

### Vanilla
- Task: Machine Translation
- Encoder & Decoder Stacks. (Multiple-heads)
- Each encoder: Embeddings->Self-Attention->FC->Layer_Norm
- Each decoder:
  - Shares a few weight matrices from the output of encoder.
  - Progressive Masked Self-attention-> Encode-Decode-like Attention -> FC
  - Auto-regressive?
  
### BERT
- Only the encoder
- Masks 15% of tokens randomly
- Tasks: Masked token prediction and `ifNextSentence`
- Embeddings: Word_Piece Emb (Learnable) + Position Embs + Segment Embs
- Has special tokens like [CLS], etc.

### Transformer-XL
- Solves fixed sequence-length problems using recurrence
- All hidden states now is a function of current input and prev-state (RNN-like)
- Hence captures long-term dependencies

### ELMo
- 2-layer BiLSTM

### E-ELMo (Entity-aware)
- Input: Character convolution of each character position
- Predicts multiple targets

### ULMFiT
- Universal Language Modeling Fine-Tuning
- Pre-trained on any general-domain corpus
- Fine-tuning: Discriminative and uses Slanted Triangular LR
- Classifier: Gradual Unfreezing of layers

### OpenAI GPT & GPT-2
- Only the decoder
- Task: Next word prediction
- Massive in size, that's it.
- Byte Pair Encoding
