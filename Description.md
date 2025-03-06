# lncRNA-Protein Interaction Analysis

## Project Overview
This dataset comprises predicted interactions between long non-coding RNAs (lncRNAs) and RNA-binding proteins (RBPs). Specifically, we have predictions of interaction probabilities for each 101 nucleotide RNA sequence for many RNA-binding proteins (RBPs).

### Data Structure:

**Index File** (`_index.tsv`):  
Contains metadata about each lncRNA transcript, including:

| Column            | Description                                       | Example                           |
|-------------------|---------------------------------------------------|-----------------------------------|
| `transcript_id`   | Ensembl Transcript ID                             | ENST00000429829.6                 |
| `gene_id`         | Ensembl Gene ID                                   | ENSG00000229807.14                |
| `gene_name`       | Common gene name (if available)                   | XIST                              |
| `filepath`        | Path to associated predictions file               | ENST00000429829.6_predictions.tsv |

**Prediction Files** (`*_predictions.tsv`):  
Each file corresponds to one transcript and provides predicted interaction probabilities with RBPs:

| Column            | Description                                                      | Example
|-------------------|------------------------------------------------------------------|--------------------|
| `rna_start`       | Starting RNA nucleotide coordinate for prediction segment        | 0                  |
| `rna_index`       | Middle nucleotide location for RNA prediction segment            | 50                 |
| `rna_end`         | Ending RNA nucleotide coordinate for prediction segment          | 100                |
| `dna_start`       | Starting DNA nucleotide coordinate for geonomic segment          | 73852623           |
| `dna_index`       | Middle geonomic location for DNA geonomic segment                | 73852673           |
| `dna_end`         | Ending DNA nucleotide coordinate for geonomic segment            | 73852723           |
| Protein Columns   | Prediction probabilities of RNA-binding interactions             | 0.694644           |

### Expanded Dataset (Planned):

The complete dataset will include predictions for interactions of **36,000 lncRNA transcripts** with interactions predicted across **154 RBPs**:

- **Sample of RBPs**: 7 protein models included here as a sample (**HNRNPC, HNRNPK, HNRNPM, MATR3, PTBP1, TIA1, SRSF1**).
- **Sample of lncRNAs**: 10 lncRNA 

- **Prediction method**: Interaction probabilities were generated using advanced computational models, specifically trained and predicted via machine learning methods. Each interaction probability reflects the likelihood of binding between the RNA segment and the specified protein.

### Project Goals and Research Questions:

The analysis aims to answer two central questions:

1. **Classification of lncRNAs:**  
   Can we classify lncRNAs into distinct groups based on patterns observed in their RBP interactions?

2. **Characterizing RBP Interaction Profiles:**  
   - Which specific RBPs or groups of RBPs have consistently **high**, **medium**, or **low** interaction probabilities across different sets of lncRNAs?
   - Can these interaction patterns provide deeper biological insights into lncRNA functionality or classification?

### Computational Goals:
- Utilize exploratory data analysis (**EDA**) and visualization techniques to identify preliminary interaction patterns.
- Leverage **unsupervised clustering or classification methods** to group transcripts based on their protein-interaction profiles.
- Produce clear visualizations (**"killer graphs"**) that intuitively communicate meaningful biological patterns and facilitate hypothesis generation for further statistical testing.

### Key Questions:
- Can meaningful groups or clusters of lncRNAs be identified solely based on their patterns of RBP interactions?
- Which RBPs or sets of RBPs best define these interaction-based groups?

---
