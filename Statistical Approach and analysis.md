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

![image](https://github.com/user-attachments/assets/967a1055-3d5f-45da-9c68-b3faa61ec9d1)
Figure. 1 explanation: Bioluminescent groups are Ostracoda_bioluminescent, *Leiognathidae* (Ponyfish), *Euprymna_scolopes* (Squid), and *Anomalops_katoptron* (Flashlight fish). Non-luminous groups are included for contrast as sister taxa.

## Simulated Dataset Structure Example

```{r}
# Simulate example data
set.seed(42)
n <- 60
```
```{r}
data <- data.frame(
  species = paste("Species", 1:n),
  clade = sample(c("Cephalopod", "Fish", "Ostracod"), n, replace = TRUE),
  acquisition = sample(c(0, 1), n, replace = TRUE), # 1 = acquired symbiont
  light_organ_complexity = sample(1:5, n, replace = TRUE),
  transmission = sample(c("vertical", "horizontal"), n, replace = TRUE)
)

head(data)
```

## Logistic Regression: Predict Symbiont Acquisition

```{r}
# Predict acquisition based on clade and complexity
log_model <- glm(acquisition ~ clade + light_organ_complexity, data = data, family = "binomial")
summary(log_model)
```

## ANOVA: Compare Light Organ Complexity Across Clades

```{r}
anova_model <- aov(light_organ_complexity ~ clade, data = data)
summary(anova_model)
```
## Chi-square Test: Vertical vs Horizontal Transmission Across Clades

```{r}
# Create contingency table
trans_table <- table(data$clade, data$transmission)
```
```{r}
# Run chi-square test
chisq.test(trans_table)
```
```{r}
library(ggplot2)

# Barplot of transmission mode
ggplot(data, aes(x = clade, fill = transmission)) +
  geom_bar(position = "dodge") +
  labs(title = "Transmission Mode by Clade", x = "Clade", y = "Count")
```

![image](https://github.com/user-attachments/assets/f3b991fc-ac66-4998-94d9-a617ae8ead0e)




