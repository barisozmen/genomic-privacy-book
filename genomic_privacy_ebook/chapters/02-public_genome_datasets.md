# Chapter 2: Public Genome Datasets and Common File Formats

## 1. Public Genome Datasets

### Introduction

The past few decades have witnessed an explosion in the generation of genomic data. Publicly available genomic datasets are invaluable resources for researchers worldwide, driving discoveries in human health, evolution, agriculture, and many other fields. These datasets, often stemming from large-scale international collaborations, provide a foundation for understanding genetic variation, disease mechanisms, and the complex interplay of genes and environment. The open availability of such data promotes transparency, reproducibility, and accelerates scientific progress by allowing researchers to build upon existing knowledge and perform meta-analyses.

### Major International Consortia/Databases

A cornerstone of public genomic data accessibility is the work of international consortia that coordinate data submission, storage, and dissemination.

*   **INSDC (International Nucleotide Sequence Database Collaboration)**:
    The INSDC is a long-standing collaboration between three major public sequence repositories. Its primary role is to ensure that sequence data is freely available and that data submitted to any one of the member databases is shared among all three. This global effort prevents data fragmentation and provides a comprehensive, unified collection of nucleotide sequence information.
    *   **GenBank (NCBI - National Center for Biotechnology Information, USA)**:
        *   **Scope:** GenBank is a comprehensive public database of nucleotide sequences and their protein translations. It includes sequences submitted directly by researchers, as well as data from large-scale sequencing projects. Data types include DNA, RNA, and protein sequences, along with rich metadata such as source organism, collection date, experimental information, and publications.
        *   **Access:** Data can be accessed through the NCBI Entrez system, the NCBI Datasets portal (a newer interface for downloading sequence data and metadata), and via FTP for bulk downloads. Tools like BLAST allow sequence similarity searching against GenBank.
    *   **ENA (European Nucleotide Archive, EMBL-EBI - European Molecular Biology Laboratory-European Bioinformatics Institute)**:
        *   **Scope:** ENA provides a comprehensive record of the world's nucleotide sequencing information, covering raw sequencing data, assembled sequences, and functional annotation. It accepts data from small-scale experiments to large genome-sequencing projects. Data types are similar to GenBank, including reads, sequences, and associated metadata.
        *   **Access:** Data is accessible through the EMBL-EBI website via search tools, web services (APIs), and FTP for bulk downloads. ENA also provides tools for data submission and retrieval.
    *   **DDBJ (DNA Data Bank of Japan, National Institute of Genetics)**:
        *   **Scope:** DDBJ collects nucleotide sequence data primarily from Japanese researchers but also from other international contributors. It mirrors the data available in GenBank and ENA, ensuring global data synchronization.
        *   **Access:** Data can be accessed through web-based search tools, APIs, and FTP.

*   **Ensembl (EMBL-EBI & Wellcome Sanger Institute)**:
    Ensembl focuses on providing high-quality, automatically annotated genomes, primarily for vertebrate species but also expanding to other life forms. Its key role is in genome annotation, including gene prediction, regulatory elements, and comparative genomics. Ensembl integrates data from various sources, including INSDC databases, and provides tools for data visualization (e.g., Ensembl Genome Browser) and analysis. It's a crucial resource for researchers studying gene function, evolution, and genetic variation. Data is accessible via its website, BioMart data mining tool, REST APIs, and FTP.

### Specific Large-Scale Projects/Databases

Beyond the primary INSDC repositories, numerous large-scale projects have generated vast amounts of specific genomic data.

*   **1000 Genomes Project:**
    *   **Scope & Focus:** Completed in 2015, this landmark project aimed to create a detailed catalog of human genetic variation (SNPs, indels, structural variants) from diverse populations worldwide.
    *   **Data Types:** Whole-genome sequencing data, exome sequencing data, and genotype data for over 2,500 individuals.
    *   **Access:** Data is available through INSDC archives (ENA, GenBank, DDBJ), the International Genome Sample Resource (IGSR) portal, and cloud platforms like Amazon S3.

