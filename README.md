# Plagiarism-Detection-LSH


The aim of this project is to detect plagiarism in documents using the concept of Locality Sensitive Hashing (LSH). The principle behind this approach is that documents that are "similar" will be hashed to the same buckets with high probability.

The program takes two sets of documents:
1. Original documents: Excerpts from Wikipedia articles, susceptible to plagiarism.
2. Sample documents: Possibly plagiarised from the Wikipedia articles (original documents), and whose uniqueness will be tested by the LSH algorithm.

The implementation of the algorithm entails the following:

1. Shingles (akin to n-grams) are generated for each original and document document
2. Min-hashing is done to construct a signature matrix that can be used to determine the similarity of documents using Jaccard's distance as the metric. Min-hashing    is done using using a varied number of hash functions
3. Implementation of the LSH algorithm by hashing the documents into B buckets, after separating the signature matrix into b bands of r rows. The false 
    positives/negatives are determined
4. Various combinations of b, r and B are used to obtain optimum results

Using this algorithm, the sample documents that are suspected as having been plagiarised from the original documents, are singled out.
