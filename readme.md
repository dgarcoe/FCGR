# Frequency Chaos Game Representation

Frequency Chaos Game Representation (FCGR), an extension of Chaos Game Representation (CGR), is a reliable method for encoding DNA sequences.

## Usage

The fcgr Python package offers a wide array of functionalities for generating FCGR matrices and more:

* Read a FASTA file to generate a concatenated DNA sequence.
* Generate the FCGR kmer matrix key based on the specified kmer length.
* Retrieve the position of a k-mer within the FCGR key matrix as a tuple.
* Return the k-mer of the specified length located at the given index.
* Compute the FCGR matrix for a provided DNA sequence and kmer length using the FCGR kmer key matrix.
* Calculate the frequency of k-mers with a specified length in the FASTA file and provide them in dictionary format.
* Obtain the count of the specified k-mer within the provided DNA sequence.

## Installation
To install fcgr you must make sure that your python version is 3.10.13+.

### Prerequisites
* pandas = 2.1.4
* numpy = 1.22.4
* biopython = 1.81
* collections

## Setup
fcgr can be installed with pip as shown below,

```bash
!pip install fcgr-0.1-py3-none-any.whl

```

## fcgr functionality


### read_fasta(file_path: str)
Reads a FASTA file at the given `file_path` and concatenates the sequences into a single string.

Parameters
* file_path (str): The path to the FASTA file.
Return
* str: Concatenated DNA sequence from the FASTA file.
