# Text_Summarizer
🚀 My Awesome Summarizer
📜 Overview
This project fine-tunes a BART sequence-to-sequence model for text summarization using the Hugging Face transformers library.
It covers the full ML lifecycle:

Data preparation & tokenization

Model training and evaluation

Saving & pushing the model + tokenizer to the Hugging Face Hub

Loading the model for inference and generating summaries

✅ Model type: BartForConditionalGeneration
✅ Framework: PyTorch with Hugging Face Transformers
⚙️ Usage
See the (./summary.py) script in this repo for an example.

It:
- Loads the tokenizer & model from Hugging Face Hub
- Runs summarization on a sample text
- Prints the summary to the console

⚠️ Notes & limitations
The model was trained on relatively short input-target pairs. As a result, it sometimes generates summaries that partially reproduce the input (more extractive than abstractive).

In future iterations, fine-tuning on datasets like CNN/DailyMail or XSum, with more aggressive length penalties or shorter target lengths, would improve abstract summarization.

🧑‍💻 What I learned
How to fine-tune encoder-decoder architectures like BART for summarization.

The impact of max_length, num_beams, length_penalty on generated summaries.

Using transformers.Trainer and pushing models & tokenizers to the Hugging Face Hub.

🚀 Future work
✅ Tune decoding parameters further
✅ Train on longer documents with shorter targets for more abstractive output
✅ Experiment with sampling (top_k, top_p) for diverse summaries

🔗 Model on the Hub
👉 Youssef-El-SaYed/My-Good-Summarizer

✌️ Interview note
This project demonstrates end-to-end ML capability:

loading pretrained models,

fine-tuning on a summarization dataset,

managing tokenizer alignment,

pushing to the Hub,

loading back for inference with custom decoding strategies.

