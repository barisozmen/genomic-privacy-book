# Glossary of Terms

This glossary provides definitions for key cryptographic, genomic, and technical terms used throughout this book.

---

**A**

*   **Allele:** One of two or more versions of a DNA sequence (a single base or a segment of bases) at a given genomic location.
*   **Allele Frequency:** The relative frequency of an allele at a particular locus in a population.
*   **API (Application Programming Interface):** A set of rules and protocols that allows different software applications to communicate with each other.
*   **ASIC (Application-Specific Integrated Circuit):** A type of integrated circuit chip customized for a particular use, rather than intended for general-purpose use.
*   **Abstract Algebra:** A branch of mathematics that studies algebraic structures such as groups, rings, and fields. Foundational for FHE.
*   **APOE ε4:** A specific genetic variant (allele) of the APOE gene that is a significant risk factor for developing Alzheimer's disease.

**B**

*   **BAM (Binary Alignment Map):** A compressed binary format for storing sequence alignment data, derived from SAM format.
*   **Batching (in FHE):** A technique that allows multiple plaintext messages to be packed into a single ciphertext, enabling SIMD (Single Instruction, Multiple Data) operations for better efficiency.
*   **Biobank:** A type of biorepository that stores biological samples (usually human) for use in research.
*   **Bootstrapping (in FHE):** A process in Fully Homomorphic Encryption that "refreshes" a ciphertext whose noise has grown too large, allowing for an arbitrary number of computations. It homomorphically evaluates the decryption circuit.
*   **BRCA1/BRCA2:** Human genes that produce tumor suppressor proteins. Mutations in these genes are linked to an increased risk of breast, ovarian, and other cancers.
*   **BFV Scheme (Brakerski-Fan-Vercauteren):** An FHE scheme that supports exact integer arithmetic.
*   **BGV Scheme (Brakerski-Gentry-Vaikuntanathan):** An FHE scheme that supports exact integer arithmetic, based on Ring-LWE.
*   **Bulletproofs:** A type of non-interactive zero-knowledge proof that does not require a trusted setup and is efficient for proving statements about ranges or arithmetic circuits.

**C**

*   **Circuit (Cryptographic):** A representation of a computation as a sequence of interconnected gates (e.g., arithmetic or Boolean gates), often used as input for ZKP systems.
*   **Ciphertext:** Data that has been encrypted.
*   **CKKS Scheme (Cheon-Kim-Kim-Song):** An FHE scheme that supports approximate arithmetic on real or complex numbers, widely used for privacy-preserving machine learning.
*   **Cloud Computing:** The delivery of computing services—including servers, storage, databases, networking, software, analytics, and intelligence—over the Internet (“the cloud”).
*   **Co-design (Algorithm-Hardware):** A design approach where algorithms and the hardware they run on are developed in tandem to optimize performance.
*   **Completeness (ZKP Property):** A property of ZKPs ensuring that if a statement is true, an honest prover can convince an honest verifier.
*   **CRAM:** A compressed file format for storing aligned sequencing reads, typically offering better compression than BAM by using the reference sequence.

**D**

*   **DAO (Decentralized Autonomous Organization):** An organization represented by rules encoded as computer programs (smart contracts) that are transparent, controlled by members, and not influenced by a central authority.
*   **Data Union:** A model where individuals pool their data (or access to it) and collectively bargain for its use, often sharing in the derived value.
*   **dbGaP (Database of Genotypes and Phenotypes):** A NCBI database designed to archive and distribute data from studies that have investigated the interaction of genotype and phenotype. Access is controlled.
*   **De-identification:** The process of removing or obscuring personally identifiable information from data. Often insufficient for genomic data due_to its inherent identifiability.
*   **Differential Privacy:** A system for publicly sharing information about a dataset by describing the patterns of groups within the dataset while withholding information about individuals. Involves adding calibrated noise.
*   **DNA (Deoxyribonucleic Acid):** The molecule that carries genetic information for the development, functioning, growth, and reproduction of all known organisms.

**E**

*   **ENA (European Nucleotide Archive):** A repository providing free and unrestricted access to annotated DNA and RNA sequences, part of the INSDC.
*   **Encryption:** The process of converting information or data into a code, especially to prevent unauthorized access.
*   **Ensembl:** A genomic data resource that provides genome annotation and browsers.
*   **EVM (Ethereum Virtual Machine):** A Turing-complete virtual machine that executes smart contracts on the Ethereum blockchain. "Confidential EVM" refers to EVM-compatible systems with added privacy features.

**F**

