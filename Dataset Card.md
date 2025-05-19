## Dataset title: 
Phylogenetic Tree Project of Ascidians species.

## Dataset citation and DOI:
Gao, P., Khong, H. Y., Mao, W., Chen, X., Bao, L., Wen, X., & Xu, Y. (2023). Tunicates as sources of high-quality nutrients and bioactive compounds for food/feed and pharmaceutical applications: *A review. Foods*, *12*(19), 3684.

Ramesh, C., Tulasi, B. R., Raju, M., Thakur, N., & Dufossé, L. (2021). Marine natural products from tunicates and their associated microbes. *Marine drugs*, *19*(6), 308.

Wilson, E. R., Murphy, K. J., & Wyeth, R. C. (2022). Ecological review of the Ciona species complex. *The Biological Bulletin*, *242*(2), 153-171.

Ciona wikipedia.

https://seanet.stanford.edu/Urochordata


## Dataset Summary:
Phylogenetic Tree of Gene Sequences from National Center for Biotechnology Information (NCBI)
This dataset contains gene sequence data (nucleotide) obtained from the (NCBI) (https://www.ncbi.nlm.nih.gov/nuccore/?term=Ascidian) in FASTA format and a corresponding Nexus file used for generating phylogenetic trees. The purpose of this project is to construct and analyze phylogenetic relationships among Ascidian species using sequence data.

## Data format:
All data are DNA sequences in standard fasta files, grouped either by species (in the case of the animals) or in sequencing run (in the case of the ascidians samples).

## Languages:
English

## Data Sources:
Data retrieved from: NCBI (National Center for Biotechnology Information)

## Data Instances: 
File Formats: .fasta for gene sequences, .nexus for phylogenetic tree generation
sequences.fasta: Contains around 600bais pairs (bp) gene sequences different tunicate species (demo species collected: source: https://seanet.stanford.edu/Urochordata) in FASTA format.

## Documentation for Source Datasets
### Tunicate datasets

| Species Name  | Genetic Marker  | Tunicate Population   | Sources  |
|---|---|---|---|
| *Pyura chilensis* | 614 bp DNA, CO1* gene | Solitary | Gao et al. 2023 |
| *Styela plicata* | 624 bp DNA, COX1* gene | Solitary | Gao et al. 2023; Ramesh et al. 2021 |
| *Synoicum kincaidi* | 658 bp DNA, COX1 gene | Colonial | https://seanet.stanford.edu/Urochordata |
| *Ciona intestinalis* | 786 bp DNA, COX1 gene | Solitary | Wilson et al. 2022; Ramesh et al. 2021. |
| *Boltenia villosa* | 658 bp DNA, CO1 gene | Solitary | https://seanet.stanford.edu/Urochordata |
| *Distaplia occidentalis* | 658 bp DNA, COX1 gene | Colonial | https://seanet.stanford.edu/Urochordata |
| *Ascidia ceratodes* | 845 bp DNA, COX1 gene | Solitary | Solitary
| *Diplosoma listerianum* | 531 bp DNA, CO1 gene | Colonial | https://seanet.stanford.edu/Urochordata |
| *Cnemidocarpa finmarkiensis* | 658 bp DNA, COI gene | Solitary | https://seanet.stanford.edu/Urochordata |
| *Ciona robusta* | 626 bp DNA, COX1 gene | Solitary | Wilson et al. 2022 |
| *Ciona edwardsi* | 737 bp DNA, CO1 gene | Solitary | Ciona wiki |
| *Ciona roulei* | 744 bp DNA, CO1 gene | Solitary | Ciona wiki |
| *Ciona sp.* | 583 bp DNA, p. cox3 gene | Solitary | Ciona wiki |
| *Styela montereyensis* | 580 bp DNA, CO1 gene | Solitary | Gao et al. 2023 |
| *Pyura haustor* | 658 bp DNA, CO1 gene | Solitary | Gao et al. 2023 |
| *Halocynthia igaboja* | 708 bp DNA, COX1 gene | Solitary | Ciona wiki |
| *Sigillina signifera* | 759 bp DNA, COX1 gene | Solitary | Ramesh et al. 2021 |
| *Phallusia nigra* | 606 bp DNA, COX1 gene | Solitary | Ramesh et al. 2021 |
| *Polycarpa pomaria* | 617 bp DNA, CO1 gene | Solitary | Gao et al. 2023 |
| *Halocynthia aurantium*| 658 bp DNA, COX1 gene | Solitary | Gao et al. 2023; Ramesh et al. 2021 |


COX1* cytochorme c oxidase subunit I gene.
CO1* cytochrome oxidase subunit 1.

## Preprocessing and Data Formatting
I downloaded all the genomes as fasta files and renamed them to include the genus and species in the file names including population's name.

For the read files, I downloaded them in fasta format, and if a species had multiple read files from the same sequencing platform, I concatenated them into a single file for all downstream processing. I used ALiView for alignment and trimming all the short read files to remove adapter sequences, though I did trim them for quality as well. 

Collect them into a final fasta file and after alignment I got organized data in Nexus format for analysis in MrBayes or R program for generating tree.

## Usage: 
Analysis goals (phylogenetic tree construction).

## Limitations: 
Biases or limitations (e.g., incomplete gene sequences).
