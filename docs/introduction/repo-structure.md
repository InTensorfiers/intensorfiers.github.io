# Repository Structure

All codes and script used in this project are stored in our GitHub organization - [InTensorfiers](https://github.com/orgs/InTensorfiers/repositories).

<div class="github-card" data-github="intensorfiers" data-width="400" data-height="151" data-theme="default"></div>
<script src="//cdn.jsdelivr.net/github-cards/latest/widget.js"></script>

## Repostitories and their functionalities

### intensorfiers.github.io

<div class="github-card" data-github="intensorfiers/intensorfiers.github.io" data-width="400" data-height="" data-theme="default"></div>
<script src="//cdn.jsdelivr.net/github-cards/latest/widget.js"></script>

The website that you are currently reading.
This contains all the documentations written in this project.
In here you can find the installation steps, the architecture design choices, and benchmarks.

All documentations are written in Markdown format and were rendered into web pages with the help of [MkDocs](https://www.mkdocs.org/) and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

This project is hosted on GitHub Pages.

### GPU-config-with-Ansible

<div class="github-card" data-github="intensorfiers/gpu-config-with-ansible" data-width="400" data-height="" data-theme="default"></div>
<script src="//cdn.jsdelivr.net/github-cards/latest/widget.js"></script>

The repository that stores Ansible playbooks and all other related files.

In this repo you can find the playbook as well as the installation instructions to automatically install all compoenents i.e. Nvidia driver, conda, CUDA, cuDNN through Ansible.

Please note that in order to use it, you will need to specify the IP address of the remote machine that you want to connect, and to ensure that it accepts SSH connection from your machine.

### compute-gpu-installation

<div class="github-card" data-github="InTensorfiers/compute-gpu-installation" data-width="400" data-height="" data-theme="default"></div>
<script src="//cdn.jsdelivr.net/github-cards/latest/widget.js"></script>

This repository stores the Python scripts that detect Nvidia devices and Linux machine and install appropriate driver.

This is a fork from [GoogleCloudPlatform/compute-gpu-installation](https://github.com/GoogleCloudPlatform/compute-gpu-installation).

We create a fork to ensure the script that we will be using to instsall the driver would not be changed without prior testing.