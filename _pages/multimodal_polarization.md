---
title: ""
permalink: /multimodal_polarization/
layout: single
mathjax: true
classes: wide
---
## Methodological Advances in the Study of Online Antisemitism:
<img src="/images/header.PNG" alt="header" width="550">

**Keywords:**  
multimodal analysis · computational social science · political communication · algorithmic social media · short-form video

---

Studying the extent of online hate speech and antisemitism is essential to understanding the dynamics of digital discourse, which can help predict ongoing societal changes beyond the digital realm. However, the underlying factors that make antisemitic narratives so persuasive are frequently overlooked. This project focuses on emotive layers embedded in digital media that influence the spread of hate speech and antisemitism. It examines how frequently users devalue Jews and Israel, contrasting these expressions with those directed at opposing entities, including instances of sympathy for, or even endorsement of, violent actors such as Hamas. 

### *Beyond the Written Word...*

*Beyond the written word*, the project analyzes the **multifaceted layers of political communication** by utilizing cutting-edge technology that incorporates both **audio and visual signals** into its analysis, aiming to understand and scale the dynamics that create fertile ground for hostility in digital realms.

**Key questions driving the project include:**

1. What methodological advances are necessary to analyze online hate and measure multimodal content effectively?
2. How can these dynamics be robustly measured at scale and tracked longitudinally?
3. What recurring visual frames appear in today’s increasingly dominant short-form video content?
4. Which metrics best explain why polarizing narratives spread widely on Web 2.0 platforms?

These questions are addressed through a series of high-quality NLP-based research papers.

The paper series conducts empirical research on how political narratives circulate online by analyzing international news content, particularly on YouTube—the second most visited website worldwide. It focuses on state-funded and state-supported outlets, such as **Al Jazeera, the BBC, Deutsche Welle, and TRT World**. Using a longitudinal approach, the project measures the proportionality and dynamics of content related to the aftermath of the **Israel–Hamas war since October 7, 2023**.

<img src="/images/slideshow_3s_per_image.gif" alt="Slides" width="250">

---

## Empirical Studies


### Study 4: Multimodal Analysis of State-Funded News Coverage of the Israel–Hamas War on YouTube Shorts

<img src="https://www.random-nodes.com/wp-content/uploads/2022/04/ACL_Anthology_logo-1.jpg" alt="ACL" width="25%"> <img src="https://www.ilc.cnr.it/wp-content/uploads/2025/07/LREC2026.png" alt="LREC2026" width="5.7%">

*Proceedings of the Fourteenth Language Resources and Evaluation Conference (LREC 2026)*

**Download paper:** in print

YouTube Shorts have become central to news consumption on the platform, yet research on how geopolitical events are represented in this format remains limited. To address this gap, we present a multimodal pipeline that combines automatic transcription, aspect-based sentiment analysis (ABSA), and semantic scene classification. The pipeline is first assessed for feasibility and then applied to analyze short-form coverage of the Israel–Hamas war by state-funded outlets. Using over 2,300 conflict-related Shorts and more than 94,000 visual frames, we systematically examine war reporting across major international broadcasters. Our findings reveal that the sentiment expressed in transcripts regarding specific aspects differs across outlets and over time, whereas scene-type classifications reflect visual cues consistent with real-world events. Notably, smaller domain-adapted models outperform large transformers and even LLMs for sentiment analysis, underscoring the value of resource-efficient approaches for humanities research. The pipeline serves as a template for other short-form platforms, such as TikTok and Instagram, and demonstrates how multimodal methods, combined with qualitative interpretation, can characterize sentiment patterns and visual cues in algorithmically driven video environments.

---

### Study 3: Mapping Affective Polarization in YouTube Shorts: A Data-Driven Analysis of Political Communication During the 2023–2024 Israel–Hamas War

<img src="https://images.squarespace-cdn.com/content/v1/685abf29badff21c522541c8/808dd9b5-ce92-4e55-91c2-85015b3fb3c4/DHR_H_Light.png?format=500w" alt="DHA" width="25%">

**Download paper:** in print

This study examines the application of computational models, particularly Aspect-Based Sentiment Analysis (ABSA), to the analysis of political communication in online spaces. The paper provides an in-depth analysis of affective polarization in user-generated content on YouTube Shorts related to the 2023–2024 Israel–Hamas war. By analyzing a dataset comprising over 3.4 million comments and replies, the study utilizes a fine-tuned DeBERTa-v3-large-absa-v1.1 model to trace subtle, nuance-driven sentiment pathways that reveal ideological inclinations towards geopolitical actors. The findings indicate a persistent negative sentiment towards Israel and Zionists, alongside a consistent positive sentiment towards Palestine and Palestinians. Overall, the study illustrates how affective polarization emerges as a reaction to state-funded media discourse. Beyond its methodological contributions, the paper addresses domain adaptation, demonstrating that language imbued with evaluative and emotional undertones can be analyzed and quantitatively assessed to characterize political discourse within Web 2.0 ecosystems. Furthermore, it connects these dynamics to broader discussions surrounding polarization in digital mainstream environments.


