# BIOL 432 — Assignment 7: NCBI Sequence Retrieval with Rentrez

This is my Assignment 7 work for **BIOL 432: Computation and Big Data in Biology** at Queen's University.

## What I did

For this assignment I used the `rentrez` package in R to access nucleotide sequence data from the NCBI database. I fetched several *Borrelia burgdorferi* 16S rRNA sequences using their NCBI accession numbers and then processed the FASTA output in R.

I also searched NCBI for additional *B. burgdorferi* 16S sequences and retrieved a reference sequence from the search results.

## Main methods

- R
- `rentrez`
- NCBI Entrez API
- Nucleotide database (`nuccore`)
- FASTA sequence retrieval
- String processing and sequence extraction
- NCBI sequence searching

## What the code does

1. Installs and loads the `rentrez` package.
2. Uses NCBI accession numbers (`HQ433692.1`, `HQ433694.1`, and `HQ433691.1`) to retrieve *B. burgdorferi* nucleotide sequences.
3. Parses the FASTA output to separate sequence headers from the nucleotide sequences.
4. Stores the sequence names and sequences in a data frame.
5. Creates an unknown nucleotide sequence and reports its length.
6. Searches NCBI for *B. burgdorferi* 16S ribosomal RNA sequences.
7. Fetches the top three search results and extracts the first reference sequence and its length.

## Example sequence retrieval

The main NCBI retrieval uses:

```r
NcbiIds <- c("HQ433692.1", "HQ433694.1", "HQ433691.1")
Bburg <- entrez_fetch(db = "nuccore", id = NcbiIds, rettype = "fasta")
```

The assignment demonstrates how R can be used to programmatically retrieve biological sequence data from NCBI rather than manually downloading individual sequences.

## Running the analysis

Install and load `rentrez` in RStudio, then run the R script. An internet connection is required because the code accesses the NCBI database through Entrez.

This was one of my assignments working with biological databases and getting more comfortable with retrieving and processing sequence data in R.
