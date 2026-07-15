# MSc Research Notebook

- **Student Name:** James Kelly
- **Student ID:** 23370858
- **Proposed Research Title:** Detecting Bot-Generated Comments: Comparing Transformer-Based and Traditional Machine Learning Detectors for Machine-Generated Text
- **GitHub Repository Link:** https://github.com/Kelzo8/MSc-Research-Notebook-Kelly

------------------------------------------------------------------------

## 1. Project Overview & Evolution Track

Use this section to map out how your project evolves over the block. Whenever you change your research question, methodology, or scope, update this log.

### Current Working Research Question(s)

> *Last Updated: 13/07/2026*  
> How well do transformer-based models perform compared to more traditional machine learning methods when trying to tell apart bot‑generated comments from human comments on online platforms?
### The Pivot Log

Document any major changes in direction here. (e.g., *"Switched from quantitative survey to qualitative interviews because sample access fell through on 15/10/2026"*).

| Date | Previous Direction | New Direction | Reason for Pivot / Academic Justification |
|:-----------------|:-----------------|:-----------------|:-----------------|
|  |  |  |  |
| 09/07/2026 | Broad idea: “How AI can help detect fake or hateful comments etc.”   | Focused comparison of transformer-based vs traditional ML models for toxic/hateful comment detection   | Narrowing to a comparative modelling study makes the project feasible and aligns with current literature on toxic comment classification (e.g., ML vs DL model evaluations). |
| 13/07/2026 | Comparing ML vs deep learning models for detecting toxic/hateful human comments on social media  | Detecting and classifying bot‑ or AI‑generated comments versus human comments on online platforms                    | Bot and AI‑generated text are becoming more common online, and there is now specific work on transformer ensembles and other models for detecting machine‑generated text, so this is both timely and still within the overall theme of online content moderation.
## 2. Critical Source Evaluation Log

Do not just copy and paste citations. For every core paper that shapes your final Introduction, document your active reading process here. Also note papers that looked promising but you decided, on review, to exclude them. Note reasons for exclusion.

### [Paper 1 Short Title / Author Year]

- **Full IEEE/APA Citation:**
- **Why did you select this paper?** (What gap does it address?)
- **Key Findings & Methodology:**
- **Limitations/Weaknesses Identified:**
- **Direct Connection to *Your* Project:** (How does this support or challenge your thesis?)


### RoBERTa Ensemble for Detecting Machine-Generated Text (SemEval‑2024 SCaLAR System) / Kumar et al. 2024

- **Full IEEE/APA Citation:**
  - Kumar, A., B, A., & Murali, S. (2024). *SCaLAR at SemEval‑2024 Task 8: Unmasking the machine: Exploring the power of RoBERTa Ensemble for Detecting Machine Generated Text*. In *Proceedings of the 18th International Workshop on Semantic Evaluation (SemEval‑2024)*, 1135–1139. Association for Computational Linguistics.

- **Why did you select this paper?** (What gap does it address?)
  - I chose this paper because it reports a real system built for a shared task on detecting machine‑generated text from several different models, using RoBERTa and ensembling. It lines up closely with my idea of using transformer‑based detectors for bot comments.

- **Key Findings & Methodology:**
  - The authors augment the training data to handle longer sentences, train three RoBERTa models on different slices of this augmented data, and then combine them with a voting‑based ensemble.
  - Their system reaches 97.05% accuracy on the validation set and 76.25% accuracy on the test set for SemEval Task 8, placing 18th overall.

- **Limitations/Weaknesses Identified:**
  - The paper focuses on benchmark machine‑generated text for a competition rather than messy, real‑world comment data, so it is not clear how well the approach would transfer directly to social media comments.
  - There is limited discussion of error analysis, which would have helped understand where the ensemble struggles (e.g. specific generators or domains).

- **Direct Connection to *Your* Project:** (How does this support or challenge your thesis?)
  - This work gives me a concrete example of how to build and evaluate a transformer‑based ensemble for machine‑generated text detection, including the basic pipeline and performance figures.
  - It supports the idea that transformer models (and ensembles of them) are strong candidates to compare against simpler baselines when detecting bot‑generated comments.

---
### Ensemble and GAN-Based Approaches for Detecting Machine-Generated Text / Sharma 2024 (Purdue MSc Thesis)

- **Full IEEE/APA Citation:**
  - Sharma, S. (2024). *Exploring Ensemble Models and GAN‑Based Approaches for Automated Detection of Machine‑Generated Text* (Master’s thesis, Purdue University).

- **Why did you select this paper?**
  - This thesis looks at several different ways to spot machine‑generated text, including ensemble models and GAN‑based approaches, and reports detailed experiments and results.
  - It is at MSc level, so the scope and methods feel achievable and relevant for my own project.

- **Key Findings & Methodology:**
  - The thesis combines features such as TF‑IDF and RoBERTa embeddings with traditional models like Random Forest to improve detection accuracy.
  - It also explores using GAN‑style architectures, where a discriminator learns to distinguish between genuine and machine‑generated text, and compares these approaches with more standard models.

- **Limitations/Weaknesses Identified:**
  - The datasets used are general text datasets, not necessarily comment‑style data from social platforms, so I will need to be careful when applying the ideas to comment detection.
  - GAN‑based models can be quite heavy and may be more complex than I can realistically implement within an MSc project timeline.

- **Direct Connection to *Your* Project:**
  - The Random Forest + TF‑IDF + RoBERTa setup gives me a clear example of how to mix “traditional” ML with transformer representations in one pipeline, which fits well with my comparison theme.
  - The thesis also reinforces the value of using ensembles and richer feature sets, rather than relying on a single model, which is something I can reflect in my own experimental design.

