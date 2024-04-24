# Data 195- Final Project 
This repository primarily focuses on the detection and deciphering of Cuneiform languages using machine learning models and natural language processing (NLP) techniques.

## Authors
- Adam Anderson (PI)
- Zizhuo (Tina) Chen
## Project Overview

The primary goal of this project is to accurately translate the Cuneiform languages (e.g. Sumerian, Akkadian, Hittite, etc.), ensuring the preservation of its original meaning, into contemporary languages.
We are employing a comprehensive range of data science techniques, including text classification and advanced natural language processing (NLP) methods such as dependency parsing.
These techniques are pivotal in understanding and interpreting the complex structure of the Cuneiform language. Our methodology involves a systematic data-gathering process.
We utilize a rule-based approach to meticulously segment text from Cuneiform texts, moving from the page level to word and sentence levels. 
This structured approach is essential for the accurate processing and analysis of ancient language data. The overarching aim is to construct dependency parsers for Cuneiform and 
other underrepresented languages. To achieve this, we are leveraging Large Language Models (LLMs), which are highly effective in various linguistic tasks. These models enable us 
to delve deeper into the linguistic nuances of Cuneiform and similar low-resource languages, facilitating a better understanding and more accurate translations into modern languages.

## Directory Structure

This repo contains a few subfolders which contain the elements of this project.

| Folder | Description |
|-----|-----|
| `data`  | data from the original analysis in CSV and pip-separated format  |
| `notebooks`  | Jupyter Notebook files, including reproduction analysis |
| `output`  | output data (same as original, for demo purposes) in CSV format  |
## Data Overview

**Data Structure:**
- The data for this project is meticulously organized and stored in Google Drive. It encompasses over 13,000 files, primarily structured at the page level and categorized based on different books.
- The majority of our data sources are secondary resources. These resources are particularly diverse, containing words from various languages, which adds to the complexity and richness of the dataset.

**Data Challenges:**
- One of the significant challenges we face in this project is the transformation of raw data into a structured format suitable for detailed linguistic analysis. Given the vastness and diversity of the data,
- this process is crucial for ensuring the accuracy and efficacy of our analysis.
- The multi-language nature of the sources necessitates a careful and nuanced approach to data processing to maintain the integrity and context of the original texts.

**Data Analysis Techniques:**
- **Language Detection:** An essential component of our data analysis involves the identification of languages within the texts. This step is critical in understanding the context and meaning of the words in our dataset.
- **Lemmatization:** To facilitate accurate language processing, we employ lemmatization techniques. This helps in reducing words to their base or dictionary form, which is vital for analyzing ancient languages.
- **Computational Analysis:** Our approach includes computational methods to correctly identify and interpret the linguistic structures in the Cuneiform texts.
- **Conversion of Data:** Utilizing the `words.ipynb` notebook, we successfully convert data from page level to word level. This granular level of data processing allows for a more detailed and nuanced analysis.
- **Sentence Segmentation:** Currently, we are segmenting the text into sentences using the `sentences_strict.ipynb` notebook. This segmentation is a critical step in preparing the data for dependency parsing and further linguistic analysis.

The data structure and processing techniques in this project are designed to tackle the unique challenges of working with ancient texts, particularly in the context of low-resource languages like Cuneiform. 
Through these efforts, we aim to construct a comprehensive language model that can effectively translate and interpret these ancient scripts.

## Methodology
### Methodology for the Cuneiform Language System Project
![Dependency_pipeline](https://github.com/czz129/data195_final_project/assets/89886448/0c856266-c56e-4226-b3b6-e6738c09430d)

### Step 1: Data Cleaning and Transformation

#### Collection and Storage:
- Store all files on Google Drive.
- Digitize the raw text data using Optical Character Recognition (OCR).
- Organize the digitized data at the page level, categorizing it based on book chapters.

#### Data Transformation and Standardization:
- Process the OCR outputs by converting texts from page level to word level, assigning each word a unique identifier.

### Step 2: Language Detection

#### Preprocessing Words:
- Correct misprinted words and errors introduced during the OCR process, improving the accuracy and reliability of the textual data.

#### Translation Consistency:
- Statistical hypothesis testing was applied to address and quantify inconsistencies in translations of certain language sequences that appeared in the texts.
- A chi-square test was used to determine if the differences in translation rates between two interpretations (e.g., Sumerian versus Akkadian) were statistically significant.

### Step 3: Sentence Segmentation

#### Data Loading and Pre-processing:
- Identify punctuation marks, join partitioned words, and clean the text to prepare it for segmentation.

#### Segmentation Process:
- Use Neural Network Models to segment the sentence.
- Run a rule-based approach to further segment with regex, a set of rules and conditions designed to accurately determine sentence boundaries.

### Step 4: Language Analysis

#### Construction of Dependency Parsers:
- Development of dependency parsing algorithms to analyze grammatical structures and relationships between words within sentences.

#### Integration with Wikibase Lexicons:
- Utilization of dependency parsers to identify parts of speech and lemmatized tokens, which are then mapped to a Wikibase lexicon.

### Grapheme Level Analysis:
- Normalization, transliteration, and encoding of lexemes into Unicode cuneiform.
- Link signs and lexemes to the Wikidata list.

#### Morphological Annotation:
- Decomposition of word forms and annotation of each lexical category with corresponding Q-items from Wikidata.
- Detailed analysis of verbs, affixes, and their grammatical features to enrich the morphological understanding.

#### Syntactic and Semantic Analysis:
- Construct syntactic mappings to elucidate the roles of subjects and word forms in sentences.
- Semantic analysis through the addition of Q-identifiers as senses to lexemes, establishing connections between lexemes and senses.



## Conclusion
By integrating traditional NLP techniques with advanced language models, this project aims to significantly contribute to the understanding of Cuneiform languages. Our approach balances the use of 
rule-based methods with the innovative application of machine learning, opening new avenues in the field of historical linguistics and ancient language analysis.


[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/czz129/data195_final_project/master)

This project for Data Science Honors program. The purpose of this project is to attempt to reproduce the findings in the original analysis regarding the LLM for Cueniform Text analysis. We will also evaluate the efficacy and reliability of this data set to qualify any conclusions that we draw. For more detailed information, see the [Pre-Analysis Plan].



### MyBinder

You should note that this repository has a MyBinder link (at the top of this README) which links to MyBinder to allow others to run our code. _Your repository should also include such a link._ The steps to create this link are given below:

1. Copy the `requirements.txt` file from this repo and add it to yours. This should cover all dependencies, but if you use any that are not listed in that file, _make sure to add them_.
2. Go to the [MyBinder website](https://mybinder.org/) and paste the URL to your repo in the `GitHub repository name or URL` field (pictured below).
3. Include the brach name in the `Git branch, tag, or commit` field; for most, this will be `master`.
4. Open the dropdown below the Binder URL and copy the text next to the ![Markdown logo](images/markdown.png).
5. Paste this text into your README right below where your names are listed at the top. For our repo, it looked like this:

```markdown
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/czz129/data195_final_project/master)
```
