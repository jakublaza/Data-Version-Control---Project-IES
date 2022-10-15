# Pipelines
DVC allows to define a pipiline process. Such process include actions such as transforming our dataset, creating new fetures for our model or merging datasets. In a machine learning project pipeline can be a complete workflow that includes loading the data, transforming it, up untill running the model and evaluating it. Further metrics, parameters, and plots can be added to the pipeline. The flow of a pipelien is stored in a *yaml* file. The yaml file not only define the pipeline, but also decribes which data and commands to use, hence allowing for simple reproduction of a pipeline and its versioning. Further, DVC remembers which stages were already run and which needs to be run, so it prevents unnecessary reruns of parts of a code, thus making it efficient. 

Following picture displays how a structure of a pipeline can look like:

'''bash
dvc dag
         +---------+
         | prepare |
         +---------+
              *
              *
              *
        +-----------+
        | featurize |
        +-----------+
              *
              *
              *
          +-------+
          | train |
          +-------+
'''

## Code Reproducibility
Data modeling helps with sharing data files and versioning of a pipline then makes possible to easily reproduce code among collaborators. 




## Source 

https://dvc.org/doc/start/data-management/data-pipelines

https://dvc.org/doc/start



# Quick Demo
