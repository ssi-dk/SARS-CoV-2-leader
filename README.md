# SARS-CoV-2-leader notebook wrapper

A jupyter notebook wrapper for the SARS-CoV2-leader scripts. Please see `./notebooks/covid19_leader.ipynb` for more information.

## Requirements
- conda

## Installation
install conda env, recommendation is into project dir

`conda install -p ./.venv -c conda-forge -c bioconda --file ./notebooks/covid19_leader.requirements.txt`

Set the jupyter server to use the conda env
install conda env, recommendation is into project dir by pointing it to`./.venv`

Add associate input and output folders. The default location is `./input` and `./output`, 
- input 
    - The resulting mapped bam files for each smaple against the SARS-CoV2 reference genome.
    - (Optional) indexed bam file `.bam.bai`, this provides additional statistics with the base program, however, none of these values are used for the notebook.
- output
    - Each sample has the following files:
        - `.bam/.bai`: A bam file containing only reads with the leader sequence.
        - `.depth.txt`: A tsv file containing the depth at each position at the specified Q value.
        - `.csv` (unused): A csv file containing average coverage before and after (often empty).
        - `.sam` (unused): A sam file containing only reads with the leader sequence.
        - `.txt` (unused): The output of the original program on the single sample
    - COVID_leader_splice_sites.tsv: A tsv file containing the counts of each reads on the selected positions
    - COVID_leader_splice_sites.proportional.tsv (final data output): Contains the previous file content and calculates the proportion of each site per sample as well 
        
NOTE: for `./sars_cov2_leader.sh` to work on mac you'll also need to install md5sum (e.g. brew install md5sha1sum)
