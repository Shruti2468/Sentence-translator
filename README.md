# Sentence-translator





This project focuses on developing a neural machine translation system for translating English text into Hindi. Leveraging the capabilities of transformer-based models, the project employs the Helsinki-NLP/opus-mt-en-hi model, pre-trained on the English-Hindi translation dataset `cfilt/iitb-english-hindi`, to fine-tune a translation model tailored to specific requirements.

The project begins with the preprocessing of the dataset, including tokenization of input and output text sequences using the AutoTokenizer from the Hugging Face Transformers library. The input data is truncated to a maximum length of 128 tokens, and similarly, the target sequences are tokenized and prepared for model training.

The model is built using the TFAutoModelForSeq2SeqLM class, a TensorFlow implementation of a sequence-to-sequence transformer model. Key training parameters such as batch size, learning rate, weight decay, and the number of epochs are defined to optimize the model's performance. The training process is supported by data collators that handle the padding and batching of sequences.

After training, the model is saved for future use. For inference, the trained model and tokenizer are loaded to perform translation on new input texts. The output is decoded from token IDs to human-readable text, demonstrating the model's effectiveness in translating English sentences into Hindi.

This project highlights the application of state-of-the-art transformer models for language translation, providing a practical solution for multilingual communication and localization tasks.

