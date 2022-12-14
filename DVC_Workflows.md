# DVC Workflows

<p align="center">
<img src="https://user-images.githubusercontent.com/114607096/194352724-52e798ad-5b6c-4674-a8cb-da631b656e21.png" height = "280" width="400"/>
</p>
https://miro.medium.com/max/786/1*xcKTNUphlxoKWlbGMoZZPA.png

Git works well as a platform for the version control of codes. However, it faces some limitations when used for controlling the version of data and models. The reason is that internet hosting services like GitHub have a strictly limited capacity for uploaded files but the ML experiments typically need large-scale datasets, which might often change in the process of searching for a final model. [^1] [^2] 

Systems for data version control have been created to overcome these problems. A benefit of working with DVC is that the syntax is very similar to the one of Git.[^1] Nevertheless, there are some differences between usual Git and DVC workflows. The DVC workflow is typical for various data science tasks and projects. The figures below depict examples of both workflows graphically:[^3]    

<p align="center">
<img src="https://user-images.githubusercontent.com/114607096/195655400-c6c71513-cba1-47fa-bf69-fdc294d2d8a5.png" height = "270" width="400"/>
</p>

The DVC (Data Science) workflow allows different people to experiment with different ideas without a long time spent waiting.[^3] An example of good practice is that a separate branch is made for every experiment, followed by a merge in case of success. DVC enables users easily check previous experiments without the need to rerun them every time.[^4] Another useful tip is to keep failed experiments and remove those that are not important anymore.[^3]   

## Sources

[^1]: https://towardsdatascience.com/introduction-to-dvc-data-version-control-tool-for-machine-learning-projects-7cb49c229fe0
[^2]: https://towardsdatascience.com/version-control-ml-model-4adb2db5f87c
[^3]: https://www.slideshare.net/DmitryPetrov15/pydata-berlin-2018-dvcorg
[^4]: https://dvc.org/doc/user-guide/overview
 
