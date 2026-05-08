# NLP-POS-Tagging-for-Indian-Language
### Hindi POS Tagging using NLTK and CoNLL-U Dataset

A Hindi Part-of-Speech (POS) Tagging system built using Python, NLTK, and Indic NLP Library.
This project trains Unigram, Bigram, and Trigram taggers on the Hindi Universal Dependencies (UD) dataset in CoNLL-U format.



## 📌 Project Overview

This project performs:

* Hindi text tokenization
* POS tagging
* Statistical NLP modeling
* N-gram based contextual tagging
* Accuracy evaluation

The model predicts grammatical categories such as:

| Word  | POS Tag |
| ----- | ------- |
| राम   | PROPN   |
| स्कूल | NOUN    |
| जाता  | VERB    |



## 🚀 Features

* ✅ Hindi language support
* ✅ CoNLL-U dataset parser
* ✅ Unigram, Bigram, Trigram taggers
* ✅ Backoff tagging mechanism
* ✅ Interactive sentence tagging
* ✅ Accuracy evaluation
* ✅ Simple and lightweight implementation


## 🛠 Technologies Used

| Technology                     | Purpose              |
| ------------------------------ | -------------------- |
| Python                         | Programming Language |
| NLTK                           | NLP and POS Tagging  |
| Indic NLP Library              | Hindi Tokenization   |
| Universal Dependencies Dataset | Training Data        |


## 📂 Project Structure

```bash
Hindi-POS-Tagger/
│
├── hi_hdtb-ud-train.conllu
├── hi_hdtb-ud-test.conllu
├── pos_tagger.py
├── README.md
└── requirements.txt
```



## 📦 Installation

## 1️⃣ Clone Repository

```bash
git clone https://github.com/raje2004/NLP-POS-Tagging-for-Indian-Language.git

cd NLP-POS-Tagging-for-Indian-Language
```



## 2️⃣ Install Dependencies

```bash
pip install nltk indic-nlp-library
```


## 3️⃣ Download NLTK Resources

```python
import nltk
nltk.download('punkt')
```


## 📥 Dataset

This project uses the Hindi Universal Dependencies dataset.

Dataset files:

* `hi_hdtb-ud-train.conllu`
* `hi_hdtb-ud-test.conllu`

You can download them from:

[Universal Dependencies](https://universaldependencies.org/?utm_source=chatgpt.com)


### 📌 What is CoNLL-U?

CoNLL-U is a standard NLP dataset format used in Universal Dependencies.

Each word contains:

* Word
* POS tag
* Dependency relation
* Grammar features

Example:

```text
1	राम	_	PROPN	NNP	_	2	nsubj	_	_
2	स्कूल	_	NOUN	NN	_	3	obj	_	_
3	जाता	_	VERB	VM	_	0	root	_	_
```


# ⚙ How the Project Works

## Pipeline

```text
Dataset → Parsing → Training → Evaluation
        → Tokenization → POS Prediction
```


## Step 1: Parse Dataset

The parser extracts:

* Words
* POS tags

from CoNLL-U files.

Example output:

```python
[
 [('राम', 'PROPN'),
  ('स्कूल', 'NOUN'),
  ('जाता', 'VERB')]
]
```


## Step 2: Train Taggers

The project trains:

* DefaultTagger
* UnigramTagger
* BigramTagger
* TrigramTagger

### Backoff Chain

```text
Trigram → Bigram → Unigram → Default
```

This improves prediction accuracy.


## Step 3: Evaluate Model

Accuracy is tested using the test dataset.

Example:

```text
Unigram Accuracy : 90%
Bigram Accuracy  : 93%
Trigram Accuracy : 95%
```


## Step 4: Predict POS Tags

Input:

```text
राम स्कूल जाता है।
```

Output:

```text
राम/PROPN स्कूल/NOUN जाता/VERB है/AUX
```


## ▶ Usage

Run the script:

```bash
python pos_tagger.py
```


## 🧪 Sample Predictions

## Example 1

Input:

```text
दो आदमी आए।
```

Output:

```text
दो/NUM आदमी/NOUN आए/VERB ।/PUNCT
```


## Example 2

Input:

```text
भारत एक महान देश है।
```

Output:

```text
भारत/PROPN एक/DET महान/ADJ देश/NOUN है/AUX
```


## 💬 Interactive Mode

Enable interactive tagging:

```python
interactive_mode()
```

Then type:

```text
>>> राम बाजार गया।
```

Output:

```text
राम/PROPN बाजार/NOUN गया/VERB ।/PUNCT
```

Type `exit` to quit.

---

## 📊 NLP Concepts Used

* Tokenization
* POS Tagging
* N-grams
* Statistical NLP
* Backoff Models
* Universal Dependencies


## 📈 Future Improvements

Possible upgrades:

* Hidden Markov Models (HMM)
* Conditional Random Fields (CRF)
* BiLSTM POS Tagger
* Transformer-based tagging
* GUI/Web Interface
* Marathi and multilingual support


## 🎯 Applications

* Machine Translation
* Chatbots
* Grammar Checking
* Search Engines
* Voice Assistants
* Speech Recognition


## 📸 Sample Output

```text
📂 Loading dataset...
✔ Train sentences: 13304
✔ Test sentences: 1684

⚙ Training taggers...
✔ Training complete!

📊 Evaluating model...

Unigram Accuracy : 91.25%
Bigram Accuracy  : 93.40%
Trigram Accuracy : 94.10%

🧪 Sample Predictions:

Input : राम स्कूल जाता है।
Output: राम/PROPN स्कूल/NOUN जाता/VERB है/AUX ।/PUNCT
```


## 👨‍💻 Author

Raj Wagh


## 📜 License

This project is open-source and available under the MIT License.
