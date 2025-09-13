# arabic-offensive-words
List of Arabic offensive, vulgar, slur and profane words

# Introduction: Methodology for Lexicon Collection and Organization

This report details the creation of a comprehensive, categorized lexicon of offensive, vulgar, and slur terms in Arabic. The methodology utilized a novel approach, leveraging the analytical power of Large Language Models (LLMs) to extract specific offensive terms from existing, academically-vetted datasets.

This process ensures the resulting lexicon is grounded in attested examples of toxic language used "in the wild" on social media.

---

## 1. Data Collection: LLM-Based Lexical Extraction

Unlike traditional methods that require manual keyword seeding, our process began with established corpora already annotated for offensive content by human experts.

The workflow was executed as follows:

1.  **Data Sourcing:** We selected several diverse, publicly available datasets covering different dialects and types of offensive language.
2.  **Pre-Filtering:** From these corpora, we isolated and collected *only* the text samples that the dataset creators had already manually labeled as "Offensive," "Hate Speech," or "Misogynistic."
3.  **LLM Extraction:** This filtered dataset of verified toxic text was then fed as context to a Large Language Model (specifically Gemini Pro).
4.  **Prompting:** The LLM was prompted to analyze these thousands of offensive posts and—acting as an expert extractor—identify and list the specific words, phrases, slurs, and curses that caused the posts to be labeled offensive by the original human annotators.

This methodology combines the accuracy of human annotation (at the post level) with the comprehensive analytical speed of an LLM (at the word-extraction level).

---

## 2. Corpora Resources (Data Sources)

The comprehensiveness of the final list is ensured by sourcing data from multiple corpora covering the most widely spoken Arabic dialects (Egyptian and Levantine) and various types of offensive content:

* **Egyptian-Arabic Hate Speech Dataset:** Provided a core set of 8,169 texts (labeled as offensive or hate speech) drawn from social media, focusing specifically on the **Egyptian dialect**.
* **Let-Mi (Levantine Misogyny Dataset):** This crucial dataset offered a large sample of Levantine Arabic (from Twitter) specifically focused on **misogynistic language**, yielding many of the gendered and sexualized insults.
* **Arabic Levantine Hate Speech Detection:** This Kaggle dataset further expanded the inventory of toxic terms used specifically within the **Levantine dialect**.
* **MLMA (Multilingual and Multi-Aspect Hate Speech):** This dataset added breadth by providing a multi-aspect framework for hate speech, moving beyond a single category and capturing diverse forms of offense.

---

## 3. Organization and Taxonomy

The extraction process from these varied sources produced a massive, raw, and highly redundant list of terms. The final step was to process this output into a structured and useful resource.

This involved:

1.  **Consolidation:** Merging all unique terms extracted by the LLM from all four datasets.
2.  **De-duplication:** Identifying and merging dialectal variants, plurals, and feminine/masculine forms of the same root insult (e.g., \`كلب\`, \`كلاب\`, \`كلبة\`).
3.  **Categorization:** Developing a unified **taxonomy** (the categories seen in the final list, such as "Slurs," "Dehumanization (Animal)," "Explicit Profanity," etc.) to logically organize the lexicon. This sorting transforms the raw data from a simple list into an analytical tool that clarifies the *function*, *target*, and *nature* of each offensive term.

---

## 4. Relevant Papers and Corpora References

The datasets used as the foundation for this extraction methodology are publicly available academic resources.

* **Let-Mi:**
    * Samia, H., et al. (2021). "Let-Mi: An Arabic Levantine Twitter Dataset for Misogynistic Language." *Proceedings of the Sixth Arabic Natural Language Processing Workshop (WANLP).*
    * Link: \`https://aclanthology.org/2021.wanlp-1.16/\`

* **MLMA:**
    * Ousidhoum, N., et al. (2019). "Multilingual and Multi-Aspect Hate Speech Analysis." *Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP).*
    * Link: \`https://aclanthology.org/D19-1474/\`

* **Egyptian-Arabic Hate Speech Dataset:**
    * Ibrahim, A. (2022). "Egyptian-Arabic Hate Speech Dataset." *Hugging Face.*
    * Link: \`https://huggingface.co/datasets/IbrahimAmin/egyptian-arabic-hate-speech\`

* **Arabic Levantine Hate Speech Detection:**
    * Hermessi, H. (2022). "Arabic Levantine Hate Speech Detection." *Kaggle.*
    * Link: \`https://www.kaggle.com/datasets/haithemhermessi/arabic-levantine-hate-speech-detection\`
