# Cross-scale machine learning on large image datasets

As of version 1.4.1, ilastik supports two multiscale image formats, Precomputed Neuroglancer and OME-Zarr. Currently, users can only choose one of the available image scales and use the dataset at that scale as an input to the existing machine learning workflows.

We want to take this to the next level and allow users to run machine learning workflows across scales. For example, users could provide pixel labels at a low scale, but choose to train the classifier and run computations at native resolution.

* Mentor: @btbest
* Language: Python
* Difficulty: Hard
* Length: Large
