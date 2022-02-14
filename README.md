# SARS-CoV-2-leader notebook wrapper

A jupyter notebook wrapper for the SARS-CoV2-leader scripts. 

## Requirements
- conda

## Installation
install conda env, recommendation is into project dir

`conda install -p ./.venv -c conda-forge -c bioconda --file ./notebooks/covid19_leader.requirements.txt`

Set the jupyter server to use the conda env
install conda env, recommendation is into project dir by pointing it to`./.venv`

Add associate input and output folders. The default location is `./input` and `./output`

NOTE: for `./sars_cov2_leader.sh` to work on mac you'll also need to install md5sum (e.g. brew install md5sha1sum)

- Original repository files are all in scripts