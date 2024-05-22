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

#### Input Arguments

The arguments are as follows:

- `adata_source`: the preprocessed `scanpy.anndata` for the source dataset.
- `save_dir`: name of the directory to save the source model.
- `vec_size`: dimensionality of the embedding vectors. Defaults to 300 for SCellBOW.
- `n_worker`: number of worker threads to train the model. For a fully deterministically-reproducible run, limit the model to one worker thread. Defaults to 1 for SCellBOW.
- `iter`: Number of iterations (epochs) over the corpus. Defaults to 20 for SCellBOW.


