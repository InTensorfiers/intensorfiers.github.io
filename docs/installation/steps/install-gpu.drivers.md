# 2. Install GPU drivers  

![GPU drivers](https://images.unsplash.com/photo-1674741250252-edb6a227c166?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2148&q=80)

To harness the enhanced computing capabilities of a GPU, individuals should install the appropriate GPU drivers. These drivers facilitate seamless communication between the operating system and the GPU hardware, resulting in optimal performance for tasks like machine learning and graphics-intensive applications. 

In our project, our objective is to simplify the process by facilitating the script, as there are indeed multiple approaches available. However the general steps below outline the process:

## 1. Identify the GPU
Users should determine the make and model of the GPU (e.g., NVIDIA or AMD) as well as the specific version.
## 2. Download Drivers: 
They should visit the official website of the GPU manufacturer (NVIDIA or AMD) and locate the drivers section. The next step is to download the latest GPU drivers compatible with the GPU model and operating system version.
## 3. Installation:
On Linux (Ubuntu or other distributions):
For NVIDIA GPUs: Following the provided instructions, users should install the drivers. This typically involves executing commands in the terminal and rebooting the system.
For AMD GPUs: The installation of drivers should occur using package managers or scripts provided by the manufacturer.
## 4. Verification:
Post-installation, users should conduct a verification process to ascertain the correct functionality of the GPU drivers. This can be achieved by inspecting system information or employing GPU-related commands. This step serves to confirm whether the system accurately recognizes and effectively utilizes the GPU.

It's imperative to note that the installation procedure can differ based on the brand, model, and specific Linux distribution of the GPU. Users are strongly advised to refer to the official documentation offered by NVIDIA, AMD, or their chosen distribution for precise and updated installation instructions. The installation of GPU drivers stands as a pivotal component in harnessing maximum GPU capabilities, thereby elevating performance across a gamut of computational tasks.

## Details of the installation of GPU Drivers
As previously noted, our script validation will be carried out using a Virtual Machine. Consequently, upon the creation of an instance equipped with one or more GPUs, our system necessitates the installation of NVIDIA device drivers. These drivers are essential to enable seamless access to the device by our applications.

Google already provides us with [documentation](https://cloud.google.com/compute/docs/gpus/install-drivers-gpu) to install GPU drivers for the VMs created on Google Cloud. They even provide us with [scripts to automate the installation process](https://github.com/InTensorfiers/compute-gpu-installation), we forked the library in our Github reporsitory of their scripts.

Now, let's delve into an explanation of the script's pivotal components:

The script commences by emphasizing its adherence to the Apache License, underscoring its open-source nature. Subsequently, it imports the essential libraries and the "Drivers_url," a crucial element for its operation.

Following this, the script moves on to a critical phase where it defines the class tailored for Linux distributions' operating systems that the script effectively supports. This pivotal section is outlined below:

<iframe
  src="https://carbon.now.sh/embed/OjqnBYHW8ZXklTJVQiXJ"
  style="width: 520px; height: 272px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Then we proceed with document the most important functions :

The main function is defined as the central point of the installation script. 
If the parsed action is 'verify', the script checks whether the driver is installed. If the driver is not installed, a message is printed indicating its absence.

<iframe
  src="https://carbon.now.sh/embed/TmnAaRdyZccInk4X8BTL"
  style="width: 510px; height: 522px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>


<iframe
  src="https://carbon.now.sh/embed/q4HjGQPK4zedFPFe6S2R"
  style="width: 520px; height: 780px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>


Check Python version
<iframe
  src="https://carbon.now.sh/embed/M6m6A1PdFW9SxSXdsapd"
  style="width: 520px; height: 332px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Check drivers installed
<iframe
  src="https://carbon.now.sh/embed/svmmQu5g1mRiIcOPAnEb"
  style="width: 520px; height: 450px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Detect Linux distro

<iframe
  src="https://carbon.now.sh/embed/G0IiWWfh2ClSJ7T5YV6E"
  style="width: 520px; height: 766px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Install dependencies

<iframe
  src="https://carbon.now.sh/embed/D0bGYZx7UmuIRRixe320"
  style="width: 520px; height: 706px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Detect GPU devices 

<iframe
  src="https://carbon.now.sh/embed/O0zi4F8zSyvcixk309cK"
  style="width: 520px; height: 490px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Install Drivers runfile 
<iframe
  src="https://carbon.now.sh/embed/fHLgIxbYINPuuqs7tF6L"
  style="width: 520px; height: 962px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>

Post installation steps 

<iframe
  src="https://carbon.now.sh/embed/Q4caC0zFhhUwRdt5bJNJ"
  style="width: 520px; height: 286px; border:0; transform: scale(1); overflow:hidden;"
  sandbox="allow-scripts allow-same-origin">
</iframe>




