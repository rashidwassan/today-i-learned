# Natural Language Processing

## Introduction:
- A subfield of Artificial Intelligence (AI) that deals with the processing of Natural Language.
- Also called Computational Linguistics.
- Natural Language Processing (NLP) is the use of computers to process written and spoken language for some practical, useful, purpose: to translate languages, to get information from the web on text data banks so as to answer questions, to carry on conversations with machines, so as to get advice about, say, pensions and so on.

## Application Areas
- Machine Translation
- Text Summarization
- User Interfaces
- Speech Recognition
- Spelling and Grammar Checkers
- Natural Language Interfaces

## Divisions
- Processing Written Text
- Processing Spoken Language

## Subfields
- Natural Language Generation: It is the area of NLP concern with making it easier for you to understand a computer output.
- Natural Language Understanding: Concerned with the understanding of knowledge specified in Natural Language such that the computer can use it to perform it tasks.

## Features that make it difficult or useful
- `The problems:`
  - Sentences may have incomplete meaning.
  - Different contextual meanings.
  - No complete knowledge as new words being formed.
  - Lot of ways to say something.
- `Good side:`
  - Allows speakers to be vague or precise.
  - Talking about infinite world using finite words.
  - Can evolve as our experience.
  - When you know a lot,, facts implies easily to each other.

## Other Problems in NL Understanding
- `Ambiguity: `Lexical, Syntactic, and Referential.
- `Imprecision`
- `Incompleteness`
- `Inaccuracy`

## Parsing
In this process sentence is converted into a hierarchical structure that corresponds to the units of meaning in the sentence.
## Working of a parser
- Identification of noun and verb phrases and their breakdown.
- Syntactic analysis.
- These noun and verb phrases are further broken down for extraction of meaning.

## Lexicon
- Word bank
- Contains all the recognizable words
- Parser works closely with Lexicon
- Contains correct spellings of words

## Understander and Knowledge base
- Understander performs semantic analysis
- Understander works in conjunction with the knowledge base to determine what the sentence means.
- The knowledge base is the primary means of understanding.

## Generator
- The generator uses the understood input to create a usable output.
- In DBMS, the generator would write a program in a query language to begin a search for specific information.

## N-Gram
- A subsequence of n items from a given sequence
  - Unigram: N-Gram of Size 1
  - Bigram: N-Gram of Size 2
  - Trigram: N-Gram of Size 3
- Items:
  - Phonemes
  - Syllables
  - Letters
  - Words
- Example: Bigram: 'A bird'

## N-Gram Model
- A Probabilistic Model for Predicting the next Item in such a sequence.
- Why do we want to Predict Words? for different software.
- Predicts xi based on xi – 1, xi – 2 , ..., xi – n:
- NGram Independence Assumption:
  - word is affected only by its “prior local context” (last few words)

## Morphology
- Morphology is the study of the internal structure of words, of the way words are built up from smaller meaning units.