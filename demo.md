# Instalation 
Several option exist on how to install DVC, we provid an instalation option that is working on all platoforms such as Windows, Mac OS or Linux: 

## Anaconda

```bash
conda install -c conda-forge mamba # installs much faster than conda
mamba install -c conda-forge dvc
```


Other instalation options are available [here](https://github.com/iterative/dvc#installation).

# Versioning Large Files - Simple Demo
After DVC has been installed, it is possible to start DVC by initializing it in a Git repository: 

```bash
$ dvc init
```

Action above should create 2 new files: .dvc/.gitignore and .dvc/config.
Following command will create a file \<datasetname\>.dvc that can be versioned as it only contains metadata of the original dataset:

```bash
dvc add data.csv
```

Using a git command the \<datasetname\>.dvc is added to versioning, while the \<datasetname\> is transfered to .gitignore in order to only track the small metadata file and not the large dataset itself:

```bash
$ git add data/data.xml.dvc data/.gitignore
$ git commit -m "Add raw data"
```
To retrive the version of dataset in history, i.e. to point to specific previous command use:
```bash
git checkout HEAD^1 data/data.xml.dvc
dvc checkout
```
And your version of dataset in one commit behind HEAD will be loaded. 