---

### Study 2: Analyzing Polarization in Online Discourse on the 2023–2024 Israel–Hamas War

*Proceedings of the 21st Conference on Natural Language Processing (KONVENS 2025): Workshops, pages 7–16, Hannover, Germany.*  

<img src="https://www.random-nodes.com/wp-content/uploads/2022/04/ACL_Anthology_logo-1.jpg" alt="ACL" width="25%"> <img src="https://cpss-sig.github.io/CPSS-2025/gscl_en_light.svg" alt="ACL" width="25%">

**Download paper:** <https://aclanthology.org/2025.konvens-2.1/>

We investigate large-scale sentiment analysis of YouTube Shorts in the context of the 2023-2024 Israel–Hamas war. Using a corpus of over 3 million user comments and replies from four state-funded or state-supported international media channels, we track sentiment toward key geopolitical and ideological entities over the course of one year. We investigate the correspondence between large-scale sentiment analysis and manual fine-grained analysis of trends as well as the correspondence between a logitudinal analysis and geopolitical events. Results show that overall sentiment trends depict user attitudes, but to interpret these patterns correctly, we need domain-specific knowledge and a combination of the automatic analysis with fine-grained manual analysis. We also show that the peaks of a longitudinal analysis correspond to (geo-)political events such as the Eurovision Song Contest.

---

### Study 1: Investigating Polarization in YouTube Comments via Aspect‑Based Sentiment Analysis

*Proceedings of the 15th International Conference on Recent Advances in Natural Language Processing – NLP in the Generative AI Era (RANLP 2025).*  

<img src="https://www.random-nodes.com/wp-content/uploads/2022/04/ACL_Anthology_logo-1.jpg" alt="ACL" width="25%"> <img src="https://azizcu.github.io/img/pubs/RANLP2025.png" alt="RANLP" width="5.6%">

**Download paper:** <https://aclanthology.org/2025.ranlp-1.83/>

We investigate the use of Aspect-Based Sentiment Analysis (ABSA) to analyze polarization in online discourse. For the analysis, we use a corpus of over 3 million user comments and replies from four state-funded media channels from YouTube Shorts in the context of the 2023 Israel–Hamas war. We first annotate a subsample of approx. 5 000 comments for positive, negative, and neutral sentiment towards a list of topic-related aspects. After training an ABSA model (Yang et al., 2023) on the corpus, we evaluate its performance on this task intrinsically, before evaluating the usability of the automatic analysis of the whole corpus for analyzing polarization. Our results show that the ABSA model achieves an F1 score of 77.9. The longitudinal and outlet analyses corroborate known trends and offer subject experts more fine-grained information about the use of domain-specific language in user-generated content.

---

## Further Research Outputs

*YouTube Shorts from Major News Outlets on the Israel–Hamas War (October 2023–October 2024).*   

<img src="https://blog.zenodo.org/static/img/logos/zenodo-gradient-1000.png" alt="Zenodo" width="15%">

**Download dataset**: <https://zenodo.org/records/18017938>

This dataset comprisies the metadata of 2,370 publicly accessible YouTube Shorts disseminated by four prominent international news outlets covering the Israel–Hamas war between October 2023 and October 2024. It supports replication of the aforementioned studies and enables further research on **short‑form news coverage** and online discourse.  

---

## Talks & Conferences

### 2026
- **Analyzing Multimodal Political Communication in State-Funded News**  
  *Antisemitism & AI Forum, Contemporary Antisemitism*, Haifa, Israel.

### 2025
- **Affect Mobilization on YouTube: Emotional Toning in State-Funded News Outlets Covering the Israel–Hamas War**  
  *ISCA Early Career Speaker Series*, Indiana University, USA.

- **Analyzing Polarization in Online Discourse on the 2023–2024 Israel–Hamas War**  
  *5th Workshop on Computational Linguistics for the Political and Social Sciences (CPSS)*, University of Hildesheim, Germany.

- **Analyzing State Media and Online Commentary After October 7: A Longitudinal Study of Sentiment and Narrative**  
  *Touro University*, New York City, USA.

- **Emotion in Motion: Shifting Narratives and Sentiment in State Media and Social Discourse After October 7**  
  *Brock University*, St. Catharines, Canada.

- **Antisemitic Discourses and Discourses on Antisemitism Post–October 7**  
  *Jewish Community Centre*, London, UK.

- **Tracking Sentiment Shifts and Linguistic Patterns in Online Discourse After October 7**  
  *NLP Lab, Luddy School of Informatics, Indiana University*, USA.


---

## Contact & Inquiries

This research project is led by **Daniel Miehling** (PhD).

- **Email:** damieh@iu.edu  
- **GitHub:** <https://damieh1.github.io/>  

*If you use or cite this project, a short note is always greatly appreciated.*
