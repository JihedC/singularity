Bootstrap: docker
From: continuumio/miniconda3:4.4.10
%labels
AUTHOR jihed.chouaref@gmail.com

%environment
# ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# This sets global environment variables for anything run within the container export
PATH="/opt/conda/bin:/usr/local/bin:/usr/bin:/bin:"
unset CONDA_DEFAULT_ENV
export ANACONDA_HOME=/opt/conda

%post
# ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# This is going to be executed after the base container has been downloaded export
PATH=/opt/conda/bin:$PATH
conda config --add channels defaults
conda config --add channels conda-forge
conda config --add channels bioconda
conda install --yes bwa=0.7.15
conda install --yes sickle-trim=1.33
conda install --yes subread=1.6.1
conda install --yes samtools=1.8
conda install --yes sicer2=1.0.2
conda clean --index-cache --tarballs --packages --yes