*   **FASTQ:** A text-based file format for storing both a biological sequence (usually nucleotide sequence) and its corresponding quality scores.
*   **Federated Learning:** A machine learning technique that trains an algorithm across multiple decentralized edge devices or servers holding local data samples, without exchanging the data samples themselves.
*   **FHE (Fully Homomorphic Encryption):** A form of encryption that allows computations to be performed directly on encrypted data without requiring decryption.
*   **FHEW:** An early FHE scheme notable for fast bootstrapping of Boolean gates.
*   **FPGA (Field-Programmable Gate Array):** An integrated circuit designed to be configured by a customer or a designer after manufacturing—hence "field-programmable."

**G**

*   **GA4GH (Global Alliance for Genomics and Health):** An international organization that aims to enable responsible genomic data sharing for the benefit of human health.
*   **GenBank:** The NIH genetic sequence database, an annotated collection of all publicly available DNA sequences, part of the INSDC.
*   **Genome:** An organism's complete set of DNA, including all of its genes.
*   **Genomic Beacon:** A web service that allows users to query a database for the presence of a specific allele without revealing other information about the dataset. Can still pose privacy risks.
*   **Genotype:** The genetic constitution of an individual organism, specifically the set of alleles it possesses.
*   **GINA (Genetic Information Nondiscrimination Act):** A U.S. federal law that protects individuals from genetic discrimination in health insurance and employment.
*   **gnomAD (Genome Aggregation Database):** A database of aggregated exome and genome sequencing data from a large number of individuals, used as a reference for allele frequencies.
*   **GWAS (Genome-Wide Association Study):** An observational study of a genome-wide set of genetic variants in different individuals to see if any variant is associated with a trait.

**H**

*   **Hardware Acceleration:** The use of specialized computer hardware to perform some functions more efficiently than is possible in software running on a general-purpose CPU.
*   **Hardware Wallet:** A physical device that stores a user's private keys securely, often used for cryptocurrencies.
*   **HIPAA (Health Insurance Portability and Accountability Act):** A U.S. federal law that provides data privacy and security provisions for safeguarding medical information.
*   **Homomorphic Encryption:** A type of encryption that allows specific types of computations (e.g., addition or multiplication) to be performed on ciphertexts. FHE is a type that allows arbitrary computations.
*   **HSM (Hardware Security Module):** A physical computing device that safeguards and manages digital keys for strong authentication and provides cryptoprocessing.

**I**

*   **Immutable:** Unchanging over time or unable to be changed. Genomic data is largely immutable.
*   **INSDC (International Nucleotide Sequence Database Collaboration):** A long-standing collaboration between DDBJ (Japan), ENA (Europe), and GenBank (USA) for sharing nucleotide sequence data.

**K**

*   **k-Anonymity:** A property of data where each record is indistinguishable from at least k-1 other records based on a set of quasi-identifiers.

**L**

*   **Lattice-based Cryptography:** A class of cryptographic primitives whose security relies on the presumed hardness of certain problems on point lattices. Many modern FHE schemes are lattice-based.
*   **LWE (Learning With Errors):** A computationally hard problem that is the foundation for many modern cryptographic systems, including some FHE schemes. Ring-LWE is a variant over polynomial rings.

**M**

*   **Modular Arithmetic:** A system of arithmetic for integers, where numbers "wrap around" upon reaching a certain value—the modulus.
*   **Multi-Party Computation (MPC) / Secure Multi-Party Computation (SMPC):** A subfield of cryptography that allows multiple parties to jointly compute a function over their inputs while keeping those inputs private.

**N**

*   **Noise (in FHE):** A small error term introduced during FHE encryption that grows with homomorphic operations. If noise grows too large, the ciphertext becomes undecryptable. Bootstrapping resets this noise.
*   **NTT (Number Theoretic Transform):** A mathematical transform used in many lattice-based cryptographic schemes (including FHE) for efficient polynomial multiplication.

**P**

*   **Paillier Cryptosystem:** A partially homomorphic encryption scheme that is additively homomorphic.
*   **Penetrance (Genetic):** The proportion of individuals carrying a particular variant of a gene (allele or genotype) who also express an associated trait (phenotype).
*   **PET (Privacy-Enhancing Technology):** Technologies that embed privacy and data protection principles into information systems.
*   **Pharmacogenomics (PGx):** The study of how genes affect a person's response to drugs.
*   **Phenotype:** The set of observable characteristics of an individual resulting from the interaction of its genotype with the environment.
*   **Plaintext:** Data in its original, unencrypted form.
*   **Polynomial Commitment Scheme:** A cryptographic primitive that allows a prover to commit to a polynomial and later prove evaluations of that polynomial at specific points. Used in some ZKP systems.
*   **Private Key (Secret Key):** In asymmetric cryptography, the key that is kept secret by its owner. In FHE, it's used for decryption.
*   **Programmable Bootstrapping (TFHE):** A feature of the TFHE scheme that allows arbitrary functions to be evaluated homomorphically during the bootstrapping process itself, with high efficiency.
*   **Public Key Cryptography:** A cryptographic system that uses pairs of keys: public keys, which may be disseminated widely, and private keys, which are known only to the owner.
*   **Public Key:** In asymmetric cryptography, the key that can be shared publicly without compromising security. In FHE, it's used for encryption.

