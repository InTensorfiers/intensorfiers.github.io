# intensorfiers.github.io

![GitHub Actions badge](https://github.com/intensorfiers/intensorfiers.github.io/actions/workflows/gh-page-deploy.yml/badge.svg)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains documentation for setting up environments for Deep Learning servers using Ansible and conda. The documentation is generated using MkDocs and hosted on GitHub Pages.

## Contents

- [Overview](#overview)
- [Getting Started](#getting-started)
- [Documentation](#documentation)
- [GitHub Actions](#github-actions)
- [Contributing](#contributing)
- [License](#license)

## Overview

This repository provides comprehensive documentation for setting up environments for Deep Learning servers using Ansible and conda. The documentation covers various aspects, including installation, configuration, and management of the necessary software components and dependencies for running Deep Learning workloads.

The documentation is written using Markdown and generated using MkDocs, a static site generator. The generated documentation is hosted on GitHub Pages for easy accessibility and reference.

## Getting Started

To get started with setting up Deep Learning server environments using Ansible and conda, follow these steps:

1. Clone the repository:

   ```shell
   git clone https://github.com/intensorfiers/intensorfiers.github.io.git
   ```

2. Install the necessary dependencies:

   ```shell
   pip install -r requirements.txt
   ```

3. Navigate to the project directory:

   ```shell
   cd intensorfiers.github.io.git
   ```

4. Build the documentation:

   ```shell
   mkdocs build
   ```

5. Start a local development server to preview the documentation:

   ```shell
   mkdocs serve
   ```

   The documentation will be available at [http://localhost:8000](http://localhost:8000).

6. Customize the documentation according to your requirements, adding or modifying the content as needed.

7. Push your changes to the repository to a non-`main` branch:

   ```shell
   git push origin <your-branch-name>
   ```

8. Create a Pull Request to request the changes to be merged to `main` branch to publish

   The changes will be automatically built and deployed to GitHub Pages.

## Documentation

The documentation is organized into several sections, covering different aspects of setting up environments for Deep Learning servers using Ansible and conda. The sections include:

- Installation: Instructions for installing Ansible and conda.
- Configuration: Details on configuring Ansible playbooks and variables.
- Environment Setup: Step-by-step guide for setting up the Deep Learning environment.
- Troubleshooting: Common issues and their solutions.
- Examples: Example notebooks and configurations.

Feel free to explore the documentation and refer to the relevant sections for your specific requirements.

## GitHub Actions

This repository is integrated with GitHub Actions to automate the build process and ensure continuous testing.

- For the `main` branch, a GitHub Actions pipeline is triggered on every push. It automatically builds the documentation and deploys it to GitHub Pages.
- For all non-`main` branches, another pipeline is triggered on every push. It performs automated testing to ensure the documentation generation process is successful.

These pipelines help maintain the integrity and accuracy of the documentation and provide an up-to-date resource for users.

## Contributing

Contributions to this repository are welcome. If you find any issues or have suggestions for improvements, please feel free to open an issue or submit a pull request.

To contribute to the documentation:

1. Fork the repository.
2. Create a new branch for your changes.
3. Make the necessary modifications and additions.
4. Test the documentation locally using the steps mentioned in the "Getting Started" section.
5. Commit your changes and push the branch to your forked repository.
6. Open a pull request in this repository, describing your changes and their purpose.

Your contributions will help enhance the quality and usefulness of the documentation.

## License

The content of this repository is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute the documentation.