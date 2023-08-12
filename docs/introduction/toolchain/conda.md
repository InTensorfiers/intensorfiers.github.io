# Conda

![conda logo](../../images/conda_logo.svg)

## What is Conda?
Conda is an open-source package and environment management system.It allows you to create isolated environments containing specific packages and dependencies, making it easier to manage software for different projects.

## Why choose Conda over Base OS installation?
Installing the CUDA toolkit and all dependencies on the base OS provides the easier way to achieve the deployment, but it does not provide flexibility in mangaing multiple environments. Most likely, we will need to manage multiple environments for suiting different projects' needs. Therefore this is not desirable to install on base OS only.

## Why choose Conda over Virtualenv?

Virtualenv only creates a new Python and pip binary in a local folder. This works well for isolating Python environments. But since the CUDA toolkit is a non-Python (C++) package, Virtualenv does not help isolating and managing multiple version of the toolkit. Therefore, conda is chosen for managing individual environments for this purpose.

## How Conda Works?
Conda employs a combination of binary packages and environment specifications stored in YAML files. It resolves dependencies, manages environments, and handles package installations, ensuring compatibility.

## Choosing Miniconda over Anaconda
Miniconda is preferred for its lightweight nature, installing only Conda and a minimal set of packages.

On top of that, Anaconda provides a GUI that is aimed for desktop usage. Since this machine will be a server and thus no display will be connected to it, a GUI would be unnescessary for our workload.

This grants more control over environment customization, reducing bloat compared to Anaconda's comprehensive package collection.