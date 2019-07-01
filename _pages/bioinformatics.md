---
permalink: /bioinformatics/
title: "Bioinformatics"
---

The majority of my research depends on high-throughput analysis of large DNA sequencing datasets. In addition to publicly available tools developed by the scientific community, I have built a number of my own tools. Mostly I use python, although I typically use R for making figures.

A few of the pipelines that I have written might be useful to others. I wrote my `ChemoGeneDetection` pipeline (https://github.com/berrubin/ChemoGeneDetection) to annotate olfactory receptors and gustatory receptors in newly sequenced bee genomes. These genes evolve particularly quickly and standard gene annotation pipelines often fail to find them. Thus, my pipeline focusses exclusively on those genes similar to the set of user input sequences This pipeline should work well across insects.

`ShortfragBarcoding` (https://github.com/berrubin/ShortfragBarcoding) is a relatively simple pipeline used for identifying bee "barcode" (COI) sequences. The sequence of interest is amplified from bees and an index is attached and then the amplicon sequences are pooled on an Illumina sequencer. The pipeline demultiplexes the resulting data, finds the sequences most likely to represent each bee, and compares it to a database of known sequences to provide a species identification for that specimen. This entire procedure could be easily modified to work on another locus in another group if organisms. Bees can be very difficult to identify and sequencing an identifiable gene is sometimes the most efficient way of characterizing a species.

Whole genome alignment across multiple species is a difficult problem and those pipelines that do exist are very difficult to install. `BeeGenomeAligner` (https://github.com/berrubin/BeeGenomeAligner) is my attempt to ease this process. It merges pairwise alignments with a reference genome and creates loci that can be examined for evolutionary rate shifts.

`ComparativeGenomics` (https://github.com/berrubin/ComparativeGenomics) is a pipeline that organizes many genomics analyses. This includes both population genomics and comparative genomics tests for selection from alignments to tests for selection including dN/dS-type tests as well as MK tests.