*   **TCGA (The Cancer Genome Atlas):**
    *   **Scope & Focus:** A comprehensive project to understand the molecular basis of cancer through large-scale genome sequencing and multi-omic analysis of over 30 different types of cancer.
    *   **Data Types:** Genomic (WGS, WES), epigenomic (DNA methylation), transcriptomic (RNA-Seq), and proteomic data, along with clinical information.
    *   **Access:** TCGA data is now part of the Genomic Data Commons (GDC) portal. Access to controlled-access data (containing potentially identifiable information) requires authorization (e.g., via dbGaP).

*   **UK Biobank:**
    *   **Scope & Focus:** A prospective cohort study with deep genetic and health information from half a million UK participants. It aims to improve the prevention, diagnosis, and treatment of a wide range of serious and life-threatening illnesses.
    *   **Data Types:** Genotyping array data, exome sequencing data (for a subset), whole-genome sequencing data (planned for all), extensive health records, lifestyle information, and imaging data.
    *   **Access:** Data is available to approved researchers for health-related research in the public interest. Applications are made through the UK Biobank Access Management System.

*   **gnomAD (Genome Aggregation Database):**
    *   **Scope & Focus:** Aggregates exome and genome sequencing data from a wide variety of large-scale sequencing projects and diverse populations, with a strong focus on removing individuals with severe pediatric diseases. It serves as a powerful reference for allele frequencies in the general population.
    *   **Data Types:** Allele frequencies, genotype counts, and summary statistics for millions of genetic variants.
    *   **Access:** Data is publicly accessible through the gnomAD browser and for bulk download.

*   **Other Notable Resources:**
    *   **GEO (Gene Expression Omnibus, NCBI):** A public functional genomics data repository supporting MIAME-compliant data submissions. Stores high-throughput gene expression data (e.g., microarray, RNA-Seq), methylation, and ChIP-seq data.
    *   **SRA (Sequence Read Archive, part of INSDC):** The primary archive for raw next-generation sequencing data. While part of INSDC, it's worth noting specifically due to the sheer volume of raw data it holds.

### General Access Mechanisms

Access to these public datasets is typically provided through:

*   **Web Portals:** Interactive websites with search functionalities, data browsers (e.g., Ensembl Genome Browser, UCSC Genome Browser, gnomAD browser), and visualization tools.
*   **APIs (Application Programming Interfaces):** Allow programmatic access to data, enabling automated queries and integration into bioinformatics pipelines. Examples include NCBI Entrez Direct (E-utilities) and Ensembl REST APIs.
*   **Bulk Downloads:** FTP sites or services like Aspera are often provided for downloading large datasets, such as entire genomes, alignment files, or variant call sets. Cloud-based platforms (e.g., AWS, Google Cloud) are also increasingly used for hosting and distributing large genomic datasets.

## 2. Genomic File Formats

### Introduction

The vast amounts of data generated by sequencing and other genomic technologies require standardized file formats. These formats ensure data interoperability between different software tools, facilitate data sharing among researchers, and provide a consistent way to represent complex biological information. Understanding these formats is crucial for anyone working with genomic data.

### FASTA

*   **Primary Purpose:** Represents nucleotide (DNA/RNA) or protein sequences. It's one of the simplest and most fundamental sequence formats.
*   **Common Use Cases:** Storing reference genomes, individual gene or protein sequences, contigs from genome assembly.
*   **Basic Structure:**
    *   A header line starting with `>` (greater-than symbol), followed by a sequence identifier and an optional description.
    *   The sequence itself, which can span multiple lines.
*   **Illustrative Example:**
    ```
    >sequence_id1 description of sequence 1
    ATGCGTAGCATCGATCGATCGATCGATCGATCGATCGATCG
    GCTAGCTAGCTAGCTAGCTAGCTAGCTAGCTAGCTAGCTAG
    >protein_id2 hemoglobin subunit alpha
    MVLSPADKTNVKAAWGKVGAHAGEYGAEALERMFLSFPTTK
    TYFPHFDLSHGSAQVKGHGKKVADALTNAVAHVDDMPNALS
    ALSDLHAHKLRVDPVNFKLLSHCLLVTLAAHLPAEFTPAV
    HASLDKFLASVSTVLTSKYR
    ```
