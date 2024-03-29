# Monkey Portfolios Revisisted
"A blindfolded monkey throwing darts at a newspaper's financial pages could select a portfolio that would do just as well as one carefully selected by experts."

## Introduction

In Burton Malkiel's seminal publication, *A Random Walk Down Wall Street* (1973), the concept of "monkey portfolios" was proposed. It suggests that a portfolio randomly selected by a blindfolded monkey could perform as well as one curated by experts, echoing the efficient market hypothesis. This repository contains a Jupyter notebook that empirically investigates this theory through the construction and analysis of "monkey" portfolios.

## Repository Structure

- `Monkey_portfolios_revisisted.ipynb`: The primary Jupyter notebook containing all the code and analysis for creating and evaluating the monkey portfolios.

## Getting Started

To run the analyses contained in this repository, follow these steps:

1. Open the `Monkey_portfolios_revisisted.ipynb` notebook in Jupyter Lab or Google Colab.

2. Run the notebook cells in order to execute the portfolio simulations and analyses.

## Portfolio Simulation

The notebook simulates the performance of randomly selected portfolios against a benchmark with variables such as the number of stocks (`n`) and the rebalance frequency (`f`). The simulation aims to estimate the performance and standard deviation of these synthetic indices relative to the benchmark.

<img src="images/img1.png" alt="" width="950">

## Convex Optimization

The repository showcases the use of convex optimization in the construction of portfolios with various objectives, such as minimizing the Euclidean norm of the weights or maximizing the entropy.

## Analysis

The notebook includes a detailed analysis of the generated portfolios, evaluating their performance and risk metrics such as the Expected Shortfall (CVaR) at a 95% confidence level.

# Portfolio Analysis Scenarios

In this repository, we explore three distinct portfolio construction scenarios to examine the role of randomness versus strategic asset selection in portfolio performance.

## Scenario 1: Monkey Portfolio

The *Monkey Portfolio* simulates randomly weighted portfolios to test the hypothesis that a random selection of assets could outperform a traditional capitalization-weighted index. This approach is rooted in the belief that subsequent price changes in securities are unpredictable and depart from historical prices randomly. Should these randomly constructed portfolios consistently yield superior returns before transaction expenses, it would suggest that luck may play a larger role in investment success than is commonly believed.

## Scenario 2: The 1/n Family

The `$1/n$` portfolio concept is grounded in an equal weighting strategy, rebalanced monthly (though other frequencies such as daily are also possible). Each portfolio represents the solution to a convex optimization problem, with methods designed to:

- Minimize the Euclidean norm of the weights.
- Minimize the `$\infty$` norm of the weights.
- Maximize the entropy of the weights.
- Minimize the tracking error relative to an equal weight (`$1/n$`) portfolio.

Furthermore, this scenario introduces an example with *sparse updates*, where the portfolio is only adjusted when the deviation from the target `$1/n$` portfolio exceeds a predefined threshold, as opposed to frequent rebalancing.

This technique of framing portfolio construction as a convex optimization problem is particularly beneficial when integrating additional constraints. It establishes a link between the equal weight portfolio and Tikhonov regularization and serves as a paradigmatic example within a spectrum of more complex portfolios.

## Scenario 3: Sparse Updates

In practical applications, frequent rebalancing of the portfolio may not be desirable or necessary. The *Sparse Updates* approach tolerates minor deviations from the exact `$1/n$` portfolio, aiming for a balance between performance and transaction costs. The portfolio is rebalanced to equal weights across all assets only if the change in weights since the last adjustment exceeds 20%. For changes less than this threshold, the current portfolio state is preserved.


## Plots

Visual representations of the portfolio distributions are generated, comparing the monkey portfolio, equal weight (1/n) portfolio, and sparse updates portfolio.

## Contributions

Contributions are welcome! If you have suggestions or improvements, please open an issue or pull request.

## License

This project is licensed under the Apache License, Version 2.0.

## Contact

For questions or feedback, please contact <your-email>.

## Acknowledgements

- Burton Malkiel for the concept of monkey portfolios.
- Stanford University's Convex Optimization Group for convex optimization tools.
