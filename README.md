# Snakemake files for initial NGS

The first snakemake file, `snake_make_CHiP_ATACseq  `, provides rules that are common to most NGS data.  This file assume human genome GRCh38 and `Genome = ...` should be changed to work with another genome.

**1** Building index for a genome, rule `index_genome` creates *genome*`.index` for *genome*`.fa`

**2** Aligning reads, rule `align_reads` creates *sample*`.bam` for *sample*`.fastaq`

**3** Computing metrics of the alignment, rule `macs2peaks` creates *sample*`.peaks` for *sample*`.bam`

**4** Computing peaks using MACS2, rule `` creates *sample*`.peaks/` directory for *sample*`.bam`