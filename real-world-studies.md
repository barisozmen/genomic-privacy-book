# Real World Studies

## Federated GWAS + FHE
[Paper. 2021, Truly privacy-preserving federated analytics for precision medicine with multiparty homomorphic encryption](https://www.nature.com/articles/s41467-021-25972-y)

This paper presents FAMHE (Federated Analytics with Multiparty Homomorphic Encryption), a privacy-preserving system for analyzing medical data distributed across multiple healthcare institutions. Here are the key ideas and methods:

## Core Problem
Healthcare data is scattered across institutions but cannot be centralized due to privacy regulations like GDPR. Traditional federated learning approaches still leak sensitive information through shared intermediate results.

## Key Innovation: FAMHE System
The authors developed a novel approach that combines:
- **Multiparty Homomorphic Encryption (MHE)**: Enables computation on encrypted data without decryption
- **Distributed computation**: Each institution computes locally on their cleartext data, then encrypts results
- **Collective aggregation**: Encrypted results are combined without revealing intermediate values

## FAMHE Workflow
1. **Local Computation & Encryption**: Each data provider computes on their local data and encrypts results with a collective public key
2. **Collective Aggregation**: Encrypted results are combined homomorphically
3. **Iteration**: Process repeats for iterative algorithms
4. **Collective Key Switching**: Final result is switched from collective encryption to querier's key
5. **Decryption**: Only the querier can decrypt the final result

## Optimization Techniques
- **SIMD (Single Instruction, Multiple Data)**: Parallel computation on vector values within ciphertexts
- **Edge computing**: Maximizes local cleartext computation to minimize encrypted operations
- **Polynomial approximation**: Replaces complex operations like matrix inversion with polynomial functions
- **Ciphertext packing**: Optimizes data organization for efficient computation

## Demonstrated Applications

### 1. Kaplan-Meier Survival Analysis
- Reproduced cancer survival curves from Samstein et al. study
- Analyzed tumor mutational burden (TMB) as predictor of treatment response
- Achieved identical results to centralized analysis in <12 seconds

### 2. Genome-Wide Association Studies (GWAS)
- Reproduced HIV-1 viral load study from McLaren et al.
- Two approaches developed:
  - **FAMHE-GWAS**: Exact linear regression with no accuracy loss
  - **FAMHE-FastGWAS**: Faster execution with minimal accuracy trade-off
- Analyzed 1,857 patients with 4+ million genetic variants in <5 hours

## Key Advantages
- **Perfect accuracy**: No loss compared to centralized analysis
- **Strong privacy**: Only encrypted data shared between institutions
- **Scalability**: Efficient scaling with number of institutions, patients, and variants
- **Regulatory compliance**: Encrypted data may be considered "anonymous" under GDPR

## Technical Implementation
- Built on Lattigo cryptographic library
- 128-bit security level
- Supports up to 96 data providers
- Parallelized computation across multiple levels

## Significance
This work demonstrates that sophisticated biomedical analyses can be performed across institutions without compromising privacy or accuracy, potentially enabling larger-scale medical research while maintaining regulatory compliance.

Why this matters:
- Rare disease gene discovery
  - There are thousands of rare diseases with no treatment because each hospital sees only a handful of cases
- Regulatory future-proofing
  - Privacy laws are only getting stricter. By running analytics directly on encrypted data, you *comply by default*—no need for trust, just math.
- Trust & participation
  - people hesitate to donate their genome to research. What if you could say: *“We can run life-saving studies—without ever seeing your DNA”*?
- Underrepresented populations
  - unique variants from small populations