*   **Popularity & Scenarios:** Foundational and universally supported by almost all bioinformatics tools that handle sequence data. Best for simple sequence representation without quality scores or alignment information.

### FASTQ

*   **Primary Purpose:** Stores raw sequencing reads from Next-Generation Sequencing (NGS) platforms, along with per-base quality scores.
*   **Common Use Cases:** Output from sequencing machines, input for read aligners, quality control assessment of raw reads.
*   **Basic Structure:** Each read is represented by four lines:
    1.  `@` followed by a sequence identifier and optional description (similar to FASTA header but starts with `@`).
    2.  The raw sequence (nucleotides).
    3.  `+` (plus sign), optionally followed by the same sequence identifier.
    4.  Base quality scores encoded as ASCII characters, corresponding to each base in the sequence.
*   **Illustrative Example:**
    ```
    @SEQ_ID_XYZ read_1 /1
    GATTTGGGGTTCAAAGCAGTATCGATCAAATAGTAAATCCATTTGTTCAACTCACAGTTT
    +
    !''*((((***+))%%%++)(%%%%).1***-+*''))**55CCF>>>>>>CCCCCCC65
    ```
*   **Popularity & Scenarios:** The standard format for raw sequencing reads from Illumina and other NGS platforms. Essential for downstream analyses like alignment and variant calling where base quality is important.
*   **Phred Quality Scores:** Quality scores (Q) are logarithmically related to the base-calling error probabilities (P): `Q = -10 log10(P)`. A Q30 score means a 1 in 1000 chance of an incorrect base call. Different encoding schemes exist (e.g., Sanger Phred+33, Illumina Phred+64), so it's important for tools to interpret them correctly. Sanger Phred+33 is the most common standard now.

### SAM (Sequence Alignment Map)

*   **Primary Purpose:** Represents the alignment of sequencing reads (or longer sequences) to a reference sequence.
*   **Common Use Cases:** Output from read aligners (e.g., BWA, Bowtie2), input for variant callers (e.g., GATK, Samtools), alignment visualization.
*   **Basic Structure:**
    *   **Header Section:** Optional lines starting with `@` that provide metadata about the reference sequences, alignment program, sorting order, etc. (e.g., `@SQ` for reference sequence dictionary, `@RG` for read group information).
    *   **Alignment Section:** Tab-delimited lines, each representing a single alignment. There are 11 mandatory fields:
        1.  `QNAME`: Query template NAME (read ID).
        2.  `FLAG`: Bitwise FLAG indicating alignment properties (e.g., paired, mapped, strand).
        3.  `RNAME`: Reference sequence NAME.
        4.  `POS`: 1-based leftmost mapping POSition.
        5.  `MAPQ`: MAPping Quality.
        6.  `CIGAR`: CIGAR string (e.g., `76M` for 76 matches/mismatches, `50M2I24M` for 50 matches, 2 insertions, 24 matches).
        7.  `RNEXT`: Ref. name of the mate/next read.
        8.  `PNEXT`: Position of the mate/next read.
        9.  `TLEN`: Observed Template LENgth.
        10. `SEQ`: Segment SEQuence (the read sequence).
        11. `QUAL`: ASCII of Phred-scaled base QUALity+33.
        Optional fields can follow the mandatory ones, in `TAG:TYPE:VALUE` format (e.g., `NM:i:1` for one mismatch).
*   **Illustrative Example (Alignment Section only):**
    ```
    read_ABC  163 chr1  10123 60  75M chr1  10345 298 AGCT...  IIII... NM:i:0 MD:Z:75 AS:i:75 XS:i:0
    read_DEF  83  chr1  10500 30  30M1I44M  chr1  10701 270 TGCA...  JJJJ... NM:i:1 MD:Z:30A44 AS:i:68
    ```
