---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
---

## <img src="https://img.icons8.com/dusk/24/000000/open-source.png"/> Open-Source Contributions

---

### [Government Auto Insurance QA Assistant](https://github.com/AbuUbaida/saaq_qa_assistant)
* Built and deployed an end-to-end Retrieval-Augmented Generation (RAG) system to answer regulatory questions about Quebec auto insurance, reducing hallucinations by grounding LLM responses in retrieved legal documents using Weaviate, LangChain, and HuggingFace models.
* Designed a hybrid retrieval pipeline (semantic + keyword search) that indexes web and PDF content into a vector database, embeds user queries locally, and returns citation-backed answers with tracked latency and streaming support.
* Engineered a microservice architecture with FastAPI (backend), Streamlit (frontend), and Weaviate (vector DB), containerized using Docker for reliable inter-service communication, and deployed to a live production environment.
* Implemented systematic evaluation and observability for the RAG pipeline using RAGAS for faithfulness, answer relevancy, and context precision, and Phoenix (Arize) with OpenTelemetry to collect telemetry data for monitoring, debugging, and iterative quality improvements in production.


### [Open-Target Stance Detection](https://github.com/AbuUbaida/opentarget)
* Deﬁned and implemented Open-Target Stance Detection (OTSD), a novel zero-shot framework that eliminates the need for predeﬁned target lists by jointly performing target generation (TG) and stance detection (SD) from raw text.
* Engineered a custom evaluation metric (BTSD) by ﬁne-tuning a BERTweet classiﬁer on a consolidated dataset of 19 targets, achieving a high correlation with human judgment (tau 0.85) to validate target quality.
* Executed a large-scale comparative analysis of 8 LLMs, including proprietary (GPT, Gemini) and open-source models (Llama-3, Mistral), across 14,000+ samples from 3 real-world datasets (TSE, VAST, and EZSTANCE) on a high-performance computing (HPC) server.
* Optimized prompt engineering strategies, demonstrating that joint prompting (TG&SD) signiﬁcantly outperforms sequential workﬂows and Chain-of-Thought (CoT) in maintaining  target-stance coherence.
* Achieved a 13% absolute F1 improvement over the State-of-the-Art (SOTA) TSE baseline, with Mistral-Large reaching a macro F1 of 51.3% on explicit targets and 50.4% on  challenging implicit targets.
* Conducted systematic error analysis on low-context, non-explicit posts, identifying semantic drift in zero-shot models and proposing an LLM-based "coherence judge" to improve multi-target alignment.


### [Bangla News Headline Generation](https://github.com/dialect-ai/BenHeadGen)
* Engineered the Shironaam corpus, a benchmark dataset of 240,000+ Bengali news articles integrated with multimodal auxiliary data, including image captions, topic keywords, and 13 category labels.
* Built a comprehensive preprocessing pipeline to clean 900,000 raw samples crawled from 7 major dailies, utilizing regex and frequency-based ﬁltering to eliminate boilerplate text and noisy caption tokens.
* Developed an encoder-decoder (BED) model using BanglaBERT as the backbone, leveraging a BERT-to-BERT framework to achieve high-quality abstractive summarization in a low-resource language setting.
* Designed BenSim, a BERT-powered semantic similarity module that performs coarse-to-ﬁne ﬁltering of long article to select the top k topically-relevant sentences, eﬀectively managing the 512-token input constraint.
* Implemented a parallel fusion strategy that concatenates image captions and topic-ﬁltered sentences, yielding a 17.5% increase in ROUGE-1 scores compared to the article-only base model.
* Outperformed standard baselines (LEAD-1, IndicBART, and BanglaT5) by 3–10% across all metrics, achieving a peak ROUGE-1 of 52.19 and BLEU of 31.80.
* Fine-tuned the 249M-parameter model using HuggingFace and AdamW optimization for 110k steps, utilizing beam-search with length penalties and n-gram constraints to ensure headline ﬂuency.
* Conducted a domain-wise evaluation across 13 categories, demonstrating consistent performance gains in few-shot domains (e.g., Economy, Life-Health) where training data was limited.


