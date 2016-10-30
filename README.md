# [Initial commit under construction] Portuguese Words Analogy

Word embeddings are useful for a variety of NLP tasks, from the classic Part-of-speech to the state of the art machine translation. There are several word embeddings techniques, like [Word2Vec](https://papers.nips.cc/paper/5021-distributed-representations-of-words-and-phrases-and-their-compositionality.pdf) or [GloVe](http://nlp.stanford.edu/projects/glove/), but since they usually have an unsupervised training, evaluating the embeddings quality can be a challenge and depend on the problem to be solved.

[Analogical reasoning](https://www.tensorflow.org/versions/r0.11/tutorials/word2vec/index.html#evaluating-embeddings-analogical-reasoning) is a common way to measure how the learned embeddings are able to capture syntactic and semantic relationships between words and was first introduced by [Mikolov et al](http://msr-waypoint.com/en-us/um/people/gzweig/Pubs/NAACL2013Regularities.pdf). The classical example is: `king is to queen as man is to x`, where a good embedding would predict `x = woman`.

For the English language, a [commonly used file](http://download.tensorflow.org/data/questions-words.txt) has thousands of those relations, and it has been accepted as a standard test throughout the community. This repository contains similar relations for the Portuguese (BR) language. The majority of the relations come from the [original English file](http://download.tensorflow.org/data/questions-words.txt) translated automatically by [Google Translate](https://translate.google.com/). The results were manually curated by removing multiple-words translations and/or invalid translations into Portuguese.

Under the `./relations/` directory, one can find simply `x is to y` relations separated into files under certain categories. Run the `./build-questions-words.py` to build a single `questions-words-pt.txt` file with the complete `x is to y as w is to z` relations.

Feel free to contribute and expand our base :)

## Relations
The files under `./relations/` are organized as follows:

| File                                 | Relation                            | Example             |
| ------------------------------------ | ----------------------------------- |-------------------- |
| `capital-common-countries-pt.txt`    | A common capital and country        | Berlim Alemanha     |
| `capital-world-pt.txt`               | A less common capital and country   | Accra Ghana         |
| `city-in-us-state-pt.txt`            | A capital and US state              | Dallas Texas        |
| `family-pt.txt`                      | Family and relationship gender wise | marido esposa       |
| `gram1-adjective-to-adverb-pt.txt`   | Adjective and adverb                | calmo calmamente    |
| `gram2-opposite-pt.txt`              | Opposites                           | feliz infeliz       |
| `gram3-comparative-pt.txt`           | Adjective and comparatives          | pequeno menor       |
| `gram4-superlative-pt.txt`           | Adjective and superlatives          | bom melhor          |
| `gram5-gerund-pt.txt`                | Verb and gerund                     | voar voando         |
| `gram6-nationality-adjective-pt.txt` | Country and nationaly               | Dinamarca dinarquês |
| `gram7-past-tense-pt.txt`            | Verb and past tense                 | ir foi              |
| `gram8-plural-pt.txt`                | Nouns and plurals                   | dedo dedos          |
| `gram9-plural-verbs-pt.txt`          | Verbs and present tense plural      | vai vão             |