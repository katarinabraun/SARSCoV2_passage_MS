# Limited SARS-CoV-2 diversity within hosts and following passage in cell culture

**Gage K. Moreno**<sup>1*</sup>, **Katarina M. Braun**<sup>2*</sup>, Peter J. Halfmann<sup>2</sup>, Trent M. Prall<sup>1</sup>, Kasen K. Riemersma<sup>2</sup>, , Amelia K. Haj<sup>1</sup>, Joe Lalli<sup>2</sup>, Kelsey W. Florek<sup>3</sup>,Yoshihiro Kawaoka<sup>2</sup>, Thomas C. Friedrich<sup>2,3</sup>, David H. O’Connor<sup>1,3</sup> 

\* **These authors contributed equally to this work**  

1. Department of Pathology and Laboratory Medicine, University of Wisconsin-Madison, Madison, WI, United States of America
2. Department of Pathobiological Sciences, University of Wisconsin-Madison, Madison, WI, United States of America
3. Wisconsin State Lab of Hygiene, Bioinformatics, Madison, WI, United States of America 
4. Influenza Research Institute, School of Veterinary Sciences, University of Wisconsin-Madison, Madison, WI, United States
5. Wisconsin National Primate Research Center, University of Wisconsin-Madison, Madison, WI, United States of America

**Abstract**:

Since the first reports of pneumonia associated with a novel coronavirus (COVID-19) emerged in Wuhan, Hubei province, China, there have been considerable efforts to sequence the causative virus, SARS-CoV-2 (also referred to as hCoV-19) and to make viral genomic information available quickly on shared repositories. As of 30 March 2020, 7,680 consensus sequences have been shared on GISAID, the principal repository for SARS-CoV-2 genetic information. These sequences are primarily consensus sequences from clinical and passaged samples, but few reports have looked at diversity of virus populations within individual hosts or cultures. Understanding such diversity is essential to understanding viral evolutionary dynamics. Here, we characterize within-host viral diversity from a primary isolate and passaged samples, all originally deriving from an individual returning from Wuhan, China, who was diagnosed with COVID-19 and subsequently sampled in Wisconsin, United States. We use a metagenomic approach with Oxford Nanopore Technology (ONT) in combination with Illumina MiSeq to capture minor within-host frequency variants ≥1%. In a clinical swab obtained from the day of hospital presentation, we identify 15 single nucleotide variants (SNVs) ≥1% frequency, primarily located in the largest gene – ORF1a. While viral diversity is low overall, the dominant genetic signatures are likely secondary to population size changes, with some evidence for mild purifying selection throughout the genome. We see little to no evidence for positive selection or ongoing adaptation of SARS-CoV-2 within cell culture or in the primary isolate evaluated in this study. 

**What is contained in this repository**: 

This repository contains all of the raw data and/or links to the SRA bioproject where all raw data is stored that were used in this manuscript. This is contained in the `data_raw` directory. 

The pipelines used to process the raw reads (pair and merge reads, trim reads, filter for length and quality, map to reference, normalize coverage, and call variants) are contained in the `data_pipelines` directory. There is one pipeline for the ONT data and one pipeline for the Illumina data. 

All data analysis and the scripts used to generate derived data as well as most figures (figures 3, 4, 5, 6 and supplemental figures 2 and 3) are contained in the `data_derived` directory. 

The `figures` directory contains the output from all above scripts and `figures/manuscript_figures` contains all of the figures that were manipulated in Adobe Illustrator for the manuscript. 

**How to use this repository**: 

After downloading or cloning this repository, here's the recommended order of operations: 
1. Grab the raw data from this bioproject [PRJNA607948](ttps://www.ncbi.nlm.nih.gov/bioproject/PRJNA607948/)    
- This bioproject contains FASTQs that have been mapped to reference (MT039887.1) and converted from an alignment file-type back to a FASTQ. We did this to ensure we were not uploading any contaminating human reads. The FASTQs from this bioproject can be fed directly into the ONT pipeline. The Illumina pipeline is configured to take in bams, instead of FASTQs, so these bam files to feed into the Illumina pipeline can be found in this repository – `data_raw/Illumina_bams/*`. 
2. The ONT and Illumina pipelines can be found in `data_pipelines`. There are READMEs in each directory with detailed instructions about how to run these pipelines. These pipelines will spit out VCF files that are input for secondary analyses. 
3. All secondary analyses and scripts to generate figures can be found in `data_derived`. All VCFs, generated from the aforementioned pipelines, can already be found in this directory so there is no need to re-run the pipelines if you are only interested in replicating figures. All analyses and figures were written in Jupyter Notebooks so each step (seperated into cells) can be run independently. 

**Contacts us if you have questions:**

Please reach out to us if you have any questions about anything in this repository! We've done our best to make all data, derived data, and scripts available and as reproducible as possible, but we are still developing our bioinformatic skills so we apologize in advance if some things are a bit clunky. 

Here's our contact info: 
- Katarina Braun: kmbraun2@wisc.edu
- Gage Moreno: gkmoreno@wisc.edu
