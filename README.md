# automl

### Overview

This was an exercise with a TOOL rather than finding the best model.  The question that I sought to answer is if the model would beat a manually selected one on a toy data set.  This was not an exercise in accuracy, but rather the gap between man and machine in model selection and this single dataset.

### Up and Running

There are dockerfiles for both the GermanCreditData.ipynb and GermanCreditDataAuto.ipynb.   Build these two get the two environments setup.  When starting the containers, there are two bind mounts, one to the project directory and the other to the data direction (mounted as /artifacts).

Getting autosklearn to run in anaconda was a giant pain, so I gave up and used the base python3 docker image.  All you should need to do is run this file, but I didn't install matplotlib or much else (just what was needed to run autosklearn)

### GermanCreditDataAuto.ipynb

This was the manual file that filtered the data, and exported the data it was trained on (as ndarrays) for the automl container to do its thing on.  Run this in the jupyter container.

### GermanCreditDataAuto.ipynb

Be sure to run this in the autosklearn docker container.
