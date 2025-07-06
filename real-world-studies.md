# Real World Studies

## Federated GWAS + FHE
[Paper. 2021, Truly privacy-preserving federated analytics for precision medicine with multiparty homomorphic encryption](https://www.nature.com/articles/s41467-021-25972-y)

In traditional GWAS, researchers look for statistical associations between genetic variants (SNPs) and diseases. This requires access to massive datasets—ideally, *millions* of genomes from diverse populations.

Federated GWAS solves this by running the analysis over encrypted data from multiple sites—*without ever decrypting it*.

**🔒 How it works:**

1. Hospitals encrypt their genomic + phenotype datasets using FHE.
2. Encrypted datasets are sent to a central server (or better, computed peer-to-peer).
3. A research team uploads their GWAS algorithm.
4. The computation is executed homomorphically across all sites.
5. The researcher receives only association statistics—no genomes are revealed.

### Why This Matters

- Rare disease gene discovery
  - There are thousands of rare diseases with no treatment because each hospital sees only a handful of cases
- Regulatory future-proofing
  - Privacy laws are only getting stricter. By running analytics directly on encrypted data, you *comply by default*—no need for trust, just math.
- Trust & participation
  - people hesitate to donate their genome to research. What if you could say: *“We can run life-saving studies—without ever seeing your DNA”*?
- Underrepresented populations
  - unique variants from small populations




