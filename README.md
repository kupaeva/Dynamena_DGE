# Dynamena_DGE
This reporitorium consist description of pipeline of differential gene expression analysis for non-model hydroid polyp Dynamena pumila.

### Aims of the project:

*De novo* assembly and analysis of transcriptomes of the *Dynamena pumila* hydroid polyp at different parts of the colony

### Goals of the project:

* Primary data processing
* Assembling the reference
* Prepare a reference
* Count the occurrence of genes in the reference
* Normalize data
* Annotate transcriptome
* Find something interesting


### In this project we used:
* fastp (v0.20.0)    
    * cut adapters, trim data, prepare row reads
* fastQC (v0.11.5)
    * data quality check
* kraken2 (v2.0.9)
    * filtering contamination
* bbnorm
    * digital normalization of data
* rnaSPAdes (v3.14.1) 
    * *de novo* transcriptome assembly
* BUSCO (v3.6)
    * assembly quality control
* trinityrnaseq (v2.8.6)
    * assembly quality control
* cd-hit-est (v4.8.1)
    * filtering similar transcripts
* TransDecoder (v5.5.0)
   * find orf in transcripts
* blast (v2.10.1)
   * annotation, target genes founding
* Trinotate (3.2.1)
   * annotation pipeline
* hmmscan (v03.1b2)
   * mapping reads to assembly
* tximport
   * import differential expression data to DEseq2 
* DEseq2
   * analysis of differential expression data
* pcaExplorer
   * data visualisation
* EnhancedVolcano
   * data visualisation
* pheatmap
   * data visualisation
   
### Our results

We prepared the base for the analysis of any genes, which may be involved in growth tip determination:
* assembled qualified reference transcriptome
* annotated it
* counted expression
* normalized data
* verified that the data met expectations.

After it, we analyzed housekeepeng genes and WNT repertoire:

![housekeepeng genes]: (https://github.com/kupaeva/Dynamena_DGE/blob/main/housekeepeng_genes.png "housekeepeng genes")


# Citation:
1.	Alexopoulos, H. et al. (2004) Evolution of gap junctions: the missing link?, Current Biology, 14(20), pp. R879–R880. doi: 10.1016/j.cub.2004.09.067.
2.	Andrews, S. (2010) FastQC A Quality Control Tool for High Throughput Sequence Data, Babraham Bioinformatics. Available at: www.bioinformatics.babraham.ac.uk/projects/fastqc/.
3.	Bagaeva, T. S. et al. (2019) сWnt signaling modulation results in a change of the colony architecture in a hydrozoan, Developmental Biology, 456(2). doi: 10.1016/j.ydbio.2019.08.019.
4.	Blighe K, Rana S, Lewis M (2020). EnhancedVolcano: Publication-ready volcano plots with enhanced colouring and labeling. R package version 1.8.0, https://github.com/kevinblighe/EnhancedVolcano.
5.	Bryant, D. M. et al. (2017) A Tissue-Mapped Axolotl De Novo Transcriptome Enables Identification of Limb Regeneration Factors, Cell Reports. Elsevier B.V., 18(3), pp. 762–776. doi: 10.1016/j.celrep.2016.12.063.
6.	Bushnell, B. https://jgi.doe.gov/data-and-tools/bbtools/ BBTools.
7.	Chen, S. et al. (2018) fastp: an ultra-fast all-in-one FASTQ preprocessor, Bioinformatics. Oxford University Press, 34(17), pp. i884–i890. doi: 10.1093/bioinformatics/bty560.
8.	Grabherr, M. G. et al. (2011) Full-length transcriptome assembly from RNA-Seq data without a reference genome, Nature Biotechnology. NIH Public Access, 29(7), pp. 644–652. doi: 10.1038/nbt.1883.
9.	Hensel, K. et al. (2014) Lineage-specific evolution of cnidarian Wnt ligands, Evolution and Development, 16(5), pp. 259–269. doi: 10.1111/ede.12089.
10.	Horin, C. et al. (2018) The genome of the jellyfish Clytia hemisphaerica and the evolution of the cnidarian life-cycle, pp. 1–41.
11.	HMMer http://hmmer.org/
12.	Kupaeva, D., Konorov, E. and Kremnyov, S. (2019) De novo transcriptome sequencing of the thecate colonial hydrozoan, Dynamena pumila, Marine Genomics. Elsevier, (July), p. 100726. doi: 10.1016/j.margen.2019.100726.
13.	Li, W. and Godzik, A. (2006) Cd-hit: A fast program for clustering and comparing large sets of protein or nucleotide sequences, Bioinformatics. Bioinformatics, 22(13), pp. 1658–1659. doi: 10.1093/bioinformatics/btl158.
14.	Love, M. I., Huber, W. and Anders, S. (2014) Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2, Genome Biology. BioMed Central Ltd., 15(12), p. 550. doi: 10.1186/s13059-014-0550-8.
15.	Marini, F. and Binder, H. (2019) PcaExplorer: An R/Bioconductor package for interacting with RNA-seq principal components, BMC Bioinformatics. BioMed Central Ltd., 20(1), p. 331. doi: 10.1186/s12859-019-2879-1.
16.	Nikolenko, S. I., Korobeynikov, A. I. and Alekseyev, M. A. (2013) BayesHammer: Bayesian clustering for error correction in single-cell sequencing, BMC Genomics. BioMed Central Ltd., 14(Suppl 1), p. S7. doi: 10.1186/1471-2164-14-S1-S7.
17.	Patro, R. et al. (2017) Salmon provides fast and bias-aware quantification of transcript expression, Nature Methods. Nature Publishing Group, 14(4), pp. 417–419. doi: 10.1038/nmeth.4197.
18.	Seppey, M., Manni, M. and Zdobnov, E. M. (2019) BUSCO: Assessing genome assembly and annotation completeness, in Methods in Molecular Biology. Humana Press Inc., pp. 227–245. doi: 10.1007/978-1-4939-9173-0_14.
19.	Soneson, C., Love, M. I. and Robinson, M. D. (2015) Differential analyses for RNA-seq: transcript-level estimates improve gene-level inferences, F1000Research. F1000 Research, Ltd., 4, p. 1521. doi: 10.12688/f1000research.7563.1.
20.	Transdecoder https://github.com/TransDecoder/TransDecoder/wiki
21.	Wood, D. E., Lu, J. and Langmead, B. (2019) Improved metagenomic analysis with Kraken 2, Genome Biology. BioMed Central Ltd., 20(1), p. 257. doi: 10.1186/s13059-019-1891-0.
