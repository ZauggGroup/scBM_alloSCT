# scBM_alloSCT

Scripts for analysis and Figures which are part of the Manuscript with title:
The remission status of AML patients post alloSCT is associated with a distinct single-cell bone marrow T cell signature

Sample doconvolution was performed using souporcell with the commands below:

singularity exec -B /g/scb2/zaugg/amathiou/2020Dec_scBM_Tcells/:/g/scb2/zaugg/amathiou/ souporcell.sif souporcell_pipeline.py -i 1.Counts/SI-GA-D11/outs/possorted_genome_bam.bam  -f refdata-cellranger-GRCh38-3.0.0/fasta/genome.fa -t 8 -o 2.demultiplexing_souporcell/SI-GA-D11 -k 3 -b barcodes_SI-GA-D11.tsv --ploidy 2 --common_variants genome1K.phase3.SNP_AF5e4.chr1toX.hg38.vcf --skip_remap T

singularity exec -B /g/scb2/zaugg/amathiou/2020Dec_scBM_Tcells/:/g/scb2/zaugg/amathiou/ souporcell.sif souporcell_pipeline.py -i 1.Counts/SI-GA-D10/outs/possorted_genome_bam.bam -f refdata-cellranger-GRCh38-3.0.0/fasta/genome.fa -t 8 -o 2.demultiplexing_souporcell/SI-GA-D10 -k 6 -b barcodes_SI-GA-D10.tsv --ploidy 2 --common_variants genome1K.phase3.SNP_AF5e4.chr1toX.hg38.vcf --skip_remap T


