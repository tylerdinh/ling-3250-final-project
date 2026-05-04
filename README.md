# Analyzing the Efficacy of a Small BERT Model for Part-of-Speech Tagging

## Overview

Part-of-speech (POS) tagging is one of the foundational tasks in Natural Language Processing (NLP), involving the labeling of every word in a sentence with its grammatical category. While classical rule-based and statistical taggers have existed for decades, modern Transformers approaches like the bidirectional, encoder-only BERT model have shown improved performance on POS tagging tasks. This project will fine-tune a small, pretrained BERT model to perform POS tagging on English text, and then conduct a linguistic analysis of where and why the model makes errors. 

The data will be sourced from the Brown corpus, available directly through the NLTK package, which contains approximately one million words annotated with POS tags. This corpus will be split into a 80%/20% train-test split following standard machine learning practices. The model will be DistilBERT, a 40% smaller size and 60% faster runtime spin of BERT that is available through Hugging Face’s Transformers package. As a BERT family model, it can be fine-tuned as a token classification model for POS tagging tasks. The fine-tuned DistilBERT model will be publicly released on Hugging Face, allowing it to be easily used for evaluation on the test split in a Jupyter Notebook without needing to locally fine-tune it yourself.

The computational component involves setting up the data pipeline, tokenizing the corpus in a way that preserves word-to-tag alignment, fine-tuning the model, and evaluating with standard metrics including a classification report for each tag, a confusion matrix across tag classes, and a list of common prediction errors. The linguistic component will mainly include an analysis of the model's tagging errors and a focus on ambiguous words that can function as multiple parts of speech depending on context. I will also compare the fine-tuned DistilBERT model against NLTK's perceptron model POS tagger to see what differences exist between the two approaches.

## Repository Structure

fine_tune_distilbert.ipynb - The whole final project. It includes dataset explortation (Brown corpus), fine-tuning of DistilBERT Transformer model, and evaluation of the fine-tuned model on the test set.

report/ling_3250_final_project_report.pdf - The description of the whole final project in PDF format, compiled from LaTeX code in the same directory. It is a better and more comprehensive description / project overview than what this README.md file or project notebook file provides (they do still have description).

## Timeline

Start - Mid April
- Fully fine-tune DistilBERT on my own laptop
- Release public fine-tuned model through HF!
- Continue readings, specifically NLP with Transformers for getting evaluation ideas

Mid April - End
- Finish this README.md
- Finish the project, using the fine-tuned model to perform ML / Linguistic analysis
- Write and revise model page on Hugging Face for style, clarity, etc.
- Create project report through TeX

## References

[Chapter 2 of Natural Language Processing with Transformers, Revised Edition](https://www.oreilly.com/library/view/natural-language-processing/9781098136789/) - learned a bit more about Transformers and NLP with this

[Hugging Face DistilBERT API docs](https://huggingface.co/docs/transformers/en/model_doc/distilbert)

[Hugging Face Dataset API docs](https://huggingface.co/docs/datasets/package_reference/main_classes)

[Hugging Face Trainer API docs](https://huggingface.co/docs/transformers/main_classes/trainer)

[Hugging Face DistilBERT-Brown-POS Model Card](https://huggingface.co/nevertipyourlandlord/distilbert-brown-pos) - the actual fine tuned model that I was able to get

[PyTorch API docs](https://devdocs.io/pytorch~1.13/)







