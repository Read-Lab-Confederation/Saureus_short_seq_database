library(googlesheets4)
library(Biostrings)
library(tidyverse)

short_seqs <- read_sheet("https://docs.google.com/spreadsheets/d/1-8TOA2eY1j5h5frcOCiKiCoTMN0JCwU3sVijJ-GvHSc")
ss_db <- short_seqs %>%
  filter(Include_bactopia == 1)

short_blast_DNAstr <- DNAStringSet(ss_db$Sequence)
names(short_blast_DNAstr) <- ss_db$Fasta_header

writeXStringSet(short_blast_DNAstr,filepath = "./staphopia_short_seqs.fasta")