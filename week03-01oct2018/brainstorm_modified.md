

# Part 1 - Brainstorm: Statistics

## Distributions
## Statistical Models
## Methods for Estimation
## Methods for Hypothesis Testing

# Part 2 - Brainstorm: Technologies in Biology

## Microarray
## ...

## In-class exercise 1 (15 minutes)

### Technologies: 

```{r}
techs <- c("microarray", "rna-seq", "dna-seq", 
           "bisulphite-seq", "cytometry", "mass-spec", 
           "10x-chromium", "oxford-nanopore")

s <- sample(length(techs))
data.frame(row=s, techs)
```

### Task: 
#### produce a 2-3 point summary of "how it works"
#### links to a few (<5) good resources
#### create a markdown file for it and upload to README.me in "group assignment" repo

# Part 3 - Brainstorm: Applications in genomics 

# Part 4 - Brainstorm: Linking Technologies to Applications to Statistics

## e.g., microarray -> gene expression -> normally distributed (log intensities)

# Part 5 - Brainstorm: Methods/algorithms in genomics associated to Computer Science

# Part 6 - Pick a "technology" (from above, from [1] or otherwise) to briefly describe

## Exercise 2 (in groups of 1-3): 
### Goal: 
#### write ~2 sentences about what the method does
#### again, make the link (technology -> application -> statistics)
#### list the github usernames of everyone in your group
#### submit a pull request to brainstorm_modified.md

[1] [https://liorpachter.wordpress.com/seq/](https://liorpachter.wordpress.com/seq/)

##ATAC-Seq

ATAC-seq is a sensitive technique used to assess genome-wide chromatin accessibility at nucleotide level, aiming to characterize interactions between DNA and histone proteins.
The main actor is the hyperactive Tn5 transposase, which preferentially operates on nucleosome-free chromatin regions. 
The main advantage of this method is, that in combination with pre-loaded sequencing adapters, administration of Tn5 transposase enables a simultaneous fragmentation and adapter tagging for library preparation.

###Technology
The chosen technology is ATAC-seq. 

###Applications
Its applications include genome wide identification of changes in nucleosome position, transcription factor occupancy and chromatin density at nucleotide resolution.
This is helpful to characterize the development and the presence of pathological conditions. Furthermore, ATAC-seq can be applied to create personalized epigenomic maps, which display the individual daily changes in chromatin packaging.


###Statistical methods
A pipeline was developed to process and analyse the ATAC-seq data. This pipeline uses various different statistical tools, which apply different types of statistical methods: 
**ZINBA (Zero-Inflated Negative Binomial Algorithm)** -> for peak calling: novel mixture regression model,determination of relative likelihood,posterior probabilities of component membership, weighted generalized linear models
**ChromHMM**-> to calculate ATAC-seq insertion size enrichment analysis within chromatin annotations: multivariate Hidden Markov Model (defines chromatin states based on histone modification patterns)
**DANPOS** -> for dynamic nucleosome analysis at single nucleotide resolution: quantile normalization, Poisson test (default), chi square test (alternative), negative binominal test (alternative)
**CENTIPEDE** -> for transcription factor motif analysis: posterior probabilites (weighed)
hierarchial clustering (Euclidean distance)
hierarchical clustering (Pearson correlation)
mean centering

###List of members
Sarah Greve (github username: greves)
Rosamaria Lugarà (github username: rlugar)

