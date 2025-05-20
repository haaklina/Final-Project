# Title: Bioluminescent symbioses of fish and cephalopods with bacterial symbionts

## Brief introduction:

Bioluminescence is the emission of light by living organisms via biochemical including luciferin and luciferase. This feature has individually evolved several times across various taxa, which emphasizing its adaptive significance in diverse ecosystems. New details surveys have identified approximately 2,781 established bioluminescent marine species, with an extra 6,392 species from bioluminescent or prospectively luminescent genera whose luminescent status remains contradicted. This indicates that bioluminescent species constitute around 1.32% of the ~ 210,000 valid marine animal species cataloged in the World Register of Marine Species (Martini et al., 2024).

## Aim and Hypothesis:

This research is a thorough review of bioluminescent symbioses between marine organisms, specifically in relation to cephalopods and fish with bacterial symbionts. In addition, the bioluminescent symbiosis plays a significant role in biomedical science. While symbiont relationships interacting between vertebrates (e.g. sharks/fishes) and invertebrates (e.g. squids) which remains understudied in response to phylogenetic analysis of cephalopods in order to understanding the food web dynamics and future climate. In order to address this problem statement, methods will be relevance systematic literature searches, and comparative analysis of luminescence mechanisms and symbiotic interactions. 

## Brief description of your dataset (with a link to your completed GitHub repository for more details on your dataset card).
Link: https://github.com/haaklina/Final-Project/blob/main/Dataset%20Card.md

## Statistical approach (with a link to your completed GitHub repository)
Link: https://github.com/haaklina/Final-Project/blob/main/Statistical%20Approach%20and%20analysis.md

## A single reproducible figure with associated statistics as applicable:
### Phylogenetic Tree Bioluminescent and Non−luminous Marine Taxa
![image](https://github.com/user-attachments/assets/c1336c84-0d67-434f-897c-e3311e70132e)

Phylogenetic tree explains bioluminescent groups are Ostracoda_bioluminescent, *Leiognathidae*(Ponyfish), *Euprymna_scolopes*(Squid), and *Anomalops_katoptron* (Flashlight fish). Non-luminous groups are included for contrast as sister taxa.


![image](https://github.com/user-attachments/assets/4410815f-e140-40c6-93c4-42c06b167f38)

Figure 1. Box plots display the interquartile range (middle 50% of the data). Line in the box (Median): The median light organ complexity score for each clade. Whiskers extends to the minimum and maximum scores, excluding outliers. 

Interpretation: Teleost Fishes have the highest median and widest range of complexity scores. It represents greater diversity in their light organ morphology. This aligns with their wide ecological niches and multiple bioluminescent strategies. Cephalopods (e.g., squid) indicate a moderately high median with a narrower range, indicating consistently complex light organs, possibly due to the conserved role of their ventral light organs in counterillumination. Crustaceans display a lower median but with some high outliers, suggesting fewer species with high complexity, maybe reflecting diversity in habitat and light organ usage (e.g., ostracods vs. krill). Cnidaria have the lowest scores overall, indicating that their bioluminescence likely involves simpler, non-symbiotic structures, such as photocytes or protein-based light production. Ostracoda intermediate median values, with a tighter range, demonstrating more conserved structures possibly due to their unique use of bioluminescence in courtship displays.
## Interpretation of results:
Chi-square test assumes equal expected proportions (50/50) but observed is 85% horizontal and should produce a significant chi-square p-value = 3.359e-06. 85% horizontal symbiont transmission (chi-square = 21.4, p < 0.001)

ANOVA checks if the continuous light organ measure differs between two groups such as luminous or non luminous and p-value is 0.003.

Logistic regression models symbiont type (binary) predicted by categorical variables host phylogeny and habitat.

The AIC result is 86.9 that close to reported 124.6.

