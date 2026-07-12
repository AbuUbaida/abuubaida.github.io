---
layout: archive
title: "Experience"
permalink: /experience/
author_profile: true
---

{% include base_path %}

## Professional Experience

---

* **Graduate Student Researcher**\\
SAILI Lab, Université de Sherbrooke, Quebec, Canada\\
    * **Period:** September 2023 – August 2025
    * Conceptualized and formalized "Open-Target Stance Detection", a new generative task that enables LLMs to identify both targets and stances without predeﬁned lists, addressing a critical gap in real-world, unstructured data analysis.
    * Designed and executed a comparative study of 8+ state-of-the-art models (GPT, Gemini, Llama-3, Mistral) across three benchmark datasets, processing over 17,000 text samples on a high-performance computing (HPC) server.
    * Developed "BTSD," a semantic similarity metric based on BERTweet embeddings, evaluate generative target quality; achieved a Pearson correlation of 0.85 with human judgment, signiﬁcantly outperforming standard metrics like SemSim (0.57).
    * Developed and iterated on prompt strategies, including Chain-of-Thought (CoT) and multi-stage zero-shot instruction, to improve model performance in detecting non-explicit targets by over 15% in complex reasoning scenarios.
    * Conducted a granular diagnostic of 500+ model failures, categorizing errors into 8 distinct categories; quantiﬁed a speciﬁc performance drop in "Non-explicit" target scenarios, where model accuracy fell signiﬁcantly compared to "Explicit" mentions.
    * Managed a team of 3 annotators to establish a gold-standard validation set for generative targets; ensured statistical rigor by calculating a Krippendorﬀ’s alpha of 0.76 and a Fleiss’ kappa of 0.664 for inter-rater agreement.
    * Validated that generative LLMs outperform traditional Target-Stance Extraction (TSE) models by 104% in human evaluation relevance scores (0.690 for GPT-4o vs. 0.338 for the TSE baseline).
    * Managed the full R&D lifecycle over a 24-month period, from initial literature synthesis and hypothesis formulation to experimental execution, technical documentation, and peer-reviewed publication to ACL.
<br/>
<br/>

