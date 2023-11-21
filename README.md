# CS50 AI - Sentence Parser
<img src="https://files.oaiusercontent.com/file-ixZILNxe53LGuoGYjsjMIoMW?se=2023-11-21T10%3A50%3A09Z&sp=r&sv=2021-08-06&sr=b&rscc=max-age%3D31536000%2C%20immutable&rscd=attachment%3B%20filename%3De7ed0b16-24b4-4791-95e8-24e0b7cc00c9.webp&sig=r7oXP3/L6o4VG9DPxWR9zqE9/xVcHghytkCAu3kDxzo%3D">

## Overview
This Sentence Parser is a part of the CS50 AI course project. It utilizes Natural Language Processing (NLP) techniques to parse English sentences and extract noun phrase chunks. The parser is built using Python and the Natural Language Toolkit (NLTK) library.

## Installation
Before running the parser, ensure that Python and NLTK are installed on your system. You can install NLTK using pip:

```bash
pip install nltk
```

Additionally, the NLTK package `punkt` is required for tokenizing sentences. If not already installed, you can download it using the following Python commands:

```python
import nltk
nltk.download('punkt')
```

## Running the Parser
To run the parser, navigate to the directory containing the script `parser.py` and execute the following command in your terminal:

```bash
python parser1.py
```

You can input a sentence directly or specify a filename as an argument to read a sentence from a file.

## Functionality
The parser processes English sentences and prints their syntactic structure, followed by the identified noun phrase chunks. Here's an overview of its key functions:

### preprocess
This function converts a sentence into a list of words, transforming all characters to lowercase and removing any word that lacks alphabetic characters.

### np_chunk
`np_chunk` identifies and returns all noun phrase chunks in a sentence's syntax tree. A noun phrase chunk is defined as a subtree labeled "NP" that doesn't contain other noun phrases.

## Grammar Rules
The parser uses context-free grammar (CFG) rules to parse sentences. These rules are defined in the `NONTERMINALS` and `TERMINALS` variables in the script. The `NONTERMINALS` variable includes rules for sentence structure, noun phrases (NP), verb phrases (VP), prepositional phrases (PP), and more. The `TERMINALS` variable defines the lexicon for nouns (N), verbs (V), adjectives (Adj), etc.

## Sample Usage
After running the script and inputting a sentence, the parser will display its syntactic tree structure and list the noun phrase chunks. For example:

Input:
```
Sentence: Holmes sat.
```

Output:
```
        S
   _____|___
  NP        VP
  |         |
  N         V
  |         |
holmes     sat

Noun Phrase Chunks
holmes
```

## Troubleshooting
If you encounter any errors related to NLTK data, such as missing `punkt` tokenizer, follow the installation instructions to download the necessary NLTK packages.

-