---
layout: post
category: tutorial
title:  "Analyzing, curating, and annotating bacterial artificial chromosome clones from complex genomes"
date:   2017-03-28 12:40:00 +0000
categories: BAC PacBio
---

In this tutorial we explore current approaches at assembling, curating, and annotating bacterial artificial chromosomes (BACs) from complex genomes. We use an example from the <i>Mla</i> locus in barley and discuss methodologies to annotate different biological information.

## Introduction
Several strategies exist for generating large sequence insert libraries including cosmid (Lambda phage cos sequence-based; 37-52 kb), fosmid (bacterial F-plasmid; up to 40 kb), bacterial artificial chromosomes (BACs; 150-350 kb), and yeast artificial chromsomes (YACs; 100-1000 kb). While YACs can contain the largest inserts, they have been dropped from use due to instability. Large insert libraries are the foundation of assembling genomes including the generation of minimal tiling paths (MTPs) and the characterization of complex loci (such as loci containing R genes).

Sequencing of large insert libraries traditional involved the subcloning of plasmids into smaller fragments with varying length, often with fragment sizes around 3 kb. Flanking sequence within the cloned fragments are subsequently sequenced using Sanger sequencing. A depth of approximately 10X was required for assembly of the BAC. Full assembly of BAC clones would be performed phred/phrap and CAP3 software that use an overlap-based approach for assembly. The quality of the assembly could be inferred by concordance of subcloned fragment size length with anchored 5' and 3' sequenced inserts.

Significant gains in long read sequencing such as PacBio permits the identification of a single contig in one SMRT sequencing run. This improvement can be attributed to the generation of long reads up to 30 kb. These reads take the place of subcloned fragments in traditional sequencing, whereas small reads are used for refinement of the sequence. While the HGAP assembly pipeline is extremely powerful, by default it will assume that the genome is linear rather than circular. A pipeline exists to deal with the problem, but manual curation can also be used. Below are some examples of sequenced BAC clones from the Mla7 locus from the barley cultivar CI 16153 that involve various types of assembly outputs.

