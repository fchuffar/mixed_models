# mixed_models

A set of scripts and practicles illustrating the use of mixed models

## Conda environment and working directory

Set up your conda environment as follow:

```
source /home/chuffarf/conda_config.sh
# conda create -n demosnakemake_env
conda activate demosnakemake_env
# mamba install -c anaconda -c bioconda -c conda-forge -c r r-base snakemake=7.32.4 python=3.9 graphviz python-kaleido tenacity plotly 
# pip install smgantt==0.0.5
```

Exercice: Set your own conda environment on your laptop (if needed).

Set up your working directory

```
# Retrieve script and material from github
git clone https://github.com/fchuffar/demo_snakemake.git
# Go to your workdir
cd demo_snakemake
```

### Launch your first workflow

On a worker node or on your laptop:

```
snakemake -s 01st_workflow.py --cores 1 -rp clean
snakemake -s 01st_workflow.py --cores 2 -rpn
snakemake --forceall --dag -s 01st_workflow.py| dot -Tpdf > dag.pdf
smgantt
```

From frontend on many worker nodes:

```
snakemake clean -s 01st_workflow.py --cores 1 -rp
snakemake -s 01st_workflow.py --jobs 50 --cluster "oarsub --project groupecalcul -l nodes=1/core=1,walltime=00:03:00"  --latency-wait 60 -pn
```

Exercice: 

  - Reproduice the *180 seconds tutorial* section.
  - Enhance the *180 seconds tutorial* by adjusting snakemake `cores` argument and `threads` rule parameter, increasing the number of jobs, their duration... 
  - Comment.
  





## Demo (`02nd_worflow.py`)

```
# mamba install -c anaconda -c bioconda -c conda-forge -c r -c brown-data-science r-rmarkdown r-mediation 
snakemake -s 02nd_worflow.py --cores 16 -rpn
snakemake -s 02nd_worflow.py --jobs 50 --cluster "oarsub --project groupecalcul -l nodes=1/core=1,walltime=00:10:00"  --latency-wait 60 -pn
```


### 

