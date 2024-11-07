# Dotfiles Environment Setup

This project includes a series of Bash scripts for setting up a development environment. The setup consists of managing configuration dotfiles, installing necessary packages, and running a main setup script.

## Files Overview

1. **`dotfiles`**  
   This script checks for the existence of specific configuration and binary directories and creates them if they don't exist. It also manages symbolic links for organizing configuration files.

   - **Functionality**:
     - Checks for directories such as `~/.config/kak`, `~/.config/tmux`, and `~/bin`.
     - Creates the necessary directories if they don’t exist.
     - Sets up symbolic links for dotfiles in those directories.
   - **Usage**:
     Run the script to ensure required configuration directories and links are set up correctly.

2. **`install_packages`**  
   A script to install essential packages needed for the development environment, such as `kakoune` and `tmux`.

   - **Functionality**:
     - Stores package names in a variable for easy modification.
     - Iterates through the package list and installs each package if it’s not already installed.
     - Provides output to inform the user of package installation status.
   - **Usage**:
     Run this script to install all necessary packages for the setup.

3. **`main_script`**  
   The central script that requires root privileges to run, managing the execution of both the `dotfiles` and `install_packages` scripts.

   - **Functionality**:
     - Checks if the script is run as root and exits if it’s not, prompting the user to rerun with `sudo`.
     - Defines paths to the `dotfiles` and `install_packages` scripts.
     - Executes the `install_packages` script to install required software.
     - Executes the `dotfiles` script to set up configuration files.
   - **Usage**:
     Run this script as root to initialize the entire setup process:
     ```bash
     sudo ./main_script
     ```

## Getting Started

1. Clone the repository and navigate into the project directory.
2. Run the `main_script` with root privileges to initiate the setup:
   ```bash
   sudo ./main_script


## References:

## References

For additional context and understanding of the commands and concepts used in this project, see the following resources:

- **Bash scripting**: [Bash Cheat Sheet](https://devhints.io/bash)
- **SFTP command**: [Linux SFTP Command](https://linuxize.com/post/how-to-use-linux-sftp-command-to-transfer-files/)
- **Pacman package manager**: [Arch Linux Pacman Guide (Section 1.6)](https://wiki.archlinux.org/title/Pacman)
- **Condition for Sudo Access**: [Check if Script is Running as Root](https://tecadmin.net/check-if-a-script-is-running-as-root-user-in-linux/)
- **Symbolic Links**: [Creating Symbolic Links with `ln`](https://linuxize.com/post/how-to-create-symbolic-links-in-linux-using-the-ln-command/)
- **Cut command**: [Linux Cut Command](https://linuxize.com/post/linux-cut-command/)
