A shell script that allows to download and install Docker Engine with a single command specifically for Linux Mint.

## Prerequisites
- Ensure you have a compatible Linux distribution.
- You may need `sudo` privileges to install Docker.

## Pre-Installation
Before downloading the script, ensure you are in the desired directory where you want the script to be saved. You can check your current directory by running: `pwd`

Once the installation is complete, you can delete the script if you no longer need it. It does not affect the Docker installation; the script's downloaded location is simply for convenience.

## Download the Script

### For **MINT**

  `wget https://raw.githubusercontent.com/bdsahiner/install-docker-engine-on-Mint-22/main/docker-engine-mint22.sh`
  
### For **UBUNTU**

  `wget https://raw.githubusercontent.com/bdsahiner/install-docker-engine-on-Mint-22/main/docker-engine-ubuntu.sh`

## Make the Script Executable

  `chmod +x docker-engine-mint22.sh`

## Run the Script

  `./docker-engine-mint22.sh`

## Post-Installation
Once the installation is complete, you will see an output similar to: Docker version `version_number` build `build_number`

## Manage Docker as a non-root user
This allows you to run Docker commands, such as 
  `docker run hello-world`, 
without needing to prepend `sudo` each time.

Warning: The docker group grants root-level privileges to the user.

  `sudo groupadd docker`
  
  `sudo usermod -aG docker $USER` 

You can use the `whoami` command to find your username($USER)
  
  `newgrp docker`

## Uninstall Docker Engine

  `sudo apt-get purge docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin docker-ce-rootless-extras`
  
  `sudo rm -rf /var/lib/docker`
  
  `sudo rm -rf /var/lib/containerd`

## Disclaimer
This project is not affiliated with, endorsed by, or associated with Docker, Inc. 
The script provided in this repository is intended solely for educational purposes. 
The author disclaims any liability for any direct or indirect damages or issues that may arise from the use of this script or the installation of Docker. 
