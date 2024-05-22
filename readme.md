# Frequency Chaos Game Representation

Frequency Chaos Game Representation (FCGR), an extension of Chaos Game Representation (CGR), is a reliable method for encoding DNA sequences.

## Usage

* Read a FASTA file and generate a concatenated DNA sequence.
* Generate the FCGR kmer matrix key based on the kmer length specified by the user.
* Return the k-mer position within the FCGR key matrix as a tuple.
* Return the kmer of the specified length located at the given index.
* Compute the FCGR matrix for a provided DNA sequence and kmer length utilizing the FCGR kmer key matrix.
* Calculate the frequency of k-mers with a specified length in the FASTA file and provide them in dictionary format.
* Obtain the count of the specified kmer, given in the query, within the provided DNA sequence.

## Installation
To install fcgr you must make sure that your python version is 3.9 +.


## Setup
fcgr is included in PyPI, so you can install it by

'''a



1. The package folder includes all the scripts required for comparative analysis between the proposed Python-based FCGR package and the R-based "kaos" package, documentation notebooks, and a PDF file.

2. To install the package in your Python environment, use: !pip install kaos-0.15-py3-none-any.whl

3. The Motif finding folder contains the notebook for motif classification and the pickle model.


