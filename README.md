# F8 Gene Bioinformatics Analysis

**Student:** Hobe Lagurin Palopalo  
**Course:** Cell and Molecular Biology - Laboratory  
**Date:** September 2026  
**Genome Assembly:** GRCh38/hg38

---

## Overview

This repository documents a bioinformatics investigation of the **F8 gene** (coagulation factor VIII) and its association with **Hemophilia A**, an X-linked bleeding disorder. Using the UCSC Genome Browser and NCBI ClinVar databases, this analysis explores:

- Genomic location and structure of the F8 gene
- Identification of pathogenic variants, particularly in intron 22
- Tissue-specific expression patterns via GTEx data
- Molecular mechanisms connecting genotype to phenotype

**Disease Focus:** Hemophilia A  
**Gene:** F8 (Coagulation Factor VIII)  
**Primary Mutation Type:** Nonsense mutations and intron 22 inversions

---

## Part 1: Gene Location and Genomic Context

The **F8 gene**, encoding coagulation factor VIII, is located on the **X chromosome** at cytoband **Xq28**. Using the UCSC Genome Browser (GRCh38/hg38 assembly), the gene spans approximately **186,932 base pairs**, with genomic coordinates **chrX:154,835,792–155,022,723** (visible in the Move box). The gene is transcribed from the **minus (reverse) strand**, as confirmed by the leftward-pointing arrows in the MANE Select track and the exon detail annotation (NM_000132.6).

### Genomic Features

| Feature | Value |
|---------|-------|
| **Chromosome** | X (Xq28) |
| **Coordinates** | chrX:154,835,792–155,022,723 |
| **Strand** | Minus (−) |
| **Total Size** | ~186,932 bp |
| **Canonical Transcript** | NM_000132.6 / ENST00000303265.9 |
| **Protein Length** | 2,351 amino acids |

---

## Part 2: Gene Structure

The F8 gene contains **26 exons** separated by large introns. The canonical transcript (MANE Select Plus Clinical) is **NM_000132.6 / ENST00000303265.9**, which encodes a protein of **2,351 amino acids**. Exons are densely clustered near the 5' end of the gene, while **intron 22 is notably large (~32 kb)**, making it a recombination hotspot.

The gene structure was visualized using the **GENCODE V50** and **RefSeq Curated** tracks, which clearly display the exon-intron architecture with:

- **Thick blocks** = exons (protein-coding and untranslated regions)
- **Thin lines with arrows** = introns and their directionality

### Exon Distribution

- Exons 1–22 are distributed across the first ~154 kb
- Exons 23–26 are clustered in the final ~30 kb
- Large intronic gaps between exons reflect typical human gene structure

### Screenshot

