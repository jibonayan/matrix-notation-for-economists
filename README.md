# Matrix Notation for Economists

A primer for economists on reading econometrics in both summation and matrix notation, with worked derivations, translation drills and Python checks of every identity.

- **Author** Jibonayan Raychaudhuri
- **Version** 26 October 2026
- **Licence** [Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/)

**Read the primer** [2026-10-26_Matrix_Notation.pdf](2026-10-26_Matrix_Notation.pdf)

## Why this primer exists

Econometrics is written in two languages. Greene's *Econometric Analysis* derives least squares in matrix algebra. Wooldridge's *Introductory Econometrics* derives most of the same results with sums and scalars. Journal articles switch between the two from one line to the next. A reader fluent in only one system reads half of the literature.

This primer teaches economists to translate in both directions. Every result appears twice. The cross-product matrix **X′X**, for example, is shown as rows times columns and as a sum of outer products, one per observation. The second reading looks clumsy on paper. It is the reading that underpins asymptotic theory and the one that makes estimation feasible when the data will not fit in memory.

## Contents

The document runs in order, and readers who know the foundations can start at any section.

1. Scalars, vectors and matrices
2. Indexing
3. Sigma notation, with rules for single and double sums and for selecting parts of an array
4. Matrix notation
5. Index notation, free and dummy indices, and the Einstein summation convention
6. Translation rules from summation to matrix notation, the Kronecker delta and products in index form
7. The linear regression model, including OLS, seemingly unrelated regressions, pooled panels and the heteroskedasticity-consistent variance
8. Summing vectors and the centering matrix
9. Matrices of functions
10. Matrix calculus, including the Jacobian, the Hessian, the two workhorse derivatives and the normal equations
11. Notation at a glance
12. Translation drills with answers
13. From notation to computation in Python

Boxes headed *Check your understanding* set short exercises. Boxes headed *From the archive* carry historical notes on Gauss, Sylvester and Cayley, Einstein, Hollerith, Legendre and the programmers of ENIAC. The historical notes are not examinable.

## The Python section

The final section checks the algebra numerically with NumPy. It computes **X′X** three ways, solves the normal equations, confirms that residuals are orthogonal to the regressors and verifies the traces of the centering and projection matrices. It then accumulates **X′X** in blocks of rows and computes White standard errors.

NumPy's `einsum` evaluates the Einstein summation convention directly. The index string `"ij,ik->jk"` is the notation of Section 5, and in this case the notation runs as code.

## Repository contents

```
matrix-notation-for-economists/
├── 2026-10-26_Matrix_Notation.pdf   the primer, about 33 pages
├── .github/ISSUE_TEMPLATE/
│   └── correction.md                form for reporting errors and suggestions
├── LICENSE                          full text of CC BY 4.0
└── README.md
```

## Comments and corrections

Corrections, questions and suggestions are welcome. Please [open an issue](https://github.com/jibonayan/matrix-notation-for-economists/issues/new/choose) and give the page and section number of the PDF. A GitHub account is required.

## How to cite

Please cite the primer as

> Raychaudhuri, J. (2026). *A Primer on Matrix Notation*. Teaching notes, version of 26 October 2026. <https://github.com/jibonayan/matrix-notation-for-economists>

BibTeX:

```bibtex
@misc{raychaudhuri2026matrix,
  author       = {Raychaudhuri, Jibonayan},
  title        = {A Primer on Matrix Notation},
  year         = {2026},
  note         = {Teaching notes, version of 26 October 2026},
  howpublished = {GitHub repository},
  url          = {https://github.com/jibonayan/matrix-notation-for-economists}
}
```

## Licence

Copyright © 2026 Jibonayan Raychaudhuri.

The text, mathematics, exercises and code in this repository are licensed under the [Creative Commons Attribution 4.0 International Licence (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). The full legal text is in `LICENSE` and at <https://creativecommons.org/licenses/by/4.0/legalcode>.

You may copy and redistribute the material in any medium or format. You may adapt, remix, translate and build on it for any purpose, including commercial teaching. These freedoms come with one condition.

**Attribution is required.** Any copy or adaptation must

1. credit the author as **Jibonayan Raychaudhuri**,
2. give the title **A Primer on Matrix Notation** and link to this repository, <https://github.com/jibonayan/matrix-notation-for-economists>,
3. link to the licence, <https://creativecommons.org/licenses/by/4.0/>, and
4. state whether you made changes, and if so describe them briefly.

A suitable credit line is

> Adapted from *A Primer on Matrix Notation* by Jibonayan Raychaudhuri (2026), licensed under CC BY 4.0. 

Attribution must not suggest that the author endorses you or your use of the material. You may not add legal terms or technological measures that stop others from doing anything the licence permits.

### Images are licensed separately

The six images reproduced in the PDF are **not** covered by the CC BY 4.0 licence above. Each keeps its own terms, and each is credited beneath the image and on the Image Credits page of the PDF. All were obtained from Wikimedia Commons and resized.

| Section | Work | Licence |
|---|---|---|
| Sigma notation | Carl Friedrich Gauss, oil portrait by Christian Albrecht Jensen, 1840 | Public domain |
| Matrix notation | Arthur Cayley, photograph by Herbert Beraud, before 1883 | Public domain |
| Index notation | Albert Einstein, photograph by Ferdinand Schmutzer, 1921, restored by Adam Cuerden | Public domain |
| Summing vectors | Replica of a Hollerith tabulator, Computer History Museum, photograph by Adam Schuster, 2007 | [CC BY 2.0](https://creativecommons.org/licenses/by/2.0/) |
| Matrix calculus | Adrien-Marie Legendre, watercolour caricature by Julien-Léopold Boilly, 1820 | Public domain |
| Python section | Betty Jennings and Frances Bilas operating ENIAC, U.S. Army photograph, 1945 to 1947 | Public domain |

The Hollerith photograph requires its own attribution. Anyone reusing it must credit Adam Schuster, link to the CC BY 2.0 licence and note that the image was resized.

### Third-party material

The summation rules in Section 3 follow the structure of James H. Steiger's notes on summation algebra, with new examples. Other sources are cited in the text and listed in the reference section of the document. Citation is not a licence. Quoted or closely paraphrased third-party material remains subject to its owners' rights.

## Acknowledgements

The presentation draws on Greene (2018), Wooldridge (2020), Cameron and Trivedi (2005), Searle and Khuri (2017), Abadir and Magnus (2005), Magnus and Neudecker (2019) and Harville (1997). Historical notes rely on Hayes (2006), Higham (2008), Cayley (1858), Einstein (1916), Stigler (1981), Duren (2009), the U.S. Census Bureau and Penn Engineering. Full references are in the document.
