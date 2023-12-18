A trigram model is a type of probabilistic language model used in natural language processing and computational linguistics. It's a specific case of n-gram model, where "n" represents the number of words or characters considered together as a unit. In the case of a trigram model, "n" is equal to 3, meaning that the model looks at sequences of three consecutive words in a text.

The trigram model is based on the assumption that the probability of a word depends only on the previous two words. It estimates the probability of the next word in a sequence given the two preceding words. This model is trained on a large corpus of text data to learn the likelihood of different word combinations.

The probability of a trigram (W1, W2, W3) occurring is typically calculated as:

\[ P(W3 | W1, W2) = \frac{Count(W1, W2, W3)}{Count(W1, W2)} \]

Here, \( Count(W1, W2, W3) \) is the number of occurrences of the trigram (W1, W2, W3) in the training corpus, and \( Count(W1, W2) \) is the number of occurrences of the bigram (W1, W2).

Trigram models are used in various natural language processing tasks such as language modeling, text generation, and machine translation. While trigram models capture some aspects of language structure and context, they are limited by the fact that they only consider a small context window, and more advanced models, like neural language models, have since been developed to capture longer-range dependencies and semantic relationships in text.