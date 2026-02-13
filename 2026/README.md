# Structural Variant Teaching Dataset  
Bos taurus – Chromosome 13 (IGV-ready subset)

---

## Overview

This dataset was prepared for teaching structural variant (SV) analysis using long-read sequencing data (Oxford Nanopore).

The material includes:

- Two samples (2024 and 2025)
- High-confidence structural variants
- Chromosome 13 only
- Reads restricted to ±20 kb around selected SV loci

The dataset is intentionally reduced in size so that it loads quickly in IGV and can be used in classroom settings without heavy computational requirements.

---

## Dataset Contents

### Reference Genome (Chromosome 13 only)

- `Bos_taurus_chr13.fa`
- `Bos_taurus_chr13.fa.fai`

Reference sequence used for alignment and visualization.

---

### Alignment Files

- `2024_chr13_teaching_20kb.bam`
- `2024_chr13_teaching_20kb.bam.bai`
- `2025_chr13_teaching_20kb.bam`
- `2025_chr13_teaching_20kb.bam.bai`

These BAM files contain only reads overlapping selected structural variant regions (±20 kb).  
They allow direct comparison between two samples.

---

### Structural Variant Calls

- `joint_chr13_teaching_20kb.vcf.gz`
- `joint_chr13_teaching_20kb.vcf.gz.tbi`

Joint multi-sample SV calls generated using Sniffles2 (v2.0.7).

High-confidence variants were selected using the following criteria:

- PRECISE calls only
- QUAL ≥ 50
- One sample homozygous alternate (1/1)
- The other sample homozygous reference (0/0)
- Variant read support ≥ 4
- No conflicting reference reads in the alternate sample

---

### Gene Annotation

- `Bos_taurus_chr13.gtf.gz`
- `Bos_taurus_chr13.gtf.gz.tbi`

Ensembl gene annotation restricted to chromosome 13.

---

## How to Use in IGV

1. Load the reference genome (`Bos_taurus_chr13.fa`)
2. Load both BAM files
3. Load the VCF file
4. Load the gene annotation (GTF)
5. Navigate to a variant coordinate
6. Compare genotype and read support between samples

---

## Educational Purpose

This dataset enables students to:

- Visualize insertions and deletions in long-read alignments
- Compare genotypes between two samples
- Interpret read-level support (DV / DR)
- Understand how structural variants are represented in VCF
- Connect structural variation to gene structure
- Investigate gene function using public databases

---

## Software Required

- IGV (recommended for visualization)
- samtools
- bcftools
- bedtools
- Sniffles2 (for reproducibility)

---

## Notes

- Data were derived from course-based research activities.
- Only chromosome 13 is included.
- Only selected high-confidence SV regions are retained.
- The dataset is intended for teaching and demonstration purposes.

---
