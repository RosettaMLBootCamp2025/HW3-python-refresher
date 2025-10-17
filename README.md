# HW3: Python Refresher

## Overview

This assignment is designed as a Python refresher for biologists and bioinformaticians who may be a bit rusty. You'll complete a series of small exercises that build up to creating a simple sequence analysis tool. This assignment should take approximately 30-45 minutes to complete.

You will:
1. Practice basic Python fundamentals
2. Write functions for biological sequence analysis
3. Read and parse FASTA files
4. Combine everything into a sequence analysis tool

## Prerequisites

- HW1 completed (Python environment set up)

## Instructions

Complete the exercises in order. Each Python file has TODO comments indicating what you need to implement.

### Part 1: Python Basics Warmup (basics.py)

Open `basics.py` and complete the exercises:
- Write a function to reverse a string
- Use a for loop to count characters in a string
- Create a dictionary to count nucleotide frequencies
- Use a list comprehension to filter sequences

**To test your work:**
```bash
conda activate bootcamp2025_HW1
python basics.py
```

### Part 2: Sequence Utilities (sequence_utils.py)

Open `sequence_utils.py` and implement these bioinformatics functions:
- `reverse_complement(dna_seq)` - Returns the reverse complement of a DNA sequence
- `translate_codon(codon)` - Translates a single codon to an amino acid
- `gc_content(seq)` - Calculates the GC percentage of a sequence
- `find_motif(seq, motif)` - Finds all positions of a motif in a sequence

**To test your work:**
```bash
python sequence_utils.py
```

### Part 3: FASTA File Parsing (read_fasta.py)

Open `read_fasta.py` and implement:
- A function to read and parse a FASTA file
- Store sequences in a dictionary (header → sequence)
- Print basic statistics about the sequences

**To test your work:**
```bash
python read_fasta.py sample.fasta
```

### Part 4: Sequence Analysis Tool (analyze_sequence.py)

Open `analyze_sequence.py` and create a complete analysis script that:
- Imports your `sequence_utils` module
- Uses your FASTA parsing function
- Analyzes all sequences in the file
- Writes results to an output file (`analysis_results.txt`)

**To run your analysis:**
```bash
python analyze_sequence.py sample.fasta
```

This should create an `analysis_results.txt` file with your results.

## Submission

Once you've completed all exercises and generated the output file, commit your work:

```bash
# Add all your completed Python files and the output
git add basics.py sequence_utils.py read_fasta.py analyze_sequence.py analysis_results.txt

# Commit your work
git commit -m "Complete Python refresher exercises"

# Push to GitHub
git push
```

## Tips

- **Test frequently**: Run your code after each function to catch errors early
- **Use print statements**: Debug by printing intermediate values
- **Read the TODO comments carefully**: They contain hints and requirements
- **Don't worry about edge cases**: Focus on getting the basic functionality working
- **Ask for help**: If you're stuck, reach out!

## Expected Output

When you run `analyze_sequence.py`, you should see output similar to:

```
Analyzing sequences from sample.fasta...

Sequence: gene_example_1
  Length: 120 bp
  GC Content: 45.83%
  Reverse Complement: CGATCG...

Results written to analysis_results.txt
```

## Questions?

If you run into any issues or have questions, contact Ian at: **icanderson@ucdavis.edu**
