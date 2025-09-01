# 🧰 EDA Tools Installation — ESDCS 2025
---

## Scope of this repo
This includes **only the installation** of the required tools.  
**How to use** these tools is already explained clearly in the **Tutorial PDF shared on Microsoft Teams**, so we **won’t repeat usage steps here**.

- **Git Repo Link**: [Link to this git repository](https://github.com/shubhamlanjewar97/ESDCS_EDA_TOOLS)  
---

## Version Specs
- **Ubuntu**: 22.04.5 LTS (Jammy Jellyfish)  
- **macOS**: 15.6 (Sequoia)
- **Windows**: 11 

> ✅ These versions are tested and known to work reliably with the tools in this course.

---

## Platforms

### 🔹 Windows (3 Options)
1. **Preinstalled Ubuntu Image**
2. **WSL (Windows Subsystem for Linux)**
3. **Ubuntu 22.04.5 in VirtualBox** 

➡️ See the following steps/link given above for the installation process.

---

### 🔹 Linux (Ubuntu 22.04.5)
Just run:
```bash
sudo apt install -y iverilog gtkwave yosys opensta
```
➡️ That’s all you need on Linux.

---

### 🔹 macOS (15.6 Sequoia)
We will use Docker to create a Linux environment for **iverilog, yosys, opensta**. We will use **Surfer** natively on macOS as waveform viewer.  

➡️ See the following steps/link given above for the installation process.

---

<div align="center">

&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  

</div>


# <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5f/Windows_logo_-_2012.svg/88px-Windows_logo_-_2012.svg.png" alt="Windows Logo" width="25"/> EDA Tools Installation — Windows 11


## Installation Options on Windows

### 1️⃣ Option 1: Preinstalled Ubuntu Image (If RAM >= 8GB && Disk Space > 25 GB you can go with this option. Otherwise go to option 2)

#### Step 1: Download and Install VirtualBox
Download from: [VirtualBox Download](https://www.virtualbox.org/wiki/Downloads)

#### Step 2: Download .ova file (Open Virtualization Archive format)

Download the `.ova` file for preinstalled apps from 

Either this Google Drive Link(generally faster): [![Google Drive](https://img.shields.io/badge/Google%20Drive-34A853?logo=googledrive&logoColor=white)](https://drive.google.com/file/d/1_P-tEtRUpTZADc26KuqlRG38UXV6wA_J/view?usp=sharing)

OR  from One Drive Link: [![OneDrive](https://img.shields.io/badge/OneDrive-blue?logo=microsoft-onedrive&logoColor=white)](https://indianinstituteofscience-my.sharepoint.com/:u:/g/personal/shubhaml_iisc_ac_in/Eb3L3PkAOZBMtYQH9pJAQqsBrpyRsw5gBYMe7jH5dtrj4g?e=DRUdzv)  

For OpenRoad, download the .ova file from Annexure B. (This is optional. You won't need this for course assignments and project. We shall tell more about it in the Lab session)

#### Step 3: Import Appliance in VirtualBox
1. Open **VirtualBox**  
2. Go to **File → Import Appliance**  
3. In **Source**, select the downloaded `.ova` file  
4. In **Settings**, select the path where you want to keep the Ubuntu files  
   - If OS drive has less space than **25 GB**, prefer another drive  
   - Preferably choose a **faster drive** for better performance  
   - You can also adjust **RAM, CPU cores, and other resources** here if needed  
5. Click **Finish** → Import will take some time

#### Step 4: Start and Use Ubuntu VM
- Start the imported VM from VirtualBox  
- Credentials:  
  - **Username**: `esdcs`  
  - **Password**: `esdcs#123`
    
It has preinstalled tools (iverilog, gtkwave, opensta, yosys). It also has folders `NANGATE_OPEN_STDCELL` and `tutorials` at location /home/esdcs/. 




#### Step 5: Other few setups

To setup **shared folders** and to do **other few setups**, you can go through `Step 7` onwards of `Option 3 : Installing Ubuntu 22.04.5 in VirtualBox`.
Same steps are followed in the following video from timestamp 7:58 onwards.

📺 **Video Walkthrough(from 7:58 onwards):** [Ubuntu on VM few setups (7:58 onwards)](https://youtu.be/E_-FE6aHIUA?t=477))  
[![Watch on YouTube](https://img.shields.io/badge/Watch%20Now-red?logo=youtube&logoColor=white)](https://youtu.be/E_-FE6aHIUA?t=477)
    
---

### 2️⃣ Option 2: WSL (Windows Subsystem for Linux)


📺 **Video Walkthrough:** [EDA Tools Installation on WSL](https://youtu.be/qvrV6PENzNk)  
[![Watch on YouTube](https://img.shields.io/badge/Watch%20Now-red?logo=youtube&logoColor=white)](https://youtu.be/qvrV6PENzNk)


#### Step 1: Enable WSL and Install Ubuntu 22.04.5
Open CMD or PowerShell as Administrator and run:
```powershell
wsl --install -d Ubuntu-22.04
```

Restart if prompted.

#### Step 2: Open Ubuntu (WSL shell)
From the **Start Menu**, search and open **Ubuntu 22.04 LTS**, or run the following command in CMD:

```powershell
wsl
```

#### Step 3: Install EDA Tools
Inside Ubuntu shell:
```bash
sudo apt update
sudo apt install -y iverilog yosys opensta gtkwave 
```

#### Step 4: Verify installation
```bash
iverilog -V
yosys -V
sta -help
gtkwave -h
lsb_release -a
```

(Mandatory : Please refer Annexure A for required folders)  

#### Notes

- To see the list of installed WSL distributions:
 ```powershell
wsl --list --verbose
```
- To remove a WSL distribution:  
 ```powershell
wsl --unregister Ubuntu
```
- Access Windows files inside WSL at `/mnt/c/...`. 


---

### 3️⃣ Option 3: Installing Ubuntu 22.04.5 in VirtualBox

To keep this repository concise, the detailed steps for this option are provided separately. You can refer the link below for a step-by-step guide:

**Git Repo Link**: [Installing Ubuntu 22.04.5 in VirtualBox](https://github.com/shubhamlanjewar97/ESDCS_EDA_Ubuntu_on_VBox)  

---

<div align="center">

&nbsp;  
&nbsp;  
&nbsp;  
&nbsp;  

</div>


# <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Apple_logo_grey.svg" alt="Apple Logo" width="25"/> EDA Tools Installation — macOS 15.6 Sequoia

Here, we will install: **iverilog** (Verilog simulator), **yosys** (Logic synthesis tool), **opensta** (Static timing analysis), **Surfer** (Waveform viewer - used instead of GTKWave)  

---
## Installation Steps
📺 **Video Walkthrough:** [EDA Tools Installation on macOS](https://youtu.be/3GBMIc1RFXI)  
[![Watch on YouTube](https://img.shields.io/badge/Watch%20Now-red?logo=youtube&logoColor=white)](https://youtu.be/3GBMIc1RFXI)

### Step 1: Install Homebrew
[Homebrew](https://brew.sh) is the package manager for macOS.  
Install it by running this in your terminal: (You can skip this step if Homebrew is already installed)

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

---

### Step 2: Install Surfer (Waveform Viewer)
Instead of GTKWave, we will use **Surfer**. To install it, enter the following brew command:

```bash
brew install surfer
```
---

### Step 3: Install Docker Desktop
We will use the other 3 tools (iverilog, yosys, opensta) in a Linux environment using Docker.

Download and install Docker Desktop for Mac (For **Intel Macs** → use Intel version, for **Apple Silicon Macs** → use Apple version ):  
👉 [Docker Desktop Download Link](https://docs.docker.com/desktop/setup/install/mac-install/)

After installation:  
1. Launch **Docker Desktop** from Applications.  
2. Log in with your **Docker Hub** account [Simply login with google works].  

---

### Step 4: Prepare Workspace Directory
Workspace directory will be shared directory between macOS and docker Ubuntu 22.04.5. Which means contents at this path present in macOS will be accessible in Ubuntu and vice versa. 
Create such directory to store Docker-related files (Please change the path according to your needs):

> ⚠️ Please replace `/Users/shubhamlanjewar/code/esdcs_docker` with **`your_path`**

```bash
mkdir -p /Users/shubhamlanjewar/code/esdcs_docker
```

---

### Step 5: Download and load Docker Image

Download the Docker image tar file.

For Apple Silicon: `esdcs-ubuntu-img.tar` [esdcs-ubuntu-img.tar](https://drive.google.com/file/d/1qZJMRKNXvw5iDqVb7cYXbC5-fPgOxV6w/view?usp=sharing)  
For Intel Processor: `esdcs-ubuntu-img-intel.tar` [esdcs-ubuntu-img-intel.tar](https://drive.google.com/file/d/10NArIqpWZQnXYdUfpdW8AeEayYwmeTc3/view?usp=sharing)  

This Docker image contains:  
- **Ubuntu** (22.04.5 LTS), **Preinstalled tools** (iverilog, yosys, opensta, lsb_release, git, curl, vim, sudo, bash)
- **tutorials & NANGATE_OPEN_STDCEL**: Its present at same location as mentioned in Tutorial PDF ( /home/esdcs/)

To load the Docker image (for Apple silicon), go to the location where `.tar` file is present and run:
```bash
docker load -i esdcs-ubuntu-img.tar
```
alternatively, you can use the following command(only for Apple silicon), in this case, you won't need the .tar file (we are pulling the image from DockerHub account):
```bash
docker pull shubhamlanjewar97/esdcs-ubuntu-img:latest
```


For Intel processor, run:
```bash
docker load -i esdcs-ubuntu-img-intel.tar
```


---

### Step 6: Create and Run the Docker Container (First Time Only)
Run the container for the very first time:

> ⚠️ Please replace `/Users/shubhamlanjewar/code/esdcs_docker` with **`your_path`**

For Apple Silicon:
```bash
docker run -it --name esdcs-ubuntu   -v /Users/shubhamlanjewar/code/esdcs_docker:/macos_local   esdcs-ubuntu-img
```

For Intel processor:
```bash
docker run -it --name esdcs-ubuntu-intel   -v /Users/shubhamlanjewar/code/esdcs_docker:/macos_local   esdcs-ubuntu-img-intel
```

This will take you to the Linux environment with user "esdcs". This Linux environment is running inside Docker.

(Mandatory: Please refer to Annexure C for more Docker commands)  

✅ You will now be inside a Linux environment with **iverilog**, **yosys**, and **opensta** already installed.


### Note:
**iverilog, yosys, and opensta** are in the docker environment, however **surfer** is installed in the macOS environment. Make sure you are on the correct terminal to use the respective tools.


Since we already know that our workspace directory is shared between macOS (`/Users/shubhamlanjewar/code/esdcs_docker` here) and docker Ubuntu 22.04.5 (`/macos_local` here), once the `.vcd` file is generated in Ubuntu 22.04.5 environment, we can copy to `/macos_local` in Ubuntu and then go to macOS terminal (e.g. `/Users/shubhamlanjewar/code/esdcs_docker`) and use surfer to view waveforms using the following command:

```bash
surfer test.vcd
```

---

<div align="center">

&nbsp;  
&nbsp;  

</div>

# 📚 Annexures

### 🔹 Annexure A: Required Folders
Apart from installing these tools, you will need the following two folders to follow the further steps of the Tutorial PDF. We will share these folders on Teams for everyone to download:
- `NANGATE_OPEN_STDCELL` - already available on Microsoft Teams
- `tutorials` - will be shared on Microsoft Teams
---

### 🔹 Annexure B: .ova file for OpenRoad
Download the following .ova file for OpenRoad.


Ubuntu 22.04 with OpenRoad: [![Google Drive](https://img.shields.io/badge/Google%20Drive-34A853?logo=googledrive&logoColor=white)](https://drive.google.com/file/d/13iMlf2kCIFxmXj3jm3btuuTqrlR0XK00/view?usp=sharing)

---

### 🔹 Annexure C: Useful Docker Commands(Mandatory)

List Docker containers(this also shows the status of containers also e.g. exited, etc):
[For Intel processors, use `esdcs-ubuntu-img-intel` instead of `esdcs-ubuntu-img`.

```bash
docker ps -a
```

Start the container (next time onwards):
```bash
docker start -ai esdcs-ubuntu
```

Stop the container:
```bash
docker stop esdcs-ubuntu
```

Remove a container:
> ⚠️ Please use with caution! It will remove all data in the Docker container.
```bash
docker rm <container_name>
# Example:
docker rm esdcs-ubuntu
```
---

## Quick Links
- **Git Repo Link**: [EDA Tools Installation](https://github.com/shubhamlanjewar97/ESDCS_EDA_TOOLS)  
- **Tutorial PDF**: Available on Microsoft Teams
---

