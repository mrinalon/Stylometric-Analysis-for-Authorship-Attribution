# Stylometric Analysis for Authorship Attribution

## Overview

This project performs stylometric analysis using Natural Language Processing (NLP) techniques to attribute authorship of a given text. It leverages various linguistic features such as word length, stopwords, parts of speech, vocabulary, and Jaccard similarity to compare texts from different authors and determine the likely author of an unknown text.

## Features

- Tokenization and preprocessing of text data.
- Analysis of word length frequency.
- Analysis of stopwords frequency.
- Analysis of parts of speech frequency.
- Analysis of vocabulary.
- Jaccard similarity for determining textual similarity.
- Determination of the likely author of an unknown text based on stylometric features.

## Installation

### Prerequisites

- Python 3.7 or higher
- pip

### Required Libraries

Install the required libraries using the following command:

```bash
pip install -r requirements.txt
```

### NLTK Data

Ensure that NLTK data is downloaded by running the following script:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('averaged_perceptron_tagger')
```

## Usage

1. Place the text files (`hound.txt`, `war.txt`, `lost.txt`) in the root directory of the project.
2. Run the script:

    ```bash
    python stylometric_analysis.py
    ```

3. The script will read the text files, perform various stylometric analyses, and output the results, including the likely author of the unknown text.

## Code Explanation

### Functions

- **text_to_string**: Reads a text file and returns its content as a string.
- **make_word_dict**: Tokenizes words by corpus for each author.
- **find_shortest_corpus**: Finds the length of the shortest corpus among the authors.
- **word_length_test**: Analyzes word length frequency.
- **stopwords_test**: Analyzes stopwords frequency.
- **parts_of_speech_test**: Analyzes parts of speech frequency.
- **vocab_test**: Analyzes the most common words.
- **jaccard_test**: Analyzes Jaccard similarity between the unknown text and known authors' texts.
- **determine_author**: Determines the likely author of the unknown text based on Jaccard similarity.

## Project Structure

```
.
├── README.md
├── requirements.txt
├── stylometric_analysis.py
├── hound.txt
├── war.txt
└── lost.txt
```

- `README.md`: This file.
- `requirements.txt`: List of required Python libraries.
- `stylometric_analysis.py`: Script for performing stylometric analysis.
- `hound.txt`: Text file by Arthur Conan Doyle.
- `war.txt`: Text file by H.G. Wells.
- `lost.txt`: Unknown text file for authorship attribution.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributions

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/mrinalon/Stylometric-Analysis-for-Authorship-Attribution/issues) if you want to contribute.

---
