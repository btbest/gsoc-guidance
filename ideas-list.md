# GSoC 2026

ilastik participates in Google Summer of Code 2026 as a sub-organization under the Python Software Foundation umbrella. This means the [PSF's contributor guidance](https://python-gsoc.org/contributors.html) generally also applies to applications with us. At least mostly. The parts mentioning IRC definitely do not apply to ilastik.

Make sure you have read their advice!

## Try out ilastik

https://ilastik.org/download for installers - and there are example image datasets at the bottom of the page.

## First look at our code base

Like many other projects, we have a "good first issue" label on our [issue tracker](https://github.com/ilastik/ilastik/issues?q=is%3Aissue%20state%3Aopen%20label%3A%22good%20first%20issue%22), which should provide a decent entrypoint to get familiar with our code base.

Instructions for setting up the coding environment are in [contributing.md](https://github.com/ilastik/ilastik/blob/main/CONTRIBUTING.md).
Please post an issue if the instructions are unclear or something doesn't work for you. Or, even better, suggest an improvement through a Pull Request if you found a workaround despite bad instructions from us :)

Once you're running ilastik from code, you'd probably want to try what you can actually do with it. We have pretty comprehensive [user documentation](https://www.ilastik.org/documentation/) on our website (and YouTube channel linked there), and there are some example image datasets on our [downloads page](https://www.ilastik.org/download).

## Contact / Questions

Main contact and mentor for all projects will be Benedikt Best (@btbest, Central European time). Feel free to reach out by [email](mailto:team@ilastik.org?subject=[GSoC]%20Contact%20from%20ideas%20list).

## LLM Disclaimer

For GSoC 2026, we expect many proposals and communications to be heavily LLM-assisted. You may use LLMs, but do so carefully and responsibly.

Always show that you are actively using ilastik and testing any code you provide - demonstrating your work is essential.

## Project ideas

If you're already an ilastik user and have always wanted to fix something, or if you just have an idea of your own, we encourage you to suggest it! Otherwise, here are some suggestions for projects (sorted by expected duration).

### Improve Multicut colour scheme

"Boundary-based segmentation with multicut" is one of ilastik's most complex workflows.
There are probably several ways its UX could be improved, but the colours used for labelling are both inaccessible and unintuitive.
Coming up with a better colour scheme that really works is not trivial, however. A systematic approach will be necessary.

* Skills involved: Python language, PyQt, UI design
* Difficulty: Medium
* Duration: 175h

### Jupyter Notebooks showcasing the ilastik Python API

Clear, practical Jupyter notebooks can significantly lower the barrier to using ilastik’s Python API. The focus here is on realistic, end-to-end workflows rather than minimal examples.

The notebooks may cover topics such as running predictions on new data, batch processing, exporting results, and combining ilastik outputs with other tools in the scientific Python ecosystem. Together, they should serve both as tutorials for new users and as reference material.

* Skills involved: Python language, Jupyter notebooks, ilastik Python API, scientific Python ecosystem (NumPy, pandas, xarray, dask)
* Difficulty: Medium
* Duration: 175h

### Python API class for the Data Conversion Workflow

ilastik provides several user-facing workflows, such as Pixel Classification and Autocontext, which are already exposed as first-class objects in the experimental Python API. The Data Conversion workflow is currently not accessible in the same way.

Adding API support for the Data Conversion workflow would allow it to be loaded, configured, and run programmatically. This would make data preparation and format conversion workflows available from Python and enable better integration with automated pipelines and headless usage.

* Skills involved: Python language, Pydantic, ilastik Python API, ilastik workflows and internal project file structure
* Difficulty: Medium
* Duration: 175h-350h

### Export ilastik projects for publication

ilastik projects are frequently used in published research, but preparing a project for publication or archival is currently a largely manual process. Supporting a publication-oriented export would make it easier to share, archive, and reproduce ilastik-based analyses.

The core idea is an export that bundles an ilastik project together with all required datasets and metadata in a system-independent way. The result should be suitable for long-term storage or upload to services such as Zenodo, and should reduce the effort needed for others to reproduce the work.

* Skills involved: Python language, PyQt, scientific imaging file formats (HDF5, TIFF, Zarr), reproducible research concepts, ilastik workflows and internal project file structure
* Difficulty: Hard
* Duration: 350h