![Figure 1: Kulang
*Figure 1: UCSC Genome Browser overview of the F8 gene on chromosome X (GRCh38/hg38), showing exon-intron structure and annotation tracks.*

---

## Part 3: Variant Density and Pathogenic Hotspots

The **ClinVar** and **OMIM Allele** tracks reveal a **high density of known pathogenic variants** across the F8 gene, particularly in **intron 22**. This region contains **int22h-1** and **int22h-2/3** homologous repeat sequences, which are visible as **RepeatMasker annotations**. These repeats facilitate **intrachromosomal homologous recombination**, leading to the **intron 22 inversion (inv22)**—the most common cause of severe Hemophilia A (~45% of cases).

### Intron 22 Characteristics

| Feature | Description |
|---------|-------------|
| **Size** | ~32 kb |
| **Contains** | int22h-1 repeat (within intron 22) and int22h-2/3 repeats (extragenic, upstream) |
| **Mechanism** | Ectopic recombination between repeats causes 0.6 Mb inversion |
| **Clinical Consequence** | Disrupts exons 23–26, producing truncated, nonfunctional Factor VIII |

### Variant Density

Zooming into **chrX:154,890,000–154,925,000** confirmed this region's high variant density, with:

- **Hundreds of dbSNP entries** (e.g., rs182834386, rs137852460)
- **OMIM allele numbers:** 300841.0023–300841.0241
- **ClinVar variants:** Pathogenic, likely pathogenic, and benign classifications

### Screenshot

![Figure 2: Kulang
*Figure 2: Zoomed view of intron 22 (chrX:154,890,000–154,925,000), highlighting high ClinVar/OMIM variant density and RepeatMasker annotations.*

---

## Part 4: Specific Pathogenic Variant Analysis

### Selected Variant: OMIM 300841.0228 (rs137852460)

I examined **OMIM allele variant 300841.0228**, which corresponds to **dbSNP entry rs137852460**. This variant causes **Hemophilia A** and results in an amino acid change **p.Ser2170Ter** (serine at position 2170 replaced by a stop codon).

### Molecular Consequence

The "**Ter**" designation indicates a **nonsense mutation**—a premature stop codon that truncates the Factor VIII protein. Since the full-length protein contains **2,351 amino acids**, truncation at residue 2170 removes approximately **181 C-terminal residues**, eliminating critical functional domains required for:

- Protein stability
- Interaction with factor IXa
- Binding to von Willebrand factor
- Overall coagulation activity

### Genomic Context

This variant is located at **chrX:154,896,093** on the **minus strand**, placing it within **intron 22**—the same region identified as a recombination hotspot. The presence of pathogenic nonsense mutations in this interval, alongside structural rearrangements like inversions, underscores why intron 22 is clinically significant for Hemophilia A severity.

### Connection to Activity 1 (Previous Lab)

In my previous lab activity, I analyzed a different nonsense mutation (**c.2209C>T, p.Arg737Ter**) that truncated Factor VIII at residue 737. Comparing these two variants illustrates how nonsense mutations at different positions produce varying degrees of protein truncation:

| Variant | Position | Residues Lost | % Protein Lost | Phenotype |
|---------|----------|---------------|----------------|-----------|
| p.Arg737Ter | 737 | 1,614 | ~69% | Severe |
| p.Ser2170Ter | 2,170 | 181 | ~8% | Potentially Milder |

Both mechanisms abolish normal Factor VIII function but through different extents of disruption, demonstrating the structure-function relationship in coagulation proteins.

### Screenshot

![Figure 3: Kulang
*Figure 3: OMIM Allele variant 300841.0228 detail page, showing p.Ser2170Ter nonsense mutation and Hemophilia A phenotype.*

---

## Part 5: Tissue Expression Context

### GTEx Data Analysis

Using the **GTEx Gene V8 track**, I observed that F8 expression is **highly tissue-specific**. The highest median expression (~19.65 TPM) was found in **Adipose - Visceral (Omentum)**, with significant expression also in various **Artery tissues**. Expression was minimal in brain, muscle, and other non-vascular tissues.

### GTEx Expression Summary

| Tissue | Expression Level (TPM) |
|--------|----------------------|
| Adipose - Visceral (Omentum) | 19.65 (Highest) |
| Artery - Coronary | High |
| Artery - Tibial | High |
| Artery - Aorta | High |
| Brain | Minimal |
| Muscle | Minimal |
| Liver Bulk Tissue | Low |

### Discussion of Discrepancy

This result is **counterintuitive** since Factor VIII is primarily synthesized by **liver endothelial cells (sinusoidal endothelial cells)**, not hepatocytes. However, **GTEx measures bulk tissue expression**. Adipose and arterial tissues contain abundant endothelial cells (which produce Factor VIII) relative to their overall mass, while the liver is dominated by hepatocytes (which do *not* produce F8). Thus, F8 expression from liver endothelial cells is **diluted in bulk measurements**.

This discrepancy illustrates a fundamental limitation of bulk RNA-seq: **cell-type specificity is masked by tissue composition**. This is precisely why we need the **Cell Browser activity**—to resolve F8 expression at **single-cell resolution** and identify the exact endothelial subpopulations responsible for Factor VIII synthesis.

### Screenshot

![Figure 4: Kulang

*Figure 4: GTEx Gene V8 expression profile of F8 across 54 human tissues, showing highest expression in adipose and artery tissues.*

---

## Part 6: Interpretation and Reflection

### Question 1: What did UCSC show you about your gene that was not obvious from simply reading about the gene's function?

UCSC revealed that the F8 gene's **genomic architecture directly explains its disease mechanism**. While reading about Hemophilia A describes protein truncation, the browser showed that intron 22's massive size (~32 kb) and its homologous repeat sequences (int22h-1, int22h-2/3) create a **structural vulnerability**. This physical arrangement predisposes the region to recombination events that cause inversions—a mechanism not apparent from protein function alone. The visual density of variants in this specific interval made clear why intron 22 accounts for ~45% of severe cases.

### Question 2: Why is knowing the exact genomic location of a disease-associated variant useful?

Knowing the exact genomic location (e.g., chrX:154,896,093 for rs137852460) allows researchers to:

1. **Predict functional consequences** based on whether the variant falls in exons, introns, splice sites, or regulatory regions
2. **Identify structural context** (e.g., proximity to repeat sequences or recombination hotspots)
3. **Correlate genotype with clinical phenotype** by comparing mutation locations to disease severity
4. **Design targeted therapies** or screening strategies based on mutation type
5. **Understand population genetics** by mapping variants to genomic coordinates in different populations

Location determines function in ways that the variant name alone cannot convey.

### Question 3: What is one limitation of predicting a variant's effect only from its genomic location?

Genomic location alone does not reveal the **molecular consequence**. For example, two variants at different positions in the same exon might produce different outcomes:

- One could be a **silent/synonymous mutation** (no amino acid change)
- Another a **missense mutation** (altered but potentially functional protein)
- A third a **nonsense mutation** (truncation and loss of function)

Additionally, variants in introns might affect **splicing**, **regulatory elements**, or have **no effect at all**. Functional validation through cell-based assays, protein studies, and clinical phenotyping is needed to confirm predicted effects.

### Question 4: What was the most interesting feature you observed about your assigned gene?

The most interesting feature was the **striking contrast between the GTEx bulk tissue expression data** (highest in Adipose - Visceral) and the **known biology** (Factor VIII synthesized by liver endothelial cells). This discrepancy highlighted a fundamental limitation of bulk RNA-seq: **cell-type specificity is masked by tissue composition**. This observation made clear why **single-cell technologies** (like the Cell Browser) are essential for resolving true cellular sources of gene expression, especially in heterogeneous tissues like liver and adipose tissue where rare cell types (endothelial cells) may be functionally critical but numerically minor.

---

## Conclusion

The UCSC Genome Browser successfully mapped the F8 gene to chromosome Xq28, revealed its complex structure with 26 exons and large introns, and highlighted the pathological significance of intron 22 as a recombination hotspot. The GTEx expression data further contextualized F8 as an endothelial-enriched gene, bridging genomic location with functional biology.

The specific analysis of **OMIM variant 300841.0228 (p.Ser2170Ter)** demonstrated how single-nucleotide changes in this region lead to truncated, nonfunctional Factor VIII and severe Hemophilia A. Comparison with the p.Arg737Ter mutation from Activity 1 illustrated how different truncation positions produce varying disease severity.

The GTEx tissue expression pattern revealed an important limitation of bulk RNA-seq data: while F8 appears highest in adipose tissue, the true biological source is endothelial cells, which comprise a small fraction of liver mass but are the primary therapeutic target. Together, these observations connect the **molecular genetics** of Hemophilia A to its **cellular and tissue-level manifestations**, and demonstrate why integrative approaches combining genomic, transcriptomic, and single-cell data are essential for understanding human disease.

---

## References

- **UCSC Genome Browser:** https://genome.ucsc.edu/
- **UCSC Genome Browser 101 Tutorial:** https://genome.ucsc.edu/docs/tutorials/gb101.html
- **NCBI ClinVar:** https://www.ncbi.nlm.nih.gov/clinvar/
- **GTEx Portal:** https://www.gtexportal.org/
- **F8 Gene - NCBI RefSeq:** NM_000132.6 / NP_000123.1
- **OMIM - Hemophilia A:** https://www.omim.org/entry/306700
- **ClinVar - rs137852460:** https://www.ncbi.nlm.nih.gov/clinvar/variation/137852460/

---

