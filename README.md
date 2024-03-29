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

## Convex Optimization

The repository showcases the use of convex optimization in the construction of portfolios with various objectives, such as minimizing the Euclidean norm of the weights or maximizing the entropy.

## Analysis

The notebook includes a detailed analysis of the generated portfolios, evaluating their performance and risk metrics such as the Expected Shortfall (CVaR) at a 95% confidence level.

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
