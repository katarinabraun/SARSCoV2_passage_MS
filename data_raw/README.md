# Raw Data 

All raw data can be found at this bioproject: [PRJNA607948](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA607948/)    

This bioproject contains FASTQs that have been mapped to reference (MT039887.1) and converted from an alignment file-type back to a FASTQ. We did this to ensure we were not uploading any contaminating human reads. 

We have chosen to not upload the FASTQ files here because the files are quite large. 

The FASTQs from this bioproject can be fed directly into the ONT pipeline. 

The Illumina pipeline is configured to take in bams, instead of FASTQs, so these bam files to feed into the Illumina pipeline can be found in this repository – `data_raw/Illumina_bams/*`. 
