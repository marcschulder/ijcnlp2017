# Bootstrapped Lexicon of English Verbal Polarity Shifters
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3364811.svg)](https://doi.org/10.5281/zenodo.3364811)

This repository contains the data created as part of:

[Marc Schulder](http://marc.schulder.info), [Michael Wiegand](http://www.coli.uni-saarland.de/~miwieg/), [Josef Ruppenhofer](http://ruppenhofer.de/) and [Benjamin Roth](https://sites.google.com/site/rothbenj/) (2017). [**"Towards Bootstrapping a Polarity Shifter Lexicon using Linguistic Features"**](https://aclweb.org/anthology/I17-1063). Proceedings of the 8th International Joint Conference on Natural Language Processing (IJCNLP), pages 624–633, Taipei, Taiwan, 27 November – 3 December 2017.

## Content
We provide a bootstrapped lexicon of English verbal polarity shifters.
Our lexicon covers 3043 verbs of [WordNet](https://wordnet.princeton.edu/) v3.1 (Miller et al., 1990) that are single word or particle verbs.
Polarity shifter labels are given for each word lemma.

### Resources
- **Paper:** [ACL Anthology](https://aclweb.org/anthology/I17-1063)
- **Presentation:** [ACL Anthology](https://www.aclweb.org/anthology/attachments/I17-1063.Presentation.pdf)
- **Data:** See content of this repository
- **Word Embedding:** [![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.3370051.svg)](https://doi.org/10.5281/zenodo.3370051)



#### Related Resources
- **[Polarity Shifter Resources](https://github.com/uds-lsv/polarity-shifter-resources)**
  - **[LREC 2018](https://github.com/uds-lsv/lexicon-of-english-verbal-polarity-shifters):** Lexicon of English Verbal Shifters (manual, sense-level)
  - **[COLING 2018](https://github.com/uds-lsv/bootstrapped-lexicon-of-german-verbal-polarity-shifters):** Lexicon of German Verbal Shifters (bootstrapped, lemma-level)
  - **[LREC 2020](https://github.com/uds-lsv/lexicon-of-polarity-shifting-directions):** Lexicon of Polarity Shifting Directions (supervised classification, lemma-level).
  - **[JNLE 2020](https://github.com/uds-lsv/bootstrapped-lexicon-of-english-polarity-shifters):** General Lexicon of English Shifters (bootstrapped, lemma-level).
- **[Word Embedding of Amazon Product Review Corpus](https://doi.org/10.5281/zenodo.3370051):** Word2Vec word embedding used to create this data.

# Data
The data consists of:
1. Two lists of WordNet verbs (Miller et al., 1990), annotated for whether they cause shifting.
    1. The initial gold standard (§2) of 2000 randomly chosen verbs.
    2. The bootstrapped 1043 verbs (§5.3) that were labelled as shifters by our best classifier and then manually annotated.
2. Data set of verb phrases from the Amazon Product Review Data corpus (Jindal & Liu, 2008), annotated for polarity of phrase and polar noun.


## 1. Verbal Shifters
### Files
  - The initial gold standard: `verbal_shifters.gold_standard.txt`
  - The bootstrapped verbs: `verbal_shifters.bootstrapping.txt`

### Format
- Each line contains a verb and its label, separate by a whitespace.
- Multiword expressions are separated by an underscore (WORD_WORD).
- All labels were assigned by an expert annotator.

## 2. Sentiment Verb Phrases
### Files
- All annotated verb phrases: `sentiment_phrases.txt`

### Content
The file starts with 400 phrases containing shifter verbs, followed by 2231 phrases containing non-shifter verbs.
### Format
Every item consists of:
- The sentence from which the VP and the polar noun were extracted.
- The VP, polar noun and the verb heading the VP.
- Constituency parse for the VP.
- Gold labels for VP and polar noun by a human annotator.
- Predicted labels for VP and polar noun by RNTN tagger (Socher et al., 2013) and `LEX_gold` approach.
- Items are separated by a line of asterisks (*)

## Attribution
This data set is published under [Creative Commons Attribution 4.0](https://github.com/uds-lsv/bootstrapped-lexicon-of-english-verbal-polarity-shifters/blob/master/LICENSE).

If you use it in your research or work, please cite the publication (see above).

### BibTex
```
@inproceedings{schulder2017shifter,
  title={Towards Bootstrapping a Polarity Shifter Lexicon using Linguistic Features},
  author={Schulder, Marc and Wiegand, Michael and Ruppenhofer, Josef and Roth, Benjamin},
  booktitle={Proceedings of the Eighth International Joint Conference on Natural Language Processing},
  year={2017},
  publisher={Asian Federation of Natural Language Processing},
  volume={1},
  pages={624--633},
  address={Taipei, Taiwan},
  url={http://aclweb.org/anthology/I17-1063}
}
```

## Acknowledgements
This work was partially supported by the German Research Foundation (DFG) under grants RU 1873/2-1 and WI4204/2-1.

## References
G. Miller, R. Beckwith, C. Fellbaum, D. Gross, K. Miller: "Introduction to WordNet: An On-Line Lexical Database". International Journal of Lexicography, 3:235-244, 1990.

N. Jindal and B. Liu: "Opinion Spam and Analysis", in Proceedings of ACM-WSDM, 2008.

R. Socher, A. Perelygin, J. Wu, J. Chuang, C. Manning, A. Ng, C. Potts: "Recursive Deep Models for Semantic Compositionality Over a Sentiment Treebank", in EMNLP, 2013.
