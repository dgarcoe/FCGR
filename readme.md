# Frequency Chaos Game Representation

Frequency Chaos Game Representation (FCGR), an extension of Chaos Game Representation (CGR), is a reliable method for encoding DNA sequences.

## Usage

The fcgr Python package offers a wide array of functionalities for generating FCGR matrices and more:

* Read a FASTA file to generate a concatenated DNA sequence.
* Generate the FCGR kmer matrix key based on the specified kmer length.
* Retrieve the position of a *k*-mer within the FCGR key matrix as a tuple.
* Return the *k*-mer of the specified length located at the given index.
* Compute the FCGR matrix for a provided DNA sequence and kmer length using the FCGR kmer key matrix.
* Calculate the frequency of *k*-mers with a specified length in the FASTA file and provide them in dictionary format.
* Obtain the count of the specified *k*-mer within the provided DNA sequence.

## Installation
To install fcgr you must make sure that your python version is 3.10.13+.

### Prerequisites
* pandas = 2.1.4
* numpy = 1.22.4
* biopython = 1.81
* collections = 0.1.6

## Setup
fcgr can be installed with pip as shown below,

```bash
!pip install fcgr-0.1-py3-none-any.whl

```

## fcgr functionality

```bash
fcgr.read_fasta(file_path: str)
```

Reads a FASTA file at the given `file_path` and concatenates the sequences into a single string.

#### Parameters

- `file_path` (str): The path to the FASTA file.

#### Return

- `str`: Concatenated DNA sequence from the FASTA file.

```bash
fcgr.chaos_game_representation_key(kmer_length: int)
```
Generates the key matrix for Frequency Chaos Game Representation (FCGR) for the given *k*-mer length.

#### Parameters

- `kmer_length` (int): The length of the *k*-mer.

#### Returns

- `np.ndarray`: A 2D numpy array representing the key matrix for FCGR.

```bash
fcgr.return_kmer_index(kmer: str)
```
Returns the index of a specific *k*-mer in the Frequency Chaos Game Representation (FCGR) key matrix.

#### Parameters

- `kmer` (str): The *k*-mer for which the index is to be found.

#### Returns

- `tuple`: The row and column indices of the *k*-mer in the CGR key matrix.

```bash
fcgr.return_kmer_at_index(kmer_length: int, tuple_index: tuple)
```
Returns the *k*-mer at the specified index in the Frequency Chaos Game Representation (FCGR) key matrix.

#### Parameters
* kmer_length (int): The length of the *k*-mer used to generate the Frequency Chaos Game Representation (FCGR) matrix.
* tuple_index (tuple): The index (row, column) of the *k*-mer in the matrix.

#### Return
* str: The *k*-mer at the specified index.
  
```bash
fcgr.chaos_frequency_matrix(fasta_string: str, kmer_length: int, chaos_game_kmer_array: np.array = None, pseudo_count: bool = True)
```
Generates the chaos frequency matrix for the given DNA sequence.

This function calculates the Frequency Chaos Game Representation (FCGR) for a given DNA sequence and *k*-mer length, using the FCGR key matrix.

#### Parameters
* fasta_string (str): The DNA sequence in FASTA format.
* kmer_length (int): The length of the *k*-mers to consider.
* chaos_game_kmer_array (np.array, optional): The Frequency Chaos Game Representation (FCGR) key matrix. Defaults to None.
* pseudo_count (bool, optional): Whether to add 1 to each element of the matrix. Defaults to True.

#### Return
* tuple: A tuple containing:
  - np.array: The Frequency Chaos Game Representation (FCGR) representing *k*-mer frequencies.
  - np.array: The Frequency Chaos Game Representation (FCGR) key matrix used.
 
```bash    
fcgr.chaos_frequency_dictionary(fasta_string: str, kmer_length: int, chaos_game_kmer_array: np.array = None, pseudo_count: bool = True)
```
Calculate the frequency dictionary of *k*-mers in a chaos game representation matrix.

#### Parameters
* fasta_string (str): The input DNA sequence in FASTA format.
* kmer_length (int): The length of *k*-mers.
* chaos_game_kmer_array (np.array): Chaos game *k*-mer array if pre-calculated, otherwise None.
* pseudo_count (bool): Whether to add 1 to each element of the matrix. Defaults to True.
#### Returns
* frequency_dictionary (dict): A dictionary containing *k*-mer as keys and their frequencies as values.

```bash   
fcgr.return_kmer_count_individual(key_name: str, fasta_content: str)
```

Calculate the count of a specific *k*-mer in a given DNA sequence.

#### Parameters
* key_name (str): The *k*-mer sequence for which the count is to be calculated.
* fasta_content (str): The input DNA sequence in which the *k*-mer count is to be calculated.

#### Returns
* count (int): The count of the specified *k*-mer in the DNA sequence.



