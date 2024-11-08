# Project 2

# New User Creation Script
Project 2 includes:

 1. new_user script 
 2. README.md file. 

The `new_user` script function is to create a new user. The script provides options for username, shell, home directpry and groups.
Script ust be run with root privilages.

## Functionality

1. **Root Check**  
   - If the script is not run as root, it displays an error message prompting the user to run it with `sudo` and exits.

2. **Usage function**  
   - `usage` function that displays information on the required and optional arguments.
   - Displays the usage information if the required arguments are not supplied.

3. **New User Creation**  
   - Accepts options to specify the following properties for the new user:
     - **Username** (`-u`): Required. Specifies the username of the new account.
     - **Login Shell** (`-s`): Optional. Defines the login shell (defaults to `/bin/bash` if not provided).
     - **Home Directory** (`-h`): Optional. Specifies a custom home directory path.
     - **Groups** (`-g`): Optional. Adds the new user to one or more groups.
   - Creates the user with these specified options.

4. **Error Handling**  
   - Checks if each option is provided and displays usage information if any required option is missing.
   - Sends a message to the user is successful creation or if any errors have been encountered.
5. **Password creation**
   - The scripts autoamtilcaly prompts a user to create a password.
## Usage

To run the script, use the following syntax:
```bash
sudo ./new_user -u username -p password -s shell -h home_dir -g groups
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