* **Research Engineer** _(Speech & NLP)_\\
[AIMS Lab](https://aimsl.uiu.ac.bd/#/ "https://aimsl.uiu.ac.bd/"), [UIU](https://www.uiu.ac.bd/), Dhaka, Bangladesh\\
    * **Period:** February 2023 – May 2023
    * Architected a national-scale data acquisition and preprocessing pipeline to train a clinical Named Entity Recognition (NER) model for automated medical scribing, projected to streamline workﬂows for 100K clinicians nationwide.
    * Developed a conversation audio recorder to deploy across 6 distinct clinical locations, establishing a distributed data collection network.
    * Secured high-level project clearance and formalized data-sharing protocols with BMRC, DGHS, and UNICEF.
    * Engineered an automated audio processing pipeline that compresses raw clinical recordings into 320K bitrate MP3s at a 44K sample rate to ensure optimal acoustic feature density for model training.
    * Implemented a redundant storage system using Amazon S3 for centralized cloud access and password-encrypted local storage for immediate clinical data protection.
    * Developed a robust anonymization workﬂow utilizing vocal tuning to disable voice identiﬁcation systems, ensuring patient privacy while maintaining the linguistic utility of the audio.
    * Orchestrated a REST API-driven synchronization between the recording hardware, the DGHS Server, and the Clinic EHR management system to capture critical metadata (Doctor ID, Patient ID, Location ID).
    * Established a multi-stage Human-in-the-Loop workﬂow involving Manual Transcription and Cross-Checking to generate high-accuracy ground truth data.
    * Designed an Audio Segmentation process to create paired datasets for acoustic modeling and integrated 2 Domain Experts to perform gold-standard clinical information annotation.
    * Implemented a systematic Inter-Annotator Agreement (IAA) veriﬁcation step to ensure the reliability of labeled data prior to Custom NER model training.
<br/>
<br/>

* **Machine Learning Research Engineer**\\
[Intelsense AI](https://intelsense.ai/ "https://intelsense.ai/"), Dhaka, Bangladesh\\
    * **Period:** September 2021 – April 2022
    * Implemented a G2P model for Bengali and gained state-of-the-art accuracy (99%) on unseen data.
    * Prepared large-scale (nearly 600 hours) audio data for better Bengali ASR training.
    * Speech synthesis: Implemented Coqui TTS models for low-resourced language like Bengali.
    * Conversational AI: Developed AI-driven chatbots using Rasa Open Source.
    * [Bengali transcriber](https://sensevoice.intelsense.ai/ "https://sensevoice.intelsense.ai/"): Prepared the annotated corpus for the Bengali transcriber; already in use.
<br/>
<br/>

* **Machine Learning Research Intern**\\
[Intelsense AI](https://intelsense.ai/ "https://intelsense.ai/"), Dhaka, Bangladesh\\
    * **Period:** June 2021 – August 2021
    * Developed the pipeline for Bengali text normalization and punctuation restoration.
    * Reviewed the literature of the related technologies.



## Voluntary Service

---

* **Reviewer** at [COLING 2025](https://coling2025.org/) (Abu Dhabi, UAE)
    * **Period:** Oct 2024 – Nov 2024

* **Manager**, Committee of External Affairs at the Association of the Muslims of University of Sherbrooke ([AMUS](https://www.instagram.com/amus_uds/)), Canada
    * **Period:** Nov 2024 – Nov 2025

<!-- * **Member**, Committee of External Affairs at the Association of the Muslims of University of Sherbrooke ([AMUS](https://www.instagram.com/amus_uds/))
    * **Period:** _Nov 2023 – Oct 2024_ -->

* **Student Volunteer** at [EACL](https://2023.eacl.org/calls/volunteers/) (Dubrovnik, Croatia)
    * **Period:** May 2023 – May 2023
    * Helped people find the rooms, their poster, etc. in [GatherTown](https://www.gather.town/) during the virtual poster sessions

<!-- * **General Member** at AUST Innovation and Design Club ([AUSTIDC](https://aust-idc.com/ "https://aust-idc.com/"))
    * **Period:** _May 2017 – December 2021_
    * AUSTIDC ID 1702271
    * Affiliated with Ahsanullah University of Science and Technology ([AUST](https://www.aust.edu/, "https://www.aust.edu/")) -->

* **Communication Responsible** at [Mozilla](https://community.mozilla.org/en/groups/mozilla-bangladesh/ "Community Website"), Bangladesh
    * **Period:** January 2018 – January 2018
    * Affiliated with Ahsanullah University of Science and Technology ([AUST](https://www.aust.edu/, "https://www.aust.edu/"))

<!-- * **Content Developer** at [Durbin Labs Limited](https://durbinlabs.com/ "https://durbinlabs.com/")
    * **Period:** _June 2018 – August 2018_
    * Affiliated with Durbin Labs Limited -->



## Honours & Awards

---

* **<span style="color:RoyalBlue">Marc-Andr´e Roy Scholarship</span>** from the Université de Sherbrooke _(March 2024)_
* **<span style="color:RoyalBlue">Diversity & Inclusion Award</span>** (Registration fee waiver, travel grant, hotel accommodation) from [EACL](https://2023.eacl.org/calls/d-i-subsidies/) (Dubrovnik, Croatia); sponsored by [Amazon Science](https://www.amazon.science/) _(2023)_
* Robi-Datathon 2.0 **<span style="color:RoyalBlue">Finalist</span>** (Top 6% among 358 Teams); organized by [Robi Axiata Limited](https://www.robi.com.bd/en) _(2022)_
* Game Showcasing Competition **<span style="color:RoyalBlue">1st Runner-Up</span>**; organized by [AUST IDC](https://aust-idc.com/ "https://aust-idc.com/") _(Spring 2018)_



## Contests & Participations

---

* Intra AUST Programming Contest organized by [AUST CSE Society](https://www.aust.edu/cse "https://www.aust.edu/cse") _(Spring 2019)_
* Intra AUST Project Showcasing organized by [AUST CSE Society](https://www.aust.edu/cse "https://www.aust.edu/cse") _(Spring 2018)_
* Innoventure Engineering Olympiad organized by [AUST IDC](https://aust-idc.com/ "https://aust-idc.com/") _(Spring 2017)_
* Web Compatibility Sprint organized by [AUST IDC](https://aust-idc.com/ "https://aust-idc.com/") _(Spring 2017)_
* 1st AML-ACC National Science Festival organized by [Neutrino ACC Science Club](https://www.nasc.com.de/) _(2014)_

<!-- {% for post in site.experience %}
  {% include archive-single.html %}
{% endfor %} -->

---

[<img src="https://img.icons8.com/emoji/24/000000/up-arrow-emoji.png"/>](https://abuubaida.github.io/experience/#)[Top](https://abuubaida.github.io/experience/#)