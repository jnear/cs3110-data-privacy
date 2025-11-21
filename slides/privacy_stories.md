
# Real-world Privacy Stories and their Lessons

## Census Bureau

- [Title 13 requires](https://uslawexplained.com/title_13_of_the_u.s._code) the US Census to [prevent disclosure of personal information](https://www.census.gov/about/policies/privacy/data_stewardship/title_13_-_protection_of_confidential_information.html): sworn employees risk jail time if it gets out
- Traditional approach to [statistical disclosure control](https://en.wikipedia.org/wiki/Statistical_disclosure_control):
  - Aggregations with small counts suppressed
  - Swapping (how? [it's a secret!](https://arxiv.org/pdf/2306.07521))
- The [Census reconstruction attack](https://www.census.gov/library/working-papers/2023/adrm/CES-WP-23-63.html) reconstructed original rows for 50-80% of US persons
  - More accessible [slides available here](https://www.census.gov/data/academy/webinars/2021/disclosure-avoidance-series/simulated-reconstruction-abetted-re-identification-attack-on-the-2010-census.html)
  - Lesson: aggregation + swapping is not an effective defense
- [TopDown algorithm](https://www2.census.gov/library/publications/decennial/2020/census-briefs/c2020br-04.pdf) ensures differential privacy and reduces variance
  - It publishes multiple overlapping histograms (so it splits the privacy budget)
  - It uses zero-concentrated DP for accounting and Gaussian noise for privacy
- Census data users [did not like differential privacy](https://pmc.ncbi.nlm.nih.gov/articles/PMC11105149/) (some [really did not like it](https://www.jstor.org/stable/pdf/26723980.pdf))
  - Differential privacy may harm small groups via bias or variance or both!
  - Census set epsilon [quite large](https://www.census.gov/newsroom/press-releases/2021/2020-census-key-parameters.html) to address questions about data quality
  - Lesson: it's difficult to set epsilon! Multiple groups need to work together (e.g. data users and data producers); many stakeholders don't understand differential privacy; incentive structures are often disjoint
  - Lesson: there's a risk of [privacy theater](https://dl.acm.org/doi/10.1145/3555762) associated with differential privacy
- Differential privacy [has become a scapegoat for political fights](https://archive.ph/tXL4n)
  - Alabama [sued the Census Bureau](https://www.brennancenter.org/sites/default/files/2021-03/Complaint_%202021-03-11_0.pdf) in 2021
  - More recently, [this](https://archive.ph/hAwvE) and [this](https://americarenewing.com/issues/differential-privacy-in-the-2020-census-explained/)
  - Lesson: differential privacy is hard to explain and easy to scapegoat
- Most data (definitely Census data!) is [already noisy](https://desfontain.es/blog/noisy-data.html), even without privacy protection
  - The decennial census has [major sources of bias and variance](https://www.census.gov/newsroom/press-releases/2022/2020-census-estimates-of-undercount-and-overcount.html) introduced by the collection process
  - This problem is [especially bad for young children](https://www.census.gov/library/visualizations/interactive/net-coverage-error-young-children.html)
  - For statisticians, bias is **much scarier** than variance (or should be!)
    - But: no good way to disentangle these
    - Statisticians often ignore error entirely
  - Lesson: existing sources of error are often larger (and more bias-y) than differential privacy noise
  - Lesson: [communicating about error is really difficult](https://www.pnas.org/doi/pdf/10.1073/pnas.2302491120)!

## Unit of Privacy in Google Mobility Data

- ["Hierarchical organization of urban mobility and its connection with city livability"](https://www.nature.com/articles/s41467-019-12809-y) performed an analysis of a differentially private dataset
  - The dataset used a complicated unit of privacy (not person-level)
  - The paper wasn't completely clear about the unit of privacy
- ["On the difficulty of achieving Differential Privacy in practice: user-level guarantees in aggregate location data"](https://www.nature.com/articles/s41467-021-27566-0) claimed (carefully, because it was misleading) to "break" the differential privacy guarantee
- [A reply by the original authors](https://www.nature.com/articles/s41467-021-27567-z) clarified the unit of privacy
- Lesson: communicating about differential privacy is hard, even for experts!
- Lesson: unit of privacy matters at least as much as epsilon!

## Unit of Privacy in Apple's Emoji System

- [Apple uses local DP for emoji popularity](https://www.apple.com/privacy/docs/Differential_Privacy_Overview.pdf) with a user-day privacy unit
- [There is actually an attack](https://www.usenix.org/conference/usenixsecurity22/presentation/gadotti) on this system, that leverages the weak privacy unit
- Lesson: units of privacy other than user-level are dangerous!

## Units of Privacy in General

- [Lots of deployments have event-level units of privacy!](https://registry.opendp.org/deployments-registry/)
- This is a worrying trend that increases the risk of [privacy theater](https://dl.acm.org/doi/10.1145/3555762)

## Units of Privacy in Machine Learning

- In most systems, unit of privacy is "one training example"
- [VaultGemma](https://research.google/blog/vaultgemma-the-worlds-most-capable-differentially-private-llm/) uses a "sequence-level" unit of privacy
- If you write a book, you're definitely not getting person-level (or even book-level) privacy!
- [User-level training is more difficult](https://arxiv.org/abs/2406.14322) than other units

## Combining Cryptography with Differential Privacy

- Secure aggregation: individuals submit encrypted values; untrusted server computes and decrypts the sum, but can't view individual submissions
- [Google's Gboard](https://research.google/blog/improving-gboard-language-models-via-private-federated-analytics/) uses [central-model noise with secure aggregation](https://research.google/blog/distributed-differential-privacy-for-federated-learning/)
- [Apple memories](https://machinelearning.apple.com/research/scenes-differential-privacy) also uses secure aggregation