### Human or Machine? A Survey on Machine-Generated Text Detection / Ahmad et al. 2026

- **Full IEEE/APA Citation:**
  Ahmad, Z., et al. (2026). *Human or Machine? A Survey on Machine-Generated Text Detection*. IEEE Access, 14, 34113–34136. https://doi.org/10.1109/ACCESS.2026.3666781

- **Why did you select this paper?**
  I picked this paper because it is a recent, peer-reviewed survey that looks specifically at how well different methods can detect machine-generated text. It gives an overview of the current state of the field and compares model performance with human performance, which is directly relevant to my thesis.

- **Key Findings & Methodology:**
  The authors review a large number of benchmark corpora and studies on machine-generated text detection and group detection approaches into several classes (classical machine learning, deep learning, transformer-based models, commercial AI detectors, and statistical tools). They show that transformer-based detectors can achieve very high accuracy in some setups, while human evaluators perform noticeably worse, and they summarise common evaluation setups and metrics.

- **Limitations/Weaknesses Identified:**
  The focus is on general machine-generated text rather than on short, informal comments, so the findings may not directly transfer to social media or comment sections without further testing. As a survey, it cannot go into full technical detail for each individual model, so I still need to read primary research papers for deeper methodological insight.

- **Direct Connection to *Your* Project:**
  This survey helps me justify why transformer-based detectors and ensemble approaches are good candidates for detecting bot-generated comments in my thesis. It also gives me a clear picture of how different types of detectors compare and what evaluation metrics are typically used, which I can use when designing and reporting my own experiments.

*(Duplicate this block as you discover new literature throughout the course)*

------------------------------------------------------------------------

## 3. Generative AI & Digital Tool Transparency Log

In line with academic integrity policies, any use of digital tools (AI search engines, LLMs, translation, or advanced editing software) to support your research process must be declared below. **Note: Using AI to write your final text from scratch is prohibited. Using tools for brainstorming, search, or copy-editing must be documented.**

| Date | Tool Used (e.g., ChatGPT, Elicit, Claude) | Task Performed (e.g., Literature search, refining a sentence, brainstorming variables) | The Exact Prompt or Input Query Used | How you critically evaluated/modified the output before using it |
|:--------------|:--------------|:--------------|:--------------|:--------------|
|  |  |  |  |  |

------------------------------------------------------------------------

## 4. Weekly Activity & Reflection Logs

Update this section at the end of *every* week. Keep reflections concise, focusing on **actions taken**, **obstacles hit**, and **next steps**.

### Week 01: Focus Area - [Topic Selection]

- **Activities Completed:**
  - [Item 1]
  - [Item 2]
- **Key Insights / Discoveries:**
- **Obstacles Encountered & How You Overcame Them:**
- **Plan for Next Week:**

- **Activities Completed:**
  - Reviewed module brief and requirements for the digital research notebook.
  - Brainstormed broad thesis ideas around AI-assisted detection of fake and hateful comments.

- **Key Insights / Discoveries:**
  - A narrower, model-comparison thesis is more feasible than a broad “AI vs fake/hate comments” topic.
  - The area of toxic comment and hate speech detection is active, with many recent papers comparing different NLP models.

- **Obstacles Encountered & How You Overcame Them:**
  - Initial difficulty in defining a precise research question, resolved by reviewing existing work on toxic comment classification and aligning with module expectations.

- **Plan for Next Week:**
  - Finalise the definition of “toxic and hateful comments” and target platform(s).
  - Identify 3–5 key papers on toxic comment and hate speech detection to evaluate.

### Week 02: Focus Area - [e.g., Refining the Research Question]
- **Activities Completed:**
  - Decided to move the focus from toxic/hateful human comments to bot‑ or AI‑generated comments, still within the context of online platforms.
  - Spoke with a student in the year ahead who had built a classifier for transphobic strings, to get a feel for the sort of dataset size, features, and evaluation they used.
  - Picked two core sources on machine‑generated text detection, the SemEval‑2024 SCaLAR paper on RoBERTa ensembles and the Purdue MSc thesis on ensemble and GAN‑based approaches.

- **Key Insights / Discoveries:**
  - There are now shared tasks and thesis projects specifically focused on spotting machine‑generated text from different models, which gives me concrete baselines and methods to learn from.
  - Transformer models and ensemble approaches seem to be strong options for this kind of detection problem, and there are clear ways to compare them against more traditional ML pipelines.
  - Hearing about the transphobic string classifier reassured me that focused comment/text classification projects are doable within the scope of the MSc.

- **Obstacles Encountered & How You Overcame Them:**
  - I was unsure at first whether changing direction part‑way through the module would cause problems, but documenting the pivot clearly in the log and keeping the topic within “AI for online content moderation” helped justify the change.
  - It took some searching to find work specifically on bot comments and machine‑generated text, so I broadened my search terms (e.g. “machine‑generated text detection”, “transformer ensemble text detector”) until I found suitable papers.

- **Plan for Next Week:**
  - Finish reading the SemEval paper and the Purdue thesis properly and update my notes with more detail from the methods and results sections, and continue finding relevant papers for my research question and topic
  - Ask questions: How many papers are we expected to find by the end of the module?
  Do you also want us to add our latex thesis and continuosly update that as well?


*(Continue adding weekly blocks as the module progresses)*

[**NOTE:**]{.underline} Make sure to regular commits to the GitHub repository as the research notebook is updated. These commits will also form part of the evaluation of your work.
