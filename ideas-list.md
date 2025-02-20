## Contact / Questions

Main contact and mentor for all projects will be Benedikt Best (@btbest, Central European time). Feel free to reach out by [email](mailto:team@ilastik.org) or DM via image.sc [zulip chat](https://imagesc.zulipchat.com/#user/614676).

## First look at our code base

Like many other projects, we have a "good first issue" label on our [issue tracker](https://github.com/ilastik/ilastik/issues?q=is%3Aissue%20state%3Aopen%20label%3A%22good%20first%20issue%22), which should provide a decent entrypoint to get familiar with our code base.

Instructions for setting up the coding environment are in [contributing.md](https://github.com/ilastik/ilastik/blob/main/CONTRIBUTING.md). Please post an issue if the instructions are unclear or something doesn't work for you :)

## Project ideas

If you're already an ilastik user and have always wanted to fix something, or if you just have an idea of your own, we encourage you to suggest it! Otherwise, here are some suggestions for projects (sorted by expected duration).

### Testing: Outsource test data

The `ilastik-core` conda package contains dozens of megabytes of test data that aren't needed for the package to run.
We'd like to get rid of them from the package so that it's smaller and quicker to download.
The hard part is to find a way to do this that keeps the dev experience afterwards as pain-free as possible...

* Related issues: https://github.com/ilastik/ilastik/issues/2771
* Skills involved: conda packaging ecosystem, GitHub CI/CD, testing/pytest
* Difficulty: Medium
* Duration: Short (90-175h)

### Improve Multicut UX

"Boundary-based segmentation with multicut" is one of ilastik's most complex workflows.
Between the unique labelling required, the potentially inaccessible or unintuitive label colors used, and the ambiguous "Live update"/"Run" functionalities, we often see users struggling to grasp what is going on, or what they should be doing next.
There must be ways to rearrange buttons and user interactions for a more intuitive user experience.

* Skills involved: Python language, PyQt
* Difficulty: Easy
* Duration: Variable (90-350h)

### Support pixel resolution metadata

In biological images, pixel resolution is an important piece of information, because images might show objects at vastly different scales (nanometers to centimeters).
While image files typically include this information as metadata, ilastik currently entirely ignores it.

The minimum goal for this project would be to read pixel resolution metadata when the user loads a tiff file saved by [FIJI](https://fiji.sc/), and to re-include the metadata when the user exports in the tiff format, such that FIJI understands it when the tiff exported from ilastik is loaded there.
There are many benefits that ilastik could gain from knowing about real-world size of the objects being analyzed, so there is a lot that could be done beyond this minimum.

* Related issues: https://github.com/ilastik/ilastik/issues/2870, https://github.com/ilastik/ilastik/issues/967
* Skills involved: Python language, tifffile, FIJI
* Difficulty: Medium
* Duration: Variable (90-350h)

### Cross-scale machine learning on large image datasets

As of version 1.4.1, ilastik supports two multiscale image formats, Precomputed Neuroglancer and OME-Zarr.
Currently, users can only choose one of the available image scales and use the dataset at that scale as an input to the existing machine learning workflows.

We want to take this to the next level and allow users to run machine learning workflows across scales.
For example, users could provide pixel labels at a low scale, but choose to train the classifier and run computations at native resolution.

* Skills involved: Python language, scikit-image, scikit-learn
* Difficulty: Hard
* Duration: Long (350h)