*   **Popularity & Scenarios:** The standard text-based format for storing read alignments. While human-readable, its large size makes BAM more practical for most applications.

### BAM (Binary Alignment Map)

*   **Primary Purpose:** The binary, compressed version of SAM.
*   **Common Use Cases:** Storage, processing, and exchange of read alignments. Preferred over SAM for most bioinformatics pipelines due to smaller size and efficient processing.
*   **Basic Structure:** Same information content as SAM, but encoded in a compressed binary format (BGZF - Blocked GNU Zip Format). BAM files are typically indexed (using a `.bai` file) to allow fast random access to alignments in specific genomic regions.
*   **Illustrative Example:** Not human-readable directly. Requires tools like `samtools view` to convert to SAM for inspection.
*   **Popularity & Scenarios:** The de facto standard for storing and working with aligned sequence data. Its indexed nature is crucial for efficient variant calling and visualization.

### CRAM (Compressed Reference-oriented Alignment Map)

*   **Primary Purpose:** A highly compressed alignment format that achieves significant size reduction by storing differences relative to a reference sequence.
*   **Common Use Cases:** Archival of large alignment datasets, reducing storage costs and data transfer times.
*   **Basic Structure:** Data is organized into containers, slices, and blocks. Compression relies on the reference sequence. Information identical to the reference is often omitted or encoded efficiently. Lossless CRAM stores all data, while lossy CRAM can discard certain information (e.g., quality scores) for even greater compression.
*   **Illustrative Example:** Not human-readable directly. Requires tools like `samtools view` (with the reference genome) to convert to SAM/BAM.
*   **Popularity & Scenarios:** Increasingly popular for large-scale projects and long-term storage due to its superior compression ratios compared to BAM. Requires the reference genome sequence for decompression.

### VCF (Variant Call Format)

*   **Primary Purpose:** Represents genetic variations, including single nucleotide polymorphisms (SNPs), insertions/deletions (indels), and structural variants (SVs).
*   **Common Use Cases:** Output from variant calling software, input for variant annotation and filtering tools, population genetics studies, clinical genetics.
*   **Basic Structure:**
    *   **Meta-information Section (Header):** Lines starting with `##` that define file format version, reference genome, contigs, and descriptions of `INFO`, `FILTER`, and `FORMAT` fields used in the data lines.
    *   **Header Line:** A single line starting with `#CHROM` that lists the column names.
    *   **Data Lines:** Tab-delimited lines, each representing a variant. There are 8 mandatory columns:
        1.  `CHROM`: Chromosome.
        2.  `POS`: 1-based starting position of the variant.
        3.  `ID`: Identifier (e.g., dbSNP rsID). `.` if missing.
        4.  `REF`: Reference allele.
        5.  `ALT`: Alternative allele(s). Multiple ALT alleles are comma-separated.
        6.  `QUAL`: Phred-scaled quality score for the assertion made in ALT.
        7.  `FILTER`: Filter status (e.g., `PASS`, or a specific filter code). `.` if no filter applied.
        8.  `INFO`: Additional information as key-value pairs (e.g., `DP=100` for read depth).
        If genotype data for samples is present, two additional columns are typically included:
        9.  `FORMAT`: Defines the data types and order for the sample-specific information (e.g., `GT:DP:AD` for Genotype, Depth, Allelic Depth).
        10. **Sample Columns:** For each sample, values corresponding to the `FORMAT` specification.
*   **Illustrative Example:**
    ```
    ##fileformat=VCFv4.2
    ##reference=file:///seq/references/1000GenomesPilot-NCBI36.fasta
    ##INFO=<ID=DP,Number=1,Type=Integer,Description="Total Depth">
    ##FORMAT=<ID=GT,Number=1,Type=String,Description="Genotype">
    #CHROM  POS     ID      REF     ALT     QUAL    FILTER  INFO            FORMAT          SAMPLE1         SAMPLE2
    chr1    10123   rs123   A       G       100     PASS    DP=50           GT:DP           0/1:50          0/0:45
    chr1    10500   .       C       CT      70      q10     DP=30;AF=0.3    GT:AD           0/1:10,20       1/1:0,25
    ```
