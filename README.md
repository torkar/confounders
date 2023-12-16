# Replication package for study on confounders

The repository contains scripts for replication and evaluation of the methodology used in the manuscript.

The repository consists of,

[res.Rds](https://github.com/torkar/confounders/blob/main/res.Rds): A saved data file from the simulation, which one can load into R: `res <- readRDS(res.Rds)`.

[figs/](https://github.com/torkar/confounders/tree/main/figs): A Dagitty printout of the large DAG used in the experiment.

[papers/](https://github.com/torkar/confounders/tree/main/papers): The original 1998 study by Lin *et al.* describing the methodology used in the analysis.

[docs/](https://github.com/torkar/confounders/tree/main/docs): The *index.rmd* one can execute to reproduce the results, and the output *index.html*, which one can read as-is.

The index.html file canbe viewed [online](https://torkar.github.io/confounders/).

Word of warning, we use `Stan`, `brms`, etc. so there's a lot to install. In case of questions please contact [Richard Torkar](mailto:torkarr@chalmers.se?subject=[GitHub]%20Feature%20Selection).
