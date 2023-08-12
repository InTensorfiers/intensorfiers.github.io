# Ansible
<p style="margin: auto;">
<img style="margin: auto;" src="https://i0.wp.com/blog.knoldus.com/wp-content/uploads/2017/10/ansible_logo.png" width="100%"/>
</p>

## What is Ansible?
Ansible is an open source, command-line IT automation software application written in Python. It can configure systems, deploy software, and orchestrate advanced workflows to support application deployment, system updates, and more.

## Why Ansible?
Ansible streamlines machine setup, configuration, and management by codifying tasks. This ensures consistency, reduces human error, and accelerates deployment processes.

## How Ansible Works?
Ansible operates agentlessly, connecting to machines via SSH. It executes tasks defined in playbooks, which are YAML files containing instructions to achieve desired states on target systems.
Ansible’s main strengths are simplicity and ease of use. It also has a strong focus on security and reliability, featuring minimal moving parts. It uses OpenSSH for transport (with other transports and pull modes as alternatives), and uses a human-readable language that is designed for getting started quickly without a lot of training.


## Use Cases
Ansible finds use in provisioning, configuration management, application deployment, and more. It's especially effective for automating repetitive tasks across multiple machines.

- [Infrastructure automation](https://www.ansible.com/use-cases/infrastructure)

- [Network automation]((https://www.ansible.com/use-cases/infrastructure))

- Security automation

- Edge automation

- Hybrid cloud automation

## Ansible's Role in the Project

In our machine learning project, Ansible serves to automate the setup of machines for ML workloads. Playbooks can install necessary dependencies, configure GPU drivers, set up virtual environments, and ensure consistent environment states. This accelerates the process of preparing machines for ML tasks and reduces configuration drift.

- Provide a way to automate the tedious installation steps
- Pro
- Reduce human error 
- Provide idempotent deployment as Ansible can detect if a certain component is already installed and thus skip it 
- Provide a configuration option for users to customize the environment according to their needs:
  - Python version
  - CUDA toolkit version
  - Dependencies to be install