*   **Popularity & Scenarios:** The standard format for representing genetic variants. Essential for almost all variant analysis pipelines.

### BCF (Binary VCF)

*   **Primary Purpose:** The binary, compressed version of VCF.
*   **Common Use Cases:** Storage and processing of large variant datasets.
*   **Basic Structure:** Similar to how BAM relates to SAM, BCF stores the same information as VCF but in a compressed binary format (BGZF). BCF files are also typically indexed (using `.csi` or `.tbi` files) for fast access to specific genomic regions.
*   **Illustrative Example:** Not human-readable directly. Requires tools like `bcftools view` to convert to VCF.
*   **Popularity & Scenarios:** Increasingly preferred over VCF for large studies due to smaller file sizes and faster processing, especially when indexed.

### GFF/GTF (General Feature Format / Gene Transfer Format)

*   **Primary Purpose:** Describes genes and other features of DNA, RNA, and protein sequences.
*   **Common Use Cases:** Representing gene models (exons, introns, UTRs), regulatory elements, repeats, and other genomic annotations. Input for visualization tools, RNA-Seq analysis (e.g., for read counting).
*   **Basic Structure:** Tab-delimited text file with 9 fields per line:
    1.  `seqid`: Name of the chromosome or scaffold.
    2.  `source`: Name of the program or database that generated the feature.
    3.  `type`: Type of feature (e.g., `gene`, `exon`, `CDS`, `mRNA`, `UTR`).
    4.  `start`: Start position of the feature (1-based).
    5.  `end`: End position of the feature (1-based).
    6.  `score`: A floating-point score. `.` if not applicable.
    7.  `strand`: `+` (forward), `-` (reverse), or `.` (not applicable).
    8.  `phase`: For CDS features, the phase (0, 1, or 2) indicates the reading frame. `.` otherwise.
    9.  `attributes`: A semicolon-separated list of tag-value pairs providing additional information (e.g., `gene_id "GENE001"; transcript_id "TX001"`).
*   **Differences:**
    *   **GFF2:** An older version. GTF is a refinement of GFF2.
    *   **GTF (Gene Transfer Format):** Commonly used by Ensembl and in RNA-Seq analysis (e.g., by Cufflinks/StringTie). It has stricter requirements for certain attributes like `gene_id` and `transcript_id`. Typically represents features like `exon`, `CDS`, `start_codon`, `stop_codon`, `UTR`.
    *   **GFF3:** A more recent and flexible version. Allows for a hierarchical structure of features using `ID` and `Parent` attributes, making it suitable for representing complex gene models and relationships between features. Supports a wider range of feature types.
*   **Illustrative Example (GTF-like):**
    ```
    chr1  ensembl gene      1000  5000  .  +  .  gene_id "ENSG001"; gene_name "MYGENE";
    chr1  ensembl transcript  1000  5000  .  +  .  gene_id "ENSG001"; transcript_id "ENST001";
    chr1  ensembl exon      1000  1500  .  +  .  gene_id "ENSG001"; transcript_id "ENST001"; exon_number "1";
    chr1  ensembl CDS       1200  1500  .  +  0  gene_id "ENSG001"; transcript_id "ENST001"; exon_number "1";
    chr1  ensembl exon      2000  2500  .  +  .  gene_id "ENSG001"; transcript_id "ENST001"; exon_number "2";
    chr1  ensembl CDS       2000  2400  .  +  1  gene_id "ENSG001"; transcript_id "ENST001"; exon_number "2";
    ```
*   **Popularity & Scenarios:** GFF3 is very flexible and good for complex annotations. GTF is widely used in RNA-Seq pipelines and for gene/transcript definitions. Choice often depends on the specific tools being used.

This chapter provides an overview of key public genomic datasets and the common file formats used to store and exchange genomic information. Understanding these resources and formats is fundamental for anyone venturing into the field of genomics and bioinformatics.
