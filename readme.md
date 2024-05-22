# Frequency Chaos Game Representation

Frequency Chaos Game Representation (FCGR), an extension of Chaos Game Representation (CGR), is a reliable method for encoding DNA sequences.

## Usage

* read a FASTA file and generate a concatenated DNA sequence.

### `chaos_game_representation_key(.)`
This function generates the FCGR kmer matrix key based on the kmer length specified by the user.

### `return_kmer_index(.)`
This function accepts a specific kmer and returns its position within the FCGR key matrix as a tuple.

### `return_kmer_at_index(.)`
This function requires two arguments: `kmer_length` and `tuple_index`. The `kmer_length` specifies the length of the kmer used to form the FCGR matrix, while the `tuple_index` indicates the position of the kmer within the array. The function returns the kmer of the specified length located at the given index.

### `chaos_frequency_matrix(.)`
This function computes the FCGR matrix for a provided DNA sequence and kmer length utilizing the FCGR kmer key matrix. Additionally, it includes an optional boolean parameter called `pseudo_count`. When set to True (default), this parameter adds 1 to each kmer frequency. If set to False, it returns the actual frequency count.

### `chaos_frequency_dictionary(.)`
This function calculates the frequency of \textit{k}-mers with a specified length in the FASTA file and provides them in dictionary format. It has an optional boolean parameter called `pseudo_count`. When set to True (default), this parameter increases each kmer frequency by 1. If set to False, it returns the actual frequency count.

### `return_kmer_count_individual(.)`
This function provides the count of the specified kmer, given in the query, within the provided DNA sequence.


1. The package folder includes all the scripts required for comparative analysis between the proposed Python-based FCGR package and the R-based "kaos" package, documentation notebooks, and a PDF file.

2. To install the package in your Python environment, use: !pip install kaos-0.15-py3-none-any.whl

3. The Motif finding folder contains the notebook for motif classification and the pickle model.
