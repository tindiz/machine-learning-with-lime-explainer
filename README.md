# Explaining Machine Learning Classifiers using LIME

This repository contains two notebooks, each containing a machine learning project:

- YouTube spam filter: develops an ML model for Tubespam dataset which can be found on the link: [YouTube Spam Collection Data Set](https://archive.ics.uci.edu/ml/datasets/YouTube+Spam+Collection). The model used for classification is AdaBoost.
- Sentiment analysis: develops an ML model for Multi-Domain Sentiment Dataset (version 2.0) which can be found on the link: [Multi-Domain Sentiment Dataset](https://www.cs.jhu.edu/~mdredze/datasets/sentiment/). The model used for classification is Random Forrest Classifier.


Both classifiers are explained using LIME. Lime is based on the work presented in [this paper](https://arxiv.org/abs/1602.04938) ([bibtex here for citation](https://github.com/marcotcr/lime/blob/master/citation.bib)).
Lime is able to explain any black box classifier, with two or more classes. All we require is that the classifier implements a function that takes in raw text or a numpy array and outputs a probability for each class. Support for scikit-learn classifiers is built-in.

## What are explanations?

Intuitively, an explanation is a local linear approximation of the model's behaviour.
While the model may be very complex globally, it is easier to approximate it around the vicinity of a particular instance.
While treating the model as a black box, we perturb the instance we want to explain and learn a sparse linear model around it, as an explanation.
This repository also contains a summary for the LIME explainer.

## References

Alberto, T.C., Lochter J.V., Almeida, T.A. TubeSpam: Comment Spam Filtering on YouTube. Proceedings of the 14th IEEE International Conference on Machine Learning and Applications (ICMLA'15), 1-6, Miami, FL, USA, December, 2015.

T.A. ALMEIDA, T.P. SILVA, I. SANTOS and J.M. GOMEZ HIDALGO. Text Normalization and Semantic Indexing to Enhance Instant Messaging and SMS Spam Filtering. Knowledge-Based Systems, Elsevier, 108(2016), 25-32, 2016.

John Blitzer, Mark Dredze, Fernando Pereira. Biographies, Bollywood, Boom-boxes and Blenders: Domain Adaptation for Sentiment Classification. Association of Computational Linguistics (ACL), 2007.

[arXiv:1602.04938 [cs.LG]](https://doi.org/10.48550/arXiv.1602.04938)
