# exploring_nlp

## Notes

free text document can be seen as a group of features *x* = (*x<sup>0</sup>*, *x<sup>1</sup>*,...,*x<sup>i</sup>*)

*d* = document

*x<sup>i</sup>* = TF(*i*, *d*)\*IDF(*i*)

TF(*i*, *d*) = term frequency = the number of times the term *i* occurs in the document *d*. 

IDF(*i*) = log(*N*/*n<sub>i</sub>*) = Inverse Document Frequency

*N* = Total number of documents in a collection

*n<sub>i</sub>* = number of documents that contain term *i*

because *d* can be different lengths we want to normalize the vector *x* to Euclidean length 1, dividing the feature value by the Euclididan length of the original vector.

 ||*x*|| = sqrt(*x*\**x*)

**Binary Text Classification problem** - If there are exactly two classifications (spam/non-spam)

**Multi-class Problem** - More than two classifications (positive/neutral/negative) and each document falls into exactly one class.

**Multi-label Problem** - Where a document could belong to multiple classifications

Multi-class and label problems are generally reduced to binary problems.

 A training sample of classified documents for a binary classification = S={(x<sub>1</sub>,y<sub>1</sub>),…,(x<sub>n</sub>,y<sub>n</sub>)}

*n* = the number of training examples

*y<sub>i</sub>* ∈ {-1, +1} = the class label of the respective document

Risk = *R(h)* = *∫L(h(x),y)dP(x,y)*

*L(h(x), y)* is a loss function that returns a value of how bad it is if the rule predicts *h(x)* while the true label is *y*

---

Simple Classifiers:

    Naive Bayes
    Logistic Regression
    Decision Trees
    Neural Networks

Sequence Models:

    Hidden Markov Models
    Maximum Entropy Markov Models
    Conditional Random Fields
    Recursive Neural Netowrks (RNNs, LSTMs)

## Resources

[Text classification and Naive Bayes](https://nlp.stanford.edu/IR-book/html/htmledition/text-classification-and-naive-bayes-1.html)

[Introduction to Information Retrieval](https://nlp.stanford.edu/IR-book/html/htmledition/irbook.html)

[Text categorization](http://www.scholarpedia.org/article/Text_categorization)

[CS 124: From Languages to Information](http://web.stanford.edu/class/cs124/)

[Write a Spelling Corrector](http://norvig.com/spell-correct.html)