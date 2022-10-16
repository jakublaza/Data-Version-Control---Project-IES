# Why is DVC useful for ML Projects?
As was hinted in previous sections, DVC can be especially helpful for a large Machine Learning projects for which a collaboration of several people is needed. The next paragprah describes few benefits of using DVC in ML projects.

In a devlelopment of a large ML project the model and dataset usually changes. Without DVC it can be diffucult to know which specific version of dataset belogs to specific code or which code was used to produce specific model. DVC can version models as well as largefiles similarly to git, hence no more files names like *data_Final.csv*, *data_FINALFINAL2.csv* etc. and confusion about which dataset belongs to which code. Further, the versioning of pipelines makes it easy to reproduce code (more info [here](pipelines.md)).

## Sources
https://dvc.org

https://dvc.org/doc/use-cases