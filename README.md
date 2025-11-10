# Protein Family Downloader and Analyzer (UniProt API)

## Description
This Python script automatically downloads protein sequences from the **UniProt API**, cleans them according to length and quality criteria, and performs a comprehensive physicochemical analysis using **Biopython**.  
It computes key properties such as molecular weight, isoelectric point, aromaticity, instability index, hydrophobicity (GRAVY), and secondary structure fractions.  
Finally, it generates summary statistics and visualizations for the analyzed protein family.

## Features
-  Fetch sequences directly from the **UniProt REST API**  
-  Automatic filtering (length, fragments, non-standard amino acids)  
-  Calculate physicochemical descriptors using **Bio.SeqUtils.ProtParam**  
-  Visualize protein length, pI, instability, and amino acid composition  
-  Outputs detailed statistics in both terminal and plots  

## Parameters
You can modify these user parameters in the script:
```python
QUERY = 'family:"kinase" AND reviewed:true'
MAX_SEQS = 500
MIN_LEN = 50
MAX_LEN = 2000
REMOVE_FRAGMENTS = True
REMOVE_WITH_X = True
The script will:

Request sequences from UniProt (based on the query).

Clean and filter the FASTA records.

Analyze each protein sequence.

Display statistical summaries and multiple plots:

Protein Length Distribution

Isoelectric Point Distribution

Instability Index Boxplot

Average Amino Acid Composition
