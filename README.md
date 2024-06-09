# Chess Player Rankings

This project explores the application of Bayesian methods to estimate rankings for chess players using Markov Chain Monte Carlo (MCMC) sampling techniques. The inspiration for this project comes from [Martin Ingram's blog post](https://martiningram.github.io/mcmc-comparison/) comparing different MCMC algorithms.

## Dataset
The dataset used for this project is sourced from [Kaggle](https://www.kaggle.com/datasets/datasnaek/chess), containing information about chess games including player IDs and ratings.

## Methodology
1. The dataset is preprocessed to extract player IDs and ratings, creating a list of unique players and their maximum ratings.
2. Bayesian inference is applied to estimate the rankings of the players using PyMC.
3. The model is sampled using MCMC methods, specifically the NUTS sampler with the NumPyro backend.
4. The results are summarized using ArviZ and presented as posterior distributions of player skills.
5. The "skill" metric is sorted to identify the top and bottom players based on their maximum ratings.

## Results
| Predicted Ranking | Actual Ranking |       Player Name       | Skill Mean | Skill SD |
|-------------------|----------------|-------------------------|------------|----------|
|        1          |       34       |         chesscarl       |    3.474   |  0.685   |
|        2          |       71       |          siindbad       |    3.272   |  0.814   |
|        3          |      185       |           mmichael      |    3.104   |  0.823   |
|        4          |       15       |        amir2002zzz      |    2.961   |  0.835   |
|        5          |      4867      |        steelviper       |    2.861   |  0.839   |
|        ...        |      ...       |            ...          |     ...    |   ...    |
|       15631       |      7434      |         sveenemand      |   -2.771   |  0.666   |
|       15632       |      8501      |          ghaffari       |   -2.786   |  0.716   |
|       15633       |      5816      | josephelbouhessaini     |   -2.878   |  0.875   |
|       15634       |      5742      |         mccheese        |   -2.893   |  0.717   |
|       15635       |      7948      |         stellanova      |   -3.150   |  0.814   |


For detailed analysis and code implementation, refer to the Jupyter Notebook in this repository.
