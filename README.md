# Analyzing the Efficacy of a Small BERT Model for Part-of-Speech Tagging

## Overview

Part-of-speech (POS) tagging is one of the foundational tasks in Natural Language Processing (NLP), involving the labeling of every word in a sentence with its grammatical category. While classical rule-based and statistical taggers have existed for decades, modern Transformers approaches like the bidirectional, encoder-only BERT model have shown improved performance on POS tagging tasks. This project will fine-tune a small, pretrained BERT model to perform POS tagging on English text, and then conduct a linguistic analysis of where and why the model makes errors. 

The data will be sourced from the Brown corpus, available directly through the NLTK package, which contains approximately one million words annotated with POS tags. This corpus will be split into a 80%/10%/10% TTV split following standard machine learning practices. The model will be DistilBERT, a 40% smaller size and 60% faster runtime spin of BERT that is available through Hugging Face’s Transformers package. As a BERT family model, it can be fine-tuned as a token classification model for POS tagging tasks. The fine-tuned DistilBERT model will be publicly released on Hugging Face, allowing it to be used in a Jupyter Notebook.

The computational component involves setting up the data pipeline, tokenizing the corpus in a way that preserves word-to-tag alignment, fine-tuning the model, and evaluating with standard metrics likely including accuracy and a confusion matrix across tag classes. The linguistic component will include an analysis of the model's tagging errors and a focus on ambiguous words that can function as multiple parts of speech depending on context. I will also compare the fine-tuned DistilBERT model against NLTK's perceptron model POS tagger to see what differences exist between the two approaches.

## Repository Structure

TODO: format and revise

fine_tune_distilbert.ipynb - fine-tuning of DistilBERT Transformer model, in a similar manner to the NLP with Transformers reference. This should use hugging face push_to_hub() to publicly release the fine-tuned POS tagger text classification model on HF, as .safetensors file format ([as the original BERT is also released as this for easy acess with Transformers](https://huggingface.co/distilbert/distilbert-base-uncased/tree/main)) It will also contain evaluation cells, might need to change the file name.


## Timeline

Frequent commits with conventional commits!

Start - Mid April
- have a fine-tuned distilbert (pos_distilbert) model, either trained on Google Colab (most likely) or my own laptop (could also do this) in fine_tune_distilbert.ipynb
- release fine-tuned model (pos_distilbert) on HF publicly!
- continue readings, importantly NLP with Transformers for comp ling related ideas

Mid April - Late April
- finish this README.md
- finish full pipeline from fine-tuned model to ML and Ling analysis, simple explanations of roughly each step in project.ipynb
- think about expanding project if I have more time / think of something cool, likely since this is interesting
    - could maybe do a control loop with user input via STT taking in user speech -> check each POS for user speech -> TTS to tell the user out loud what POS in the sentence they have? easy, relates to FSMs (also easy)

Late April - End
- Revise README.md for style, clarity, etc.
- Revise project.ipynb for style, clarity, etc.
- Revise fine_tune_distilbert.ipynb for style, clarity, etc.
- Write and revise model page for pos_distilbert on Hugging Face for style, clarity, etc.
- Create presentation if requested


## References

Chapter 2 of Natural Language Processing with Transformers, Revised Edition - for Text Classification and DistilBERT fine-tuning usecases of project - which can be found at [this website](https://www.oreilly.com/library/view/natural-language-processing/9781098136789/)

[Hugging Face docs for DistilBERT](https://huggingface.co/docs/transformers/en/model_doc/distilbert)

NLTK Documentation for dataset stuff







