# DGE-analysis (macrophage polarization)

Differential gene expression analysis with DESeq2 and limma-voom
Data taken from the following study [1]

Count matrices and preprocessing perfomerd in Galaxy
DESeq and limma-voom analysis performed in R (Jupyter notebook w/R core in Google colab).

Galaxy processing steps included: 
Workflow 1: QC pipeline
 (1) Data download (faster download from NCBI) 
 (2) Initial QC (fastqc and multiqc) 
 (3) Adapter trimming (Cutadapt/Trimgallore) 
 (4) Advanced QC (Gene  body coverage, Infer experiment, Read distribution, RNA fragment size) 
Workflow 2: Mapping and count matrix creation
 (1) Map to reference (Bowtie) 
 (2) Count features (featureCounts) 
 (3) Create count matrix

R processing included:
Jupyter notebook 1 -  DESeq2 analysis (R core):
(1) Create a DESeq2 data object
(2)	Run DESeq2 analysis
(3) GO enrichment analysis
Jupyter notebook 2 – limma voom analysis (R core)
(1) Create DGE object
(2) Create plots (MDS, scree)
(3) Normalize data
(4) Create design matrix and contrasts
(5) Perform additional filtering 
(6) Perform voom transformation
(6) Fit linear model
(7) Apply contrasts
(8) Perform DE analysis
(9) Plots


References: 
[1] NCBI project, PRJNA258286 - Bone marrow-derived macrophages (BMDMs) treated with or without LPS and IFNr in the presence or absence of Wy14643
