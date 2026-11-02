# Expected signatures on a mesh: numerical companion

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/FlorianHuber-Math/expected-signature-minimax/blob/main/expected_signature_numerics.ipynb)

This repository accompanies the paper

> F. Huber, *Weak and strong discretization errors for signatures of Gaussian processes*.

The notebook `expected_signature_numerics.ipynb` has four parts.

| Part | Content |
|---|---|
| 0 | A short introduction to signatures: iterated integrals, Chen's identity, the shuffle identity, the expected signature of Brownian motion, and what discretization on a mesh does (weak and strong error). |
| A | Section 5 of the paper (Young range): Theorem 5.3(i), Proposition 5.14, Remarks 5.6 and 5.13, Proposition 5.18. |
| B | Section 6 (rough range): Remarks 6.7, 6.19 and 6.27, and the sign change after Corollary 6.20. |
| C | Sections 7–8 (strong error and the lower bound): Remarks 7.3 and 8.10, Proposition 7.4 (Monte Carlo illustration), and other explicit constants. |

Every numerical value quoted in the paper is reproduced. Each check prints the paper's value next to the computed one and ends in `OK` or `MISMATCH`. No proof in the paper uses a numerical value as an input.

## Running

* **Colab:** click the badge above and choose "Runtime → Run all".
* **Locally:** `pip install -r requirements.txt`, then open the notebook in Jupyter.

The first code cell sets the mode.

* `QUICK = True` (default) runs in about one minute, on smaller meshes where needed.
* `QUICK = False` uses the exact parameters of the paper and takes about six minutes on a laptop.

Except for the cells labelled *Monte Carlo*, all values are exact finite sums or closed forms (Chen's identity, Wick/Isserlis sums over mesh cells, quadrature with stated tolerance, or `mpmath`).

## Requirements

Python 3.9 or later, with `numpy`, `scipy`, `matplotlib` and `mpmath`, all preinstalled on Colab.
