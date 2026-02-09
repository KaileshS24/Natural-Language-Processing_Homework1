# Natural-Language-Processing_Homework1

#Kailesh Surarapu
#Student Id: 700793540

Q5.1 A Naïve Space-Based Tokenization

text = """Natural language processing is widely used in real-world applications. # Input paragraph
It helps computers understand human language, emotions, and intent.
However, tokenization isn't always straightforward."""

naive_tokens = text.split()  # Naïve tokenization using space split

print("Naïve Tokens:")   # Print tokens
for token in naive_tokens:
    print(token)

Q5.1 B Manual Token Correction

# Manually corrected tokens after linguistic inspection
manual_tokens = [
    'Natural', 'language', 'processing', 'is', 'widely', 'used', 'in',
    'real', 'world', 'applications',
    'It', 'helps', 'computers', 'understand', 'human',
    'language', 'emotions', 'and', 'intent',
    'However', 'tokenization', "isn't", 'always', 'straightforward'
]

print("\nManually Corrected Tokens:")
for token in manual_tokens:
    print(token)

Q5.2 Tokenization using NLTK

import nltk
from nltk.tokenize import word_tokenize

nltk.download('punkt')   # Download tokenizer data (run once)


tool_tokens = word_tokenize(text)  # Tokenize using NLTK

print("\nNLTK Tokens:")
for token in tool_tokens:
    print(token)


Q5.3 Multiword Expressions (MWEs)
Examples
Natural language processing
Real world
Machine learning

Q5.4 Reflection 

Tokenization is difficult because punctuation, contractions, and compound words create ambiguity. Simple space-based tokenization fails to capture linguistic structure. Manual tokenization improves clarity but is not scalable. NLP tools handle language rules better but may split tokens differently depending on their design. Multiword expressions further complicate tokenization because they represent single meanings across multiple words. Overall, tokenization requires balancing simplicity and linguistic accuracy.




5.1 A: Explanation:
.split() separates text only at spaces.
Punctuation stays attached to words (applications).
Hyphenated words remain combined (real-world).
This approach is fast but linguistically weak.

5.1 B : Explanation
Punctuation marks (. ,) are removed.
real-world is split into two meaningful tokens.
The contraction isn't is preserved to retain meaning.
This version is more semantically accurate than naïve tokenization.

5.2 : Explanation
NLTK separates punctuation into tokens
Splits contractions (is + n't)
Designed for grammatical analysis
Output differs from manual tokens    
