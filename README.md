# mixed_models

A set of scripts and practicles illustrating the use of mixed models

## Conda Environment

Set up your conda environment as follow:

```
# conda create -n mixedmodels_env
conda activate mixedmodels_env
# mamba install -c anaconda -c bioconda -c conda-forge -c r r-base r-rmarkdown r-nlme r-lme4
```

Exercice: Set your own conda environment on your laptop (if needed).

## Working Directory

```
# Retrieve script and material from github
git clone https://github.com/fchuffar/mixed_models.git
# Go to your workdir
cd mixed_models
```

### Practicles

```
rmarkdown::render("01_tp_Orange.Rmd")
rmarkdown::render("02_tp_sleepstudy.Rmd")
rmarkdown::render("03_tp_BodyWeight.Rmd") 
rmarkdown::render("04_tp_simulator.Rmd")
```

