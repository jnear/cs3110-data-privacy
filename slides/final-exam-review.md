# Final Exam Topic List (Fall 2026)

# Format

- Open notes: bring as much printed material as you want
- Closed computers / phones / everything else
- The final is cumulative, with approximately 60% of points covering material taught after Exam 2
- Liberal partial credit applied - if unsure, explain your reasoning (even for multiple-choice questions)

# Topics Since Exam 2

## Local Differential Privacy

- Tradeoffs of local differential privacy
  - Huge benefit: threat model
  - Huge drawback: accuracy
- Randomized response
- Unary encoding

## Synthetic Data

- Range queries
- Synthetic representations vs synthetic data
- The histogram representation for range queries
- Tradeoffs in the histogram representation (e.g. large vs small bins)
- Using histograms as probability distributions to generate synthetic data
- 1-way vs 2-way vs n-way marginal distributions
  - Advantage: n-way preserves correlation
  - Disadvantage: as n grows, counts shrink, and noise becomes overwhelming
- Challenge of dimensionality

## Privacy in Deep Learning and Practical Systems

- Privacy risks in deep learning
- Gradient clipping and noise in DP-SGD
- Composition and privacy accounting in practical systems
- Utility, privacy, and implementation tradeoffs

## Open Challenges

- Challenges in high-dimensional data, machine learning, and synthetic data
- Choosing mechanisms, units of privacy, and privacy budgets for real applications

## Tradeoffs and Lessons Learned

- Utility vs. Privacy
  - Still challenging to navigate
  - Still unclear what ε is "good"
- Clipping
  - Noise scale vs information loss
  - Prefer to avoid information loss
- Mechanism Choice
  - For small number of queries, Laplace mechanism has the best accuracy
  - For many queries at once, use the vector-valued Gaussian mechanism and L2 sensitivity
- Composition
  - Advanced composition is *worse* below ~70 queries
  - RDP and zCDP are always good, but don't offer much benefit for just a few queries
  - When composition matters, prefer RDP or zCDP
- Special tricks to use whenever possible:
  - Sparse Vector Technique (AboveThreshold)
  - Report Noisy Max
- Dimensionality
  - High-dimensional things are hard!
  - Contingency tables
  - Large workloads of queries
  - High-dimensional machine learning (e.g. deep learning)
  - High-dimensional synthetic data (e.g. k-way marginals for large k)

# Cumulative Topics

- Informal privacy, de-identification, re-identification, and k-anonymity
- Differential privacy, sensitivity, composition, clipping, and histograms
- Approximate DP, privacy variants, and the Gaussian mechanism
- Exponential mechanism, sparse vector technique, and differentially private machine learning