**Q**

*   **Quasi-identifier:** Pieces of information that are not unique by themselves but can become identifying when combined (e.g., birth date, ZIP code, gender).

**R**

*   **R1CS (Rank-1 Constraint System):** A format for representing computational problems as a set of constraints, often used to construct circuits for zk-SNARKs.
*   **Ring-LWE (Ring Learning With Errors):** A variant of the LWE problem defined over polynomial rings, often leading to more efficient cryptographic constructions.
*   **RSA Cryptosystem:** One of the first public-key cryptosystems, widely used for secure data transmission. It is multiplicatively homomorphic.

**S**

*   **SAM (Sequence Alignment Map):** A text-based format for storing biological sequences aligned to a reference sequence.
*   **Secure Enclave:** A hardware-based security feature in modern CPUs that provides an isolated execution environment for sensitive computations and data.
*   **Self-Custody:** The practice of individuals directly controlling their own cryptographic keys and digital assets, without relying on third-party custodians.
*   **Side-Channel Attack:** An attack based on information gained from the physical implementation of a cryptosystem, rather than brute force or theoretical weaknesses in the algorithms (e.g., timing information, power consumption).
*   **SIMD (Single Instruction, Multiple Data):** A class of parallel computers in Flynn's taxonomy. It describes computers with multiple processing elements that perform the same operation on multiple data points simultaneously.
*   **SMPC (Secure Multi-Party Computation):** See Multi-Party Computation.
*   **SNP (Single Nucleotide Polymorphism):** A variation at a single position in a DNA sequence among individuals.
*   **SNARK (Succinct Non-Interactive Argument of Knowledge):** See zk-SNARK.
*   **Soundness (ZKP Property):** A property of ZKPs ensuring that if a statement is false, a dishonest prover cannot (except with negligible probability) convince an honest verifier that it is true.
*   **SRA (Sequence Read Archive):** A public repository for DNA sequencing data, particularly raw reads.
*   **STARK (Scalable Transparent Argument of Knowledge):** See zk-STARK.
*   **Structural Variant (SV):** A large-scale mutation affecting a significant portion of a chromosome, such as duplications, deletions, inversions, or translocations.

**T**

*   **TCGA (The Cancer Genome Atlas):** A landmark cancer genomics program that molecularly characterized over 20,000 primary cancer and matched normal samples spanning 33 cancer types.
*   **TEE (Trusted Execution Environment):** A secure area of a main processor that guarantees code and data loaded inside to be protected with respect to confidentiality and integrity.
*   **TFHE (Fast Fully Homomorphic Encryption over the Torus):** An FHE scheme known for its efficient bootstrapping, particularly for Boolean operations.
*   **Threshold Cryptography:** Cryptographic schemes where keys or functionalities are distributed among multiple parties, and a certain threshold of parties is required to perform an operation (e.g., decrypt, sign).
*   **TPM (Trusted Platform Module):** A dedicated microcontroller designed to secure hardware through integrated cryptographic keys.
*   **Trusted Setup (for ZKPs):** A procedure required by some ZKP systems (like many zk-SNARKs) to generate public parameters. If the randomness used in this ceremony is compromised, the soundness of the proof system can be broken.

**U**

*   **UK Biobank:** A large-scale biomedical database and research resource containing in-depth genetic and health information from half a million UK participants.

**V**

*   **VCF (Variant Call Format):** A text file format for storing gene sequence variations.
*   **Verifier (ZKP):** The party in a zero-knowledge proof protocol that checks the validity of a proof provided by the prover.

**Z**

*   **Zero-Knowledge (ZKP Property):** A property of ZKPs ensuring that the verifier learns nothing beyond the truth of the statement being proven.
*   **ZKP (Zero-Knowledge Proof):** A cryptographic protocol by which one party (the prover) can prove to another party (the verifier) that they know a value x, without conveying any information apart from the fact that they know the value x.
*   **zk-SNARK (Zero-Knowledge Succinct Non-Interactive Argument of Knowledge):** A type of ZKP that produces very small proofs and is fast to verify, but often requires a trusted setup.
*   **zk-STARK (Zero-Knowledge Scalable Transparent Argument of Knowledge):** A type of ZKP that requires no trusted setup (transparent) and is designed to be scalable, though proofs can be larger than SNARKs.

---
*Previous: [Chapter 12: Concluding Perspectives and Future Horizons](12-challenges_future.md)*
