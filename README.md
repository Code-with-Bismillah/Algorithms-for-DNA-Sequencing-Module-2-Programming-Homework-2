# Algorithms-for-DNA-Sequencing-Module-2-Programming-Homework-2

## Overview

This project implements and compares several algorithms for DNA sequence analysis, focusing on exact and approximate pattern matching. The algorithms include:

- Naive String Matching (with alignment and comparison counts)
- Boyer-Moore String Matching (with alignment and comparison counts)
- Approximate Matching using k-mer Index
- Approximate Matching using Subsequence Index

The code is designed to analyze DNA sequences, such as those found in the human genome, and answer questions about the efficiency and accuracy of different matching strategies.

## File Structure

- `home-work2.ipynb`: Main Jupyter notebook containing code, explanations, and results.
- `bm_preproc.py`: Boyer-Moore preprocessing and helper functions.
- `kmer_index.py`: Implementation of a simple k-mer index for fast substring search.
- `kmer_subseq_index.py`: Implementation of a subsequence index for approximate matching.
- `chr1.GRCh38.excerpt.fasta`: Example FASTA file containing a DNA sequence excerpt.
- `README.md`: Project documentation (this file).

## Requirements

- Python 3.x
- Jupyter Notebook (for running `.ipynb` files)

No external packages are required beyond the Python standard library.

## Setup Instructions

1. **Clone the repository** (if not already done):

   ```bash
   git clone <repository-url>
   cd Algorithms-for-DNA-Sequencing-Module-2-Programming-Homework-2
   ```

2. **Ensure all files are present**:
   - `home-work2.ipynb`
   - `bm_preproc.py`
   - `kmer_index.py`
   - `kmer_subseq_index.py`
   - `chr1.GRCh38.excerpt.fasta`

3. **Launch Jupyter Notebook**:

   ```bash
   jupyter notebook
   ```

4. **Open and run `home-work2.ipynb`** to see code, explanations, and results.

## Algorithm Descriptions

### 1. Naive String Matching

- Compares the pattern to every possible position in the text.
- Counts the number of alignments tried and character comparisons made.
- Simple but inefficient for large texts.

### 2. Boyer-Moore String Matching

- Uses preprocessing (bad character and good suffix rules) to skip sections of the text.
- More efficient than naive matching, especially for long patterns and large alphabets.
- Counts alignments and character comparisons for performance analysis.

### 3. Approximate Matching with k-mer Index

- Splits the pattern into segments and uses a k-mer index to find candidate matches.
- Allows for a specified number of mismatches (Hamming distance).
- Efficient for finding approximate matches in large genomes.

### 4. Approximate Matching with Subsequence Index

- Uses a subsequence index to find matches allowing for mismatches and gaps.
- Useful for more flexible approximate matching scenarios.

## How to Use

- Modify the pattern or text in the notebook as needed.
- Run each cell to execute the algorithms and view the results.
- The notebook prints the number of alignments, character comparisons, and matches found for each method.

## References

- [Bioinformatics Algorithms: An Active Learning Approach](https://www.bioinformaticsalgorithms.org/)
- Gusfield, D. (1997). Algorithms on Strings, Trees, and Sequences.

## License

This project is for educational purposes.