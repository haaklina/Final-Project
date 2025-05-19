## Statisitical Approach:

Hypothetically 60+ species with bioluminescent symbionts across 5 marine clades analysis.

Regression for host-symbiont specificity.

ANOVA to compare light organ complexity by taxa.

Chi-square tests for symbiosis acquisition mode (vertical vs. horizontal).

### Creating a phylogenetic tree showing the relationships among bioluminescence and non-luminescence marine taxa.
Regariding tree analysis, I have overview following R codes:

```{r}
options(repos = c(CRAN = "https://cran.rstudio.com"))
```
```{r} include=FALSE}
options(repos = c(CRAN = "https://cran.rstudio.com"))
install.packages("ape")   # only if not already installed
library(ape)
```
```{r}
# Install and load ape package
install.packages("ape")  # Run only once
library(ape)

# Define the tree in Newick format
tree_text <- "((((Ostracoda_bioluminescent,Ostracoda_nonluminescent),((Leiognathidae,Non_luminous_teleosts))),((Euprymna_scolopes,Non_luminous_cephalopods),(Anomalops_katoptron,Non_luminous_Beryciformes))));"

# Read the tree from text
biolum_tree <- read.tree(text = tree_text)

# Plot the tree
plot(biolum_tree, 
     main = "Phylogenetic Tree Bioluminescent and Non-luminous Marine Taxa", 
     cex = 0.9)

# Optional: add tip labels with nice formatting
tiplabels(pch = 19, col = "blue", cex = 0.5)
```

Figure. 1 explanation: Bioluminescent groups are Ostracoda_bioluminescent, *Leiognathidae* (Ponyfish), *Euprymna_scolopes* (Squid), and *Anomalops_katoptron* (Flashlight fish). Non-luminous groups are included for contrast as sister taxa.

