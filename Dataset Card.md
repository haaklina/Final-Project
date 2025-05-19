## Dataset title: 
Bioluminescent symbioses of fish and cephalopods with bacterial symbionts.

## Dataset citation and DOI:
Gao, P., Khong, H. Y., Mao, W., Chen, X., Bao, L., Wen, X., & Xu, Y. (2023). Tunicates as sources of high-quality nutrients and bioactive compounds for food/feed and pharmaceutical applications: *A review. Foods*, *12*(19), 3684.

Ramesh, C., Tulasi, B. R., Raju, M., Thakur, N., & Dufossé, L. (2021). Marine natural products from tunicates and their associated microbes. *Marine drugs*, *19*(6), 308.

Wilson, E. R., Murphy, K. J., & Wyeth, R. C. (2022). Ecological review of the Ciona species complex. *The Biological Bulletin*, *242*(2), 153-171.


## Dataset Summary:
Phylogenetic Tree of Gene Sequences from National Center for Biotechnology Information (NCBI)
This dataset contains gene sequence data (nucleotide) obtained from the (NCBI) (https://www.ncbi.nlm.nih.gov/nuccore/?term=marineclade taxa) in FASTA format and a corresponding Nexus file used for generating phylogenetic trees. The purpose of this project is to construct and analyze phylogenetic relationships among luminous and non-luminous species using sequence data.

## Data format:
All data are DNA sequences in standard fasta files, grouped either by species (in the case of the animals) or in sequencing run.

## Languages:
English

## Data Sources:
Data retrieved from: NCBI (National Center for Biotechnology Information)

## Data Instances: 
File Formats: .fasta for gene sequences, .nexus for phylogenetic tree generation
sequences.fasta: Contains around 600bais pairs (bp) gene sequences different tunicate species (demo species collected: source: https://seanet.stanford.edu/Urochordata) in FASTA format.

## Documentation for Source Datasets
### Comparative Features of Bioluminescent Symbiosis in Euprymna scolopes and Leiognathid Fishes.


| Species Characteristics  | *Euprymna scolopes* (squid)  | *Leiognathids* (Fishes)   | Sources |
|---|---|---|---|
| **Symbiont** | *Vibrio fischeri* | *Photbacterium leiognathi* | Dunlap et al., 2008; Heath-Heckman et al., 2013 |
| **Light organ** | Ventral crypt-based | Ventral/sub-orbital shutters | Dunlap & Nakamura, 2011; Nyholm & McFall-Ngai, 2021 |
| **Acquisition** | Environmental or horizontal | Environmental and Horizontal | Yount et al., 2023; Dunlap et al., 2008 |
| **Function** | Counterillumination campuflage | Communication, Mating, Camouflage | Jones & Nishiguchi, 2004; Hellinger et al., 2017 |
| **Regulation** | Quorum sensing and host expulsion | Quorum sensing and muscular shutter | Wier et al., 2010; Lupp & Ruby, 2005 |
| **Sexual dimorphism** | None reported | Common in males, enlarged light organs, transparent flanks | Sparks et al., 2005 |

## Preprocessing and Data Formatting
I downloaded all the genomes as fasta files and renamed them to include the genus and species in the file names including population's name.

For the read files, I downloaded them in fasta format, and if a species had multiple read files from the same sequencing platform, I concatenated them into a single file for all downstream processing. I used ALiView for alignment and trimming all the short read files to remove adapter sequences, though I did trim them for quality as well. 

Collect them into a final fasta file and after alignment I got organized data in Nexus format for analysis in MrBayes or R program for generating tree.

## Usage: 
Analysis goals (phylogenetic tree construction).

## Limitations: 
Biases or limitations (e.g., incomplete gene sequences).
