---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

## <img src="https://img.icons8.com/dusk/24/000000/open-source.png"/> Open-Source Contributions

---

### BenSim
* A Python package for measuring the semantic similarity among sentences in the Bengali language.
* Users will provide a reference sentence and a list of target sentences as input; and optionally the similarity assessment approach _(Default: Cosine Similarity)_ and the maximum sequence length _(Default: 512)_. The length will be calculated in terms of the number of tokens using the WordPiece tokenizer. Currently, the maximum sequence length limit is 512.
* BenSim will perform normalization on the input texts and extract the contextual embeddings of the reference sentence and target sentences through a pre-trained BERT model. The similarities will be measured between each of the sentence pairs by applying either Euclidean distance or Cosine similarity (based on the input parameter).
* Finally, this will return a list of similarity scores between the reference sentence and the target sentences. If the assessment method is `cosine`, the higher scores will denote higher similarity, and the opposite will be for `euclidean`.
* Detail usage can be found [here](https://github.com/AbuUbaida/BenSim "GitHub").

### mSentsTokenizer
* A Python package for tokenizing multilingual documents at the sentence level.
* Users will provide a document to be segmented and the language of the document as input. Currently, there are supports for **41 languages** ranging from low to high resource, which belong to **10 language families** ( _i.e._ Afro-Asiatic, Indo-European, Sino-Tibetan, Austronesian, Japanese, Altaic, Dravidian, Tai-Kadai, Austro-Asiatic, and Niger-Congo).
* mSentsTokenizer matches the input language with the available supports of language from the pre-existing packages and simply invokes the corresponding package to tokenize the input document. Finally, this will return a list of sentences as the output.
* Detail usage can be found [here](https://github.com/AbuUbaida/mSentsTokenizer "GitHub").



## <img src="https://img.icons8.com/external-dygo-kerismaker/24/000000/external-Project-crowdfunding-dygo-kerismaker.png"/> Experimental Projects

---

* **Question Similarity Assessment using Transfer Learning:** The basic workflow of transfer learning from a general pre-trained language model ([BERT](https://arxiv.org/abs/1810.04805)) to a specific task of similarity assessment was practiced. For this task, the [Quora dataset](https://huggingface.co/datasets/quora) was utilized, which is composed of question pairs for the task to determine if the qustions are paraphrases of each other (have the same meaning). For avoiding the model level complexity and to minimize the expensive GPU cost, a basic transformer model ([bert-base-uncased](https://huggingface.co/bert-base-uncased)) was used from [HuggingFace](https://huggingface.co/) library. The codebase **(PyTorch)** can be found [here](https://github.com/AbuUbaida/quesSim-bert "GitHub").

* **News Classification using Vanilla Transformer:** The main goal was to explore the transformer from ["Attention is All You Need"](https://arxiv.org/abs/1706.03762) from scratch and implement it for text classification. For this task, the [AG news classification dataset](https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset) was utilized, which is constructed by choosing 4 largest classes from the [original corpus](http://groups.di.unipi.it/~gulli/AG_corpus_of_news_articles.html). The transformer network implementation was based on the [annotated version](http://nlp.seas.harvard.edu/2018/04/03/attention.html) from Harvard NLP, but some modifications were made to work for the text classification problem. Only the encoder part was used, residual connection and layer normalization were skipped, and the masking was not considered either. For extracting the features, multihead attention and positionwise feedforward network were incorporated, and finally, a linear layer was added to get the logits. The codebase **(PyTorch)** can be found [here](https://github.com/AbuUbaida/classification-trans-vanilla).

* **B2E Neural Machine Translation with Seq2Seq Model using Attention:** In this experiment, machine translation was performed using a deep learning based approach and attention mechanism. Specifically, a sequence to sequence model was trained for Bengali to English translation. For this task, a [bilingual corpus](http://www.manythings.org/anki/) was utilized, which is formed with tab-delimited Bengali-English sentence pairs. [GRU](https://en.wikipedia.org/wiki/Gated_recurrent_unit) was incorporated in both of the encoder and decoder with attention layer. After learning the patterns in input language (_i.e._ Bengali), the encoder output and hidden state were passed to the decoder along with the start token for generating the output sequences (_i.e._ English). For deciding the next input to the decoder, teacher forcing was performed. The codebase **(PyTorch)** can be found [here](https://github.com/AbuUbaida/b2e-nmt-attention).

* **Character-Level Name Generation using LSTM:** The focus of this experiment was to train a language model to generate text character-by-character. For this task, an [English name corpus](https://data.world/nkrishnaswami/us-ssa-baby-names-national) was chosen from Data World which contains a large number of baby names. Considering the longer inputs, LSTM model was incorporated to generate the names. In this case, each of the input and output tokens is a character. Moreover, the language model outputs a conditional probabilty distribution over the character set. According to this generated probabilty distribution, the next token was picked using [Top-K sampler](https://huggingface.co/blog/how-to-generate#top-k-sampling). The codebase **(PyTorch)** can be found [here](https://github.com/AbuUbaida/nameGen-lstm).



## <img src="https://img.icons8.com/stickers/24/000000/my-computer.png"/> Undergraduate Projects

---

* **Bengali Hand Digit Recognition using Deep Neural Network:** Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.

* **Flight Fare Prediction using Machine Learning:** Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.

* **Medicine Sheba:** Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.

* **Crime Management System (CMS):** Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.

* **Talks of Code:** Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.

* **Check My Trip:** Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.

* **Police Assistant:** Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.

* **The Driver:** Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum is simply dummy text of the printing and typesetting industry.