### [BenSim](https://github.com/dialect-ai/BenSim)
* A Python package for measuring the semantic similarity among sentences in the Bengali language.
* Users will provide a reference sentence and a list of target sentences as input; and optionally the similarity assessment approach _(Default: Cosine Similarity)_ and the maximum sequence length _(Default: 512)_. The length will be calculated in terms of the number of tokens using the [WordPiece tokenizer](https://huggingface.co/course/chapter6/6?fw=pt#tokenization-algorithm). Currently, the maximum sequence length limit is 512.
* BenSim will perform [normalization](https://github.com/csebuetnlp/normalizer) on the input texts and extract the contextual embeddings of the reference sentence and target sentences through a [pre-trained BERT](https://huggingface.co/sagorsarker/bangla-bert-base) model. The similarities will be measured between each of the sentence pairs by applying either [Euclidean distance](https://en.wikipedia.org/wiki/Euclidean_distance) or [Cosine similarity](https://en.wikipedia.org/wiki/Cosine_similarity) (based on the input parameter).
* Finally, this will return a list of similarity scores between the reference sentence and the target sentences. If the assessment method is `cosine`, the higher scores will denote higher similarity, and the opposite will be for `euclidean`.


### [mSentsTokenizer](https://github.com/AbuUbaida/mSentsTokenizer)
* A Python package for tokenizing multilingual documents at the sentence level.
* Users will provide a document to be segmented and the language of the document as input. Currently, there are supports for **41 languages** ranging from low to high resource, which belong to **10 language families** ( _i.e._ Afro-Asiatic, Indo-European, Sino-Tibetan, Austronesian, Japanese, Altaic, Dravidian, Tai-Kadai, Austro-Asiatic, and Niger-Congo).
* mSentsTokenizer matches the input language with the [available supports](https://github.com/AbuUbaida/mSentsTokenizer#invoked-libraries) of language from the pre-existing packages and simply invokes the corresponding package to tokenize the input document. Finally, this will return a list of sentences as the output.



## <img src="https://img.icons8.com/external-dygo-kerismaker/24/000000/external-Project-crowdfunding-dygo-kerismaker.png"/> Experimental Projects

---

* **Question Similarity Assessment using Transfer Learning:** The basic workflow of transfer learning from a general pre-trained language model ([BERT](https://arxiv.org/abs/1810.04805)) to a specific task of similarity assessment was practiced. For this task, the [Quora dataset](https://huggingface.co/datasets/quora) was utilized, which is composed of question pairs for the task to determine if the qustions are paraphrases of each other (have the same meaning). For avoiding the model level complexity and to minimize the expensive GPU cost, a basic transformer model ([bert-base-uncased](https://huggingface.co/bert-base-uncased)) was used from [HuggingFace](https://huggingface.co/) library. The codebase **(PyTorch)** can be found [here](https://github.com/AbuUbaida/quesSim-bert "GitHub").

* **News Classification using Vanilla Transformer:** The main goal was to explore the transformer from ["Attention is All You Need"](https://arxiv.org/abs/1706.03762) from scratch and implement it for text classification. For this task, the [AG news classification dataset](https://www.kaggle.com/datasets/amananandrai/ag-news-classification-dataset) was utilized, which is constructed by choosing 4 largest classes from the [original corpus](http://groups.di.unipi.it/~gulli/AG_corpus_of_news_articles.html). The transformer network implementation was based on the [annotated version](http://nlp.seas.harvard.edu/2018/04/03/attention.html) from Harvard NLP, but some modifications were made to work for the text classification problem. Only the encoder part was used, residual connection and layer normalization were skipped, and the masking was not considered either. For extracting the features, multihead attention and positionwise feedforward network were incorporated, and finally, a linear layer was added to get the logits. The codebase **(PyTorch)** can be found [here](https://github.com/AbuUbaida/classification-trans-vanilla).

* **B2E Neural Machine Translation with Seq2Seq Model using Attention:** In this experiment, machine translation was performed using a deep learning based approach and attention mechanism. Specifically, a sequence to sequence model was trained for Bengali to English translation. For this task, a [bilingual corpus](http://www.manythings.org/anki/) was utilized, which is formed with tab-delimited Bengali-English sentence pairs. [GRU](https://en.wikipedia.org/wiki/Gated_recurrent_unit) was incorporated in both of the encoder and decoder with attention layer. After learning the patterns in input language (_i.e._ Bengali), the encoder output and hidden state were passed to the decoder along with the start token for generating the output sequences (_i.e._ English). For deciding the next input to the decoder, teacher forcing was performed. The codebase **(PyTorch)** can be found [here](https://github.com/AbuUbaida/b2e-nmt-attention).

* **Character-Level Name Generation using LSTM:** The focus of this experiment was to train a language model to generate text character-by-character. For this task, an [English name corpus](https://data.world/nkrishnaswami/us-ssa-baby-names-national) was chosen from Data World which contains a large number of baby names. Considering the longer inputs, LSTM model was incorporated to generate the names. In this case, each of the input and output tokens is a character. Moreover, the language model outputs a conditional probability distribution over the character set. According to this generated probability distribution, the next token was picked using [Top-K sampler](https://huggingface.co/blog/how-to-generate#top-k-sampling). The codebase **(PyTorch)** can be found [here](https://github.com/AbuUbaida/nameGen-lstm).



## <img src="https://img.icons8.com/stickers/24/000000/my-computer.png"/> Undergraduate Course Projects

---

* **Bengali Handwritten Digit Recognition using Deep Neural Network:** Implemented a deep neural network model for Bengali handwritten digit classification in the Soft Computing Lab. Experimented with different hyper-parameter settings. <span style="color:RoyalBlue">(DNN, PyTorch)</span> _[Fall 2020]_

* **Flight Fare Prediction using Machine Learning:** A project for predicting flight fares of Indian Airlines using classical Machine Learning algorithms in the Pattern Recognition Lab. The performance was compared between different regression algorithms _i.e._ Linear, Lasso, Ridge, Elastic Net, Decision Tree, Random Forest, and Gradient Boosting. In addition to this, the dataset was analyzed by Bar plot, Count plot, Box plot, and Scatter plot. <span style="color:RoyalBlue">(Matplotlib, Seaborn, Scikit-Learn, XGBoost, Python)</span> _[Fall 2020]_
 
* **House Price Prediction using PL/SQL**: This project was done in the Distributed Database Systems Lab where Linear Regression was performed in the context of PL/SQL. Training data were stored in the distributed database. Two virtual PCs were created to make a distributed system. One user could perform CRUD operations on the database containing training data; on the other hand, another user could get a prediction on unseen data through the command line interface by applying Linear Regression rule on the database. <span style="color:RoyalBlue">(PL/SQL, Logistic Regression, Virtual Box)</span> _[Spring 2020]_

* **Library Management System:** A simple web application for a digital library management system, was developed in the Software Development Lab. Users were able to search for books based on author, genre, _etc._ and borrow books to read them online. <span style="color:RoyalBlue">(C#, MS .Net, MySQL)</span> _[Fall 2019]_

* **Medicine Sheba:** A cross-platform application for medicine sales & delivery systems was built in the Information System Design and Software Engineering Lab. There was a dual-user mode. The general users could search for necessary medicines from a central database containing information from all the registered pharmacies' individual databases; users could place an order from any specific pharmacy and also were able to track their order. On the other hand, the Pharmacies could register themselves, maintain their own database, and sell their products. <span style="color:RoyalBlue">(JavaScript, NoSQL, React Native, MongoDB, Express, Node.js)</span> _[Fall 2019]_

* **Criminal Management System (CMS):** A desktop application for criminal data management was built in the Database Lab. Law enforcement agencies could manage a relational database of criminals and store all sorts of information including custody info, general diary info, criminal images, and so on. The focus was to perform advanced operations on tables to maintain the dynamic of the CRUD operations. <span style="color:RoyalBlue">(RDBMS, Java, MySQL, MS SQL Server)</span>  _[Spring 2019]_

* **Talks of Code:** A website was built with PHP in the Software Development Lab. The focus was to make a tutorial site for learning programming languages through reading documents. <span style="color:RoyalBlue">(PHP, HTML, CSS)</span> _[Spring 2019]_

* **Police Assistant:** An android mobile application was built in the Software Development Lab. There was a dual-user mode: Admin, General. Law enforcement agencies could act as admins and post information about suspects or wanted persons including their pictures. Regular citizens, on the other hand, could act as General users, where they could respond to any post by in-app call or by leaving a private comment. There was a feature of rewarding the informant upon justification. <span style="color:RoyalBlue">(Java, Android Studio, MySQL)</span> _[Fall 2018]_

* **Check My Trip:** A desktop application, was developed in the Software Development Lab. Users were able to find nearby visiting places, mosques, hospitals, _etc._ by locating their current latitude-longitude. Additionally, there were features like finding the distance between two places, setting a location as an attractive spot by the local people which might not be shown on Google Map as a visiting place, and getting the list of transportation costs from the current location to the destination (especially for a long drive). All the features were implemented by leveraging Google Map API. <span style="color:RoyalBlue">(Java, JavaFX, Google Map API)</span> _[Spring 2018]_

* **The Driver:** This was a racing game, built in the Software Development Lab. Here you can play as a cop & as a racer. The cop has a special bullet by which it can destroy the racing car. In the racer mode, there is an extra NOS facility for the racer. There is _[gameplay](https://youtu.be/HkmhB2Hv_-g)_ available on YouTube. <span style="color:RoyalBlue">(C++, iGraphics, Visual Studio)</span> _[Fall 2017]_

---

[<img src="https://img.icons8.com/emoji/24/000000/up-arrow-emoji.png"/>Top](https://abuubaida.github.io/projects/#)