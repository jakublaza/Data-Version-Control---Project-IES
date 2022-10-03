# Instalation 
Several option exist on how to install DVC, we provid an instalation option that is working on all platoforms such as Windows, Mac OS or Linux: 

## Anaconda
`conda install -c conda-forge mamba # installs much faster than conda
mamba install -c conda-forge dvc`

Other instalation options are available [here](https://github.com/iterative/dvc#installation).

# Quick Demo
After DVC has been installed, it is possible to start DVC by initializing it in a Git repository: 

`$ dvc init`

Action above should create 2 new files: .dvc/.gitignore and .dvc/config.
Following command will create a file \<datasetname\>.dvc that can be versioned as it only contains metadata of the original dataset:

`dvc add data.parquet`

Using a git command the \<datasetname\>.dvc is added to versioning, while the \<datasetname\> is transfered to .gitignore in order to only track the small metadata file and not the large dataset itself:

`$ git add data/data.xml.dvc data/.gitignore`

`$ git commit -m "Add raw data"`


