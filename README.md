# Question-MCQS-Generator-Using-Machine-learning-NLP

# Introduction:

Our project aims to generate multiple-choice questions (MCQs) using machine learning and natural language processing (NLP) techniques. MCQs are widely used in educational assessments to evaluate students' understanding of a given topic. By automating the generation of MCQs, educators can save time and effort while ensuring the quality and relevance of the questions.



# Part 2:

# code:

# Load English tokenizer, tagger, parser, NER, and word vectors
nlp = spacy.load("en_core_web_sm")

# input text

text = """
The Greek historian knew what he was talking about. The Nile River fed Egyptian civilization for hundreds of years. The Longest River the Nile is 4,160 miles long—the world’s longest river. It begins near the equator in Africa and flows north to the Mediterranean Sea. In the south the Nile churns with cataracts. A cataract is a waterfall. Near the sea the Nile branches into a delta. A delta is an area near a river’s mouth where the water deposits fine soil called silt. In the delta, the Nile divides into many streams. The river is called the upper Nile in the south and the lower Nile in the north. For centuries, heavy rains in Ethiopia caused the Nile to flood every summer. The floods deposited rich soil along the Nile’s shores. This soil was fertile, which means it was good for growing crops. Unlike the Tigris and Euphrates, the Nile River flooded at the same time every year, so farmers could predict when to plant their crops.
"""

num_questions=5

# Process the text with spaCy

doc = nlp(text)

# Extract sentences from the text

sentences = [sent.text for sent in doc.sents]

# Randomly select sentences to form questions

selected_sentences = random.sample(sentences, min(num_questions, len(sentences)))
selected_sentences


# Explanation of the Code:

# Loading Modules:

The code begins by importing necessary modules, including spacy for NLP processing and random for random selection of sentences.

# Loading English Language Model:

It loads the English language model from spaCy (en_core_web_sm) for tokenization, tagging, parsing, named entity recognition (NER), and word vectors.


# Input Text:

The input text contains information about the Nile River, its significance, and characteristics.

# Processing the Text:

The input text is processed using spaCy, which tokenizes the text into words, identifies parts of speech, parses the structure, recognizes named entities, and generates word vectors.

# Extracting Sentences:

The processed text is split into sentences, and each sentence is stored in a list named sentences.
Randomly Selecting Sentences:
Randomly selects a subset of sentences from the list of sentences to form questions. The number of questions to generate is specified by num_questions.


#  Result:
The selected sentences are stored in the selected_sentences list, which will be used to generate MCQs.
