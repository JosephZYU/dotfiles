⭐ Strictly follow the official link from Microsoft: https://docs.microsoft.com/en-us/windows/wsl/install-win10#step-4---download-the-linux-kernel-update-package

  Search keyword "Customizing Your Terminal" from Corey's home page: https://www.youtube.com/c/Coreyms/featured

  Origina GitHub Repo: https://github.com/mathiasbynens/dotfiles

  Video Instructions: https://youtu.be/c5RZWDLqifA?t=790

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Step 1 - Enable the Windows Subsystem for Linux
    Open PowerShell as Administrator and run:

    💲 dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart


Step 2 - Check requirements for running WSL 2
    NOTE: For x64 systems: Version 1903 or higher, with Build 18362 or higher.
    Open PowerShell or CMD and run:

    💲 winver

Step 3 - Enable Virtual Machine feature
    Before installing WSL 2, you must enable the Virtual Machine Platform optional feature. Your machine will require virtualization capabilities to use this feature.
    Open PowerShell as Administrator and run:

    💲 dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
    
    (Optional - restart your machine to complete the WSL install and update to WSL 2.)

Step 4 - Download the Linux kernel update package
    Download the latest package:

    ⏬ https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi


Step 5 - Set WSL 2 as your default version
    Open PowerShell and run this command to set WSL 2 as the default version when installing a new Linux distribution:

    💲 wsl --set-default-version 2

Step 6 - Install your Linux distribution of choice
    Download from Microsoft Store or click the link for Ubuntu 20.04 LTS:

    ⏬ https://www.microsoft.com/en-sg/p/ubuntu-2004-lts/9n6svws3rx71?rtc=1

------------------------------------------------------------------------------------------------------------------------------------------------------------------------

⭐⭐⭐ https://www.liquidweb.com/kb/how-to-install-and-update-python-to-3-9-in-ubuntu/ ⭐⭐⭐

PUT ALL TOGETHER
    💲 sudo apt -y update && sudo apt -y upgrade
    💲 sudo apt install software-properties-common && sudo add-apt-repository ppa:deadsnakes/ppa && sudo apt -y update && sudo apt install python3.9 python3.9-venv python3.9-dev

# Check your current versino of Python
    💲 python --version

# Update and Refresh Repository Lists
# -y: YES to all update! 😎
    💲 sudo apt -y update
    (NOTE: you MUST complete this update before installing pip ❗)

    (💲 apt list --upgradable) - Optional
    (💲 sudo apt -y upgrade) - Optional

Finally, we run the installation to add the latest version of Python. 
As an aside, we have opted to install the -dev and -venv features as well. 
This ensures we have Python 3.8, pip, and virtualenv. 

    💲 sudo apt install python3.9
    💲 sudo apt install python3.9 python3.9-venv python3.9-dev
    💲 sudo apt install python3.9 python3.9-venv python3.9-dev python3-pip (NOTE: NOTE yet tested)

# Verify installaion
    💲 python3.9 -V
    💲 ls /usr/bin/python*

# Clean Up
After a successful installation, remove the downloaded archive to save disk space
    💲 cd /usr/src/
    💲 rm -f Python-3.8.6.tgz (rm -f Python*)