# Exam 2 Topic List (Fall 2026)

# Format

- Open notes: bring as much printed material as you want
- Closed computers / phones / everything else
- Should take only 30-40 minutes
- Liberal partial credit applied - if unsure, explain your reasoning (even for multiple-choice questions)

# Topics

## Parallel Composition

- Definition / theorem
- Histograms and their sensitivity

## (ε, δ)-Differential Privacy

- Definition
- Gaussian mechanism
- L1 / L2 sensitivity of vector-valued functions
- Advanced composition
- Advantages and disadvantages (e.g. failure probability)

## Variants of Differential Privacy

- Advantages compared to ε, (ε,δ)-DP
- Rényi DP
- Zero-concentrated DP
- Conversion from variants to (ε,δ)-DP

## Algorithm Design

- Exponential mechanism
- Sparse vector technique
- Splitting the privacy budget

## Differentially Private Machine Learning

- Why machine learning models can memorize sensitive training data
- Gradient perturbation (noisy gradient descent)
  - What is gradient descent
  - What is the format of a linear model
  - How to bound the sensitivity of the gradient (clipping the gradient's L2 norm)
  - Composition issues and best privacy variants

## Local Differential Privacy

- Tradeoffs of local differential privacy
  - Huge benefit: threat model
  - Huge drawback: accuracy
- Randomized response
- Unary encoding

## Units of Privacy

- Definition (in terms of neighboring datasets)
- Evaluating a unit of privacy: "user-level" vs others
- Common units
  - User-level (individual-level)
  - Row-level (event-level)
  - User-day-level
  - User-month-level
- Transforming the unit of privacy
  - Bounding user contribution & adjusting sensitivity
