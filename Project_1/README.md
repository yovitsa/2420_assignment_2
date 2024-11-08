# ACIT 2420 Assignment 2
# Project 1

Project 1 includes:

  1. dotfiles
  2. install_packages
  3. main
  4. README.md

## Files Overview

1. **`dotfiles`**  
   dotfiles will check if certain directories exist, and it will create them if they don't exist
   dotfiles also creates symoblic links for xertain directories if they do not exist
   

   - **Functionality of dotfiles**:
     - Checks for directories such as `~/.config/kak`, `~/.config/tmux`, and `~/bin`.
     - Creates the necessary directories if they don’t exist.
     - Sets up symbolic links for dotfiles in those directories.
   - **Usage**:
     Run the script to ensure required configuration directories and links are set up correctly.

2. **`install_packages`**  
   install_packages script installs packages `kakoune` and `tmux`.

   - **Functionality**:
     - Stores package names in a variable.
     - Iterates through the package list and installs each package if it’s not already installed.
     - Sends a message to the user about the package installation status.
   - **Usage**:
     Run this script to install all necessary packages for the setup.

3. **`main_script`**  
   main_script requires root privileges to run, it executes both scripts, `dotfiles` and `install_packages`.

   - **Functionality**:
     - Checks if the script is run as root and exits if it’s not, prompting the user to use `sudo`.
     - Defines paths to the `dotfiles` and `install_packages` scripts.
     - Executes the `install_packages` script to install required software.
     - Executes the `dotfiles` script to set up configuration files.
   - **Usage**:
     Run this script as root to initialize the entire setup process:
     ```
     sudo ./main_script
     ```

## Getting Started

1. Clone this repository.
2. Run the `main_script` with root privileges to initiate the setup:
   ```bash
   sudo ./main_script
   ```

#
## References


- **Bash scripting**: [Bash Cheat Sheet](https://devhints.io/bash)
- **SFTP command**: [Linux SFTP Command](https://linuxize.com/post/how-to-use-linux-sftp-command-to-transfer-files/)
- **Pacman package manager**: [Arch Linux Pacman Guide](https://wiki.archlinux.org/title/Pacman)
- **Condition for Sudo Access**: [Check if Script is Running as Root](https://tecadmin.net/check-if-a-script-is-running-as-root-user-in-linux/)
- **Symbolic Links**: [Creating Symbolic Links with `ln`](https://linuxize.com/post/how-to-create-symbolic-links-in-linux-using-the-ln-command/)
- **Cut command**: [Linux Cut Command](https://linuxize.com/post/linux-cut-command/)
- **tee command**: [tee Command](https://www.geeksforgeeks.org/tee-command-linux-example/)
