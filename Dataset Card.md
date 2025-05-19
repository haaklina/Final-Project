## Dataset title: 
Bioluminescent symbioses of fish and cephalopods with bacterial symbionts.

## Dataset citation and DOI:
Dunlap, P. V., Davis, K. M., Tomiyama, S., Fujino, M., & Fukui, A. (2008). Developmental and microbiological analysis of the inception of bioluminescent symbiosis in the marine fish Nuchequula nuchalis (Perciformes: Leiognathidae). Applied and environmental microbiology, 74(24), 7471-7481.

Jones, B. W., & Nishiguchi, M. K. (2004). Counterillumination in the hawaiian bobtail squid, Euprymna scolopes Berry (Mollusca: Cephalopoda). Marine Biology, 144(6), 1151-1155. (Primary review).

Hellinger, J., Jägers, P., Donner, M., Sutt, F., Mark, M. D., Senen, B., ... & Herlitze, S. (2017). The flashlight fish Anomalops katoptron uses bioluminescent light to detect prey in the dark. PLoS One, 12(2), e0170489.

Heath-Heckman, E. A., Peyer, S. M., Whistler, C. A., Apicella, M. A., Goldman, W. E., & McFall-Ngai, M. J. (2013). Bacterial bioluminescence regulates expression of a host cryptochrome gene in the squid-vibrio symbiosis. MBio, 4(2), 10-1128. 

Lupp, C., & Ruby, E. G. (2005). Vibrio fischeri uses two quorum-sensing systems for the regulation of early and late colonization factors. Journal of bacteriology, 187(11), 3620-3629.

Nyholm, S. V., & McFall-Ngai, M. J. (2021). A lasting symbiosis: how the Hawaiian bobtail squid finds and keeps its bioluminescent bacterial partner. Nature Reviews Microbiology, 19(10), 666-679.

Sparks, J. S., Dunlap, P. V., & Smith, W. L. (2005). Evolution and diversification of a sexually dimorphic luminescent system in ponyfishes (Teleostei: Leiognathidae), including diagnoses for two new genera. Cladistics, 21(4), 305-327.

Wier, A. M., Nyholm, S. V., Mandel, M. J., Massengo-Tiassé, R. P., Schaefer, A. L., Koroleva, I., ... & McFall-Ngai, M. J. (2010). Transcriptional patterns in both host and bacterium underlie a daily rhythm of anatomical and metabolic change in a beneficial symbiosis. Proceedings of the National Academy of Sciences, 107(5), 2259-2264.

Yount, T. A., Murtha, A. N., Cecere, A. G., & Miyashiro, T. I. (2023). Quorum sensing facilitates interpopulation signaling by Vibrio fischeri within the light organ of Euprymna scolopes. Israel journal of chemistry, 63(5-6), e202200061.

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
### Comparative Features of Bioluminescent Symbiosis in *Euprymna scolopes* and *Leiognathid* Fishes.


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
