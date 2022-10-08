# Versioning Large Files
DVC can take a snapshot of a data file and commit it to git without storing the file. Under the hood, DVC creates a file that contains only a meta-data of the file, the file itself can be stored on your computer or on cloud. The meta-file connects the file stored outside git with your git files and thanks to that link you can use DVC to create and restore previous version of your dataset. 

In case of a collaboration with others it might be useful to store the files on the cloud - s3, gs, azure, oss, ssh are all available. 

Following picture shows how each commit contains information about changes to data as well as featurs and model in case of, for example, ML project:
![picture](https://dvc.org/static/39d86590fa8ead1cd1247c883a8cf2c0/cb690/project-versions.png)

# Quick Demo
How to install DVC can be found [here](https://github.com/iterative/dvc#installation).

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


