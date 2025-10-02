# Mixed Models — Practical Exercises

A set of scripts and practical exercises illustrating the use of **mixed models** in `R`.

This repository contains a series of hands-on practicals to explore mixed models using `nlme` and `lme4`. 
These exercises are designed for students and researchers interested in statistical modelling with `R`.

## Conda Environment Setup

To run the practicals, set up your conda environment as follows:

```
# Install mamba for faster dependency resolution
conda install -c conda-forge mamba

# Create and activate environment
conda create -n mixedmodels_env
conda activate mixedmodels_env

# Install required R packages
mamba install -c anaconda -c bioconda -c conda-forge -c r \
    r-base r-rmarkdown r-nlme r-lme4
```

**Exercise**: Try setting up your own conda environment on your laptop if not already done.






## Practicals

The repository contains four practicals implemented in R Markdown. You can render them with:

```
rmarkdown::render("01_tp_Orange.Rmd")
rmarkdown::render("02_tp_sleepstudy.Rmd")
rmarkdown::render("03_tp_BodyWeight.Rmd")
rmarkdown::render("04_tp_simulator.Rmd")
````

Practical Contents:

01_tp_Orange.Rmd — Introduction to mixed models with Orange dataset

02_tp_sleepstudy.Rmd — Sleep study dataset analysis

03_tp_BodyWeight.Rmd — Body weight dataset and random effects

04_tp_simulator.Rmd — Simulating mixed model data




## References

Pinheiro, J. C., & Bates, D. M. (2000). Mixed-Effects Models in S and S-PLUS. Springer.

Bates, D., Mächler, M., Bolker, B., & Walker, S. (2015). Fitting Linear Mixed-Effects Models Using lme4. Journal of Statistical Software.


