# 2. Install GPU drivers  

![GPU drivers](https://images.unsplash.com/photo-1674741250252-edb6a227c166?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2148&q=80)

To harness the enhanced computing capabilities of a GPU, individuals should install the appropriate GPU drivers. These drivers facilitate seamless communication between the operating system and the GPU hardware, resulting in optimal performance for tasks like machine learning and graphics-intensive applications. 

In our project, our objective is to simplify the process by facilitating the script, as there are indeed multiple approaches available. However the general steps below outline the process:

## 1. Identify the GPU
Users should determine the make and model of the GPU (e.g., NVIDIA or AMD) as well as the specific version.
## 2. Download Drivers
They should visit the official website of the GPU manufacturer (NVIDIA or AMD) and locate the drivers section. The next step is to download the latest GPU drivers compatible with the GPU model and operating system version.
## 3. Installation
On Linux (Ubuntu or other distributions):
For NVIDIA GPUs: Following the provided instructions, users should install the drivers. This typically involves executing commands in the terminal and rebooting the system.
For AMD GPUs: The installation of drivers should occur using package managers or scripts provided by the manufacturer.
## 4. Verification
Post-installation, users should conduct a verification process to ascertain the correct functionality of the GPU drivers. This can be achieved by inspecting system information or employing GPU-related commands. This step serves to confirm whether the system accurately recognizes and effectively utilizes the GPU.

It's imperative to note that the installation procedure can differ based on the brand, model, and specific Linux distribution of the GPU. Users are strongly advised to refer to the official documentation offered by NVIDIA, AMD, or their chosen distribution for precise and updated installation instructions. The installation of GPU drivers stands as a pivotal component in harnessing maximum GPU capabilities, thereby elevating performance across a gamut of computational tasks.

## Details of the installation of GPU Drivers
As previously noted, our script validation will be carried out using a Virtual Machine. Consequently, upon the creation of an instance equipped with one or more GPUs, our system necessitates the installation of NVIDIA device drivers. These drivers are essential to enable seamless access to the device by our applications.

Google already provides us with [documentation](https://cloud.google.com/compute/docs/gpus/install-drivers-gpu) to install GPU drivers for the VMs created on Google Cloud. They even provide us with [scripts to automate the installation process](https://github.com/InTensorfiers/compute-gpu-installation), we forked the library in our Github reporsitory of their scripts.

To make the job easier, here is the summary of NVIDIA driver installation process.

1. Ensure Python3 is installed on your operating system

```bash
python3 --version
```

2. Download the installation script

```bash
curl https://raw.githubusercontent.com/InTensorfiers/compute-gpu-installation/main/linux/install_gpu_driver.py --output install_gpu_driver.py
```

3. Run the installation script

```bash
sudo python3 install_gpu_driver.py
```
> Note: The script takes some time to run. It might restart your VM. If the VM restarts, run the script again to continue the installation.

4. Verify the installation

```bash
sudo nvidia-smi
```

The output should be similar to the following:

```bash
        Tue Mar 21 19:50:15 2023
    +-----------------------------------------------------------------------------+
    | NVIDIA-SMI 530.30.02    Driver Version: 530.30.02    CUDA Version: 12.1     |
    |-------------------------------+----------------------+----------------------+
    | GPU  Name        Persistence-M| Bus-Id        Disp.A | Volatile Uncorr. ECC |
    | Fan  Temp  Perf  Pwr:Usage/Cap|         Memory-Usage | GPU-Util  Compute M. |
    |                               |                      |               MIG M. |
    |===============================+======================+======================|
    |   0  NVIDIA L4           Off  | 00000000:00:03.0 Off |                    0 |
    | N/A   63C    P0    30W /  75W |      0MiB / 23034MiB |      8%      Default |
    |                               |                      |                  N/A |
    +-------------------------------+----------------------+----------------------+

    +-----------------------------------------------------------------------------+
    | Processes:                                                                  |
    |  GPU   GI   CI        PID   Type   Process name                  GPU Memory |
    |        ID   ID                                                   Usage      |
    |=============================================================================|
    |  No running processes found                                                 |
    +-----------------------------------------------------------------------------+
```

Now, let's delve into an explanation of the script's pivotal components:

The script commences by emphasizing its adherence to the Apache License, underscoring its open-source nature. 

Following this, the script moves to a phase where it defines the class tailored for Linux distributions' operating systems that the script effectively supports. This section is outlined below:

<iframe
  src="https://carbon.now.sh/embed/OjqnBYHW8ZXklTJVQiXJ"
  style="width: 520px; height: 272px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Then we proceed with script's the most important functions :

The `main` function is defined as the entry point of the installation script. It takes three actions as arguments: `verify`, `install`, or `force`. The default value is `install`. If the parsed action is `verify`, the script checks whether the driver is installed or not. If the driver is not installed, a message is printed indicating its absence. Otherwise, if the parsed action is `install` it proceeds with the installation process. Finally, if the argument is `--force` then it forces driver installation, even if there is no GPU detected.

<iframe
  src="https://carbon.now.sh/embed/TmnAaRdyZccInk4X8BTL"
  style="width: 510px; height: 534px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

The `install` function is the place where all the necessary steps to successfully install NVIDIA drivers are laid out. At a high level, these are the steps it follows for the installation process:

1. Checks the systems python version
2. Checks for root privileges. If no root privileges are given, stops the process.
3. Checks whether NVIDIA drivers have already been installed or not. If so, stops the process.
4. Detects the system's Linux distro.
5. Installs library dependencies.
6. Detects whether the systems possesses a valid GPU or not. If it does not detect a valid GPU and the installation scripts has not been forced, then it stops the process.
7. Installs the NVIDIA drivers.
8. Executes post installation steps.

<iframe
  src="https://carbon.now.sh/embed/q4HjGQPK4zedFPFe6S2R"
  style="width: 520px; height: 936px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

The `check_python_version` function makes sure that the script is run with `Python 3.6` or newer. Otherwise, it throws are runtime error.
<iframe
  src="https://carbon.now.sh/embed/M6m6A1PdFW9SxSXdsapd"
  style="width: 518px; height: 416px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

The `check_driver_installed` function checks if the driver is already installed by calling the `nvidia-smi` binary. If it's available, that means the driver is already installed.
<iframe
  src="https://carbon.now.sh/embed/svmmQu5g1mRiIcOPAnEb"
  style="width: 520px; height: 504px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

The `detect_linux_distro` functions checks the `/etc/os-release` file to figure out what distribution of OS we're running.
<iframe
  src="https://carbon.now.sh/embed/G0IiWWfh2ClSJ7T5YV6E"
  style="width: 520px; height: 868px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

The `install_dependencies` function installs the driver dependencies to the system. The function may restart the system after installing some of the packages, in such situations the script should just be started again. 
<iframe
  src="https://carbon.now.sh/embed/D0bGYZx7UmuIRRixe320"
  style="width: 520px; height: 952px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

The `detect_gpu_device` function checks if there is an NVIDIA GPU device attached and return its device code.
<iframe
  src="https://carbon.now.sh/embed/O0zi4F8zSyvcixk309cK"
  style="width: 520px; height: 574px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

The `install_driver_runfile` function installs the correct driver for the detected GPU. The function has a limit of three attempts to install the correct GPU drivers.
<iframe
  src="https://carbon.now.sh/embed/fHLgIxbYINPuuqs7tF6L"
  style="width: 516px; height: 1244px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

The `post_install_steps` function writes the success message to log.
<iframe
  src="https://carbon.now.sh/embed/Q4caC0zFhhUwRdt5bJNJ"
  style="width: 516px; height: 316px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>




