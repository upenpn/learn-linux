

## Best Documentation to learn linux 
https://linuxjourney.com/

Introduction to Administrative Privileges: A Comparison Guide for Beginners

## `sudo` Command in Unix-like Systems   

## sudo` (superuser do) 

## SUDO 

- **Definition:**
  - Command in Unix-like systems allowing users to execute commands with administrative privileges by granting temporary administrative privileges.(Every sudo command run gare paxi admin user password halnu paryo which make it temporary adminstrative privileged)
  
- **Purpose:**
  - `sudo` (superuser do) is a command used in Unix-like operating systems (including Linux) to allow a permitted user to execute commands with elevated privileges, typically as the root user or another specified user.
  
- **Use:**
  - Primarily used for system administration tasks such as:
    - Installing or removing system-wide packages (`apt`, `snap`, `dpkg`)
        - apt, snap, and dpkg are all commonly referred to as package managers in the context of Linux systems. 
        - Each serves a specific purpose in managing software packages, dependencies, and installations on a Linux-based operating system
 ## Package Managers in Linux Systems
 
| Package Manager | Description                                                                                      | Purpose                                                                                                     | Strengths                                                                                                    | Example Usage                             |
|-----------------|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| apt             | A command-line tool primarily used in Debian-based distributions like Ubuntu for package management | Handles installation, upgrading, and removal of software packages, relying on repositories for management | Well-suited for managing system-wide packages and dependencies from official repositories                 | `sudo apt install package_name`           |
| snap            | A software packaging and deployment system developed by Canonical for Ubuntu                     | Manages self-contained Snap packages with all dependencies bundled                                         | Offers isolation and security benefits, allowing independent distribution and updates of applications   | `sudo snap install package_name`          |
| dpkg            | Low-level package manager used in Debian-based distributions, including Ubuntu                  | Handles installation, removal, and information about .deb packages                                          | Useful for manual package management or troubleshooting tasks                                           | `sudo dpkg -i package_name.deb`          |

## Similarities and Differences

| Feature               | apt                                                           | snap                                                             | dpkg                                                             |
|-----------------------|---------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------|
| Installation Source   | Online repositories maintained by the distribution           | Snap Store (online platform by Canonical)                       | `.deb` files downloaded from the internet or other sources       |
| Dependency Handling   | Automatic resolution of dependencies                          | Self-contained packages with bundled dependencies               | Manual resolution of dependencies (not automatic)                |
| Installation Command  | `sudo apt install package_name`                               | `sudo snap install package_name`                               | `sudo dpkg -i package_name.deb`                                   |
| After Removal         | Removes package and configuration files                        | Completely removes package and its dependencies                 | Removes package but retains configuration files                   |
| Cleanup of Unused Dependencies | `sudo apt autoremove`                                      | Automatically handled by snap (no residual dependencies)        | Manual purging of unused dependencies with `sudo dpkg -P`         |
| Safety                | Generally safe due to curated repositories                    | Generally safe due to sandboxed packages and Snap Store         | Safe when used with trusted `.deb` packages                       |
| When to Use           | Suitable for everyday software installations                  | Suitable for isolated packages, bleeding-edge software         | Suitable for specific package installations and control          |
| Recommended Use Case  | Desktop and server applications, system utilities             | Development, testing, and experimental software                | Advanced users requiring specific package management              |
| Example 1             | `sudo apt update` (Updates package lists)                     | `sudo snap refresh` (Updates snap packages)                     | `sudo dpkg -l` (Lists installed packages)                         |
| Example 2             | `sudo apt upgrade` (Upgrades installed packages)              | `sudo snap revert package_name` (Reverts a snap package)        | `sudo dpkg -r package_name` (Removes a package)                   |
| Example 3             | `sudo apt remove package_name` (Removes a package)            | `sudo snap disable package_name` (Disables a snap package)      | `sudo dpkg -i package_name.deb` (Installs a `.deb` package)       |
| Example 4             | `sudo apt search keyword` (Searches for packages)             | `sudo snap find keyword` (Searches for snaps)                   | `sudo dpkg -S /path/to/file` (Locates which package a file belongs to) |
| Example 5             | `sudo apt list --upgradable` (Lists upgradable packages)      | `sudo snap list --all` (Lists all installed snaps)              | `sudo dpkg --configure -a` (Configures all unconfigured packages) |
| Example 6             | `sudo apt full-upgrade` (Upgrades packages with dependencies) | `sudo snap info package_name` (Displays information about a snap) | `sudo dpkg-reconfigure package_name` (Reconfigures a package)    |
| Installation Example  | `sudo apt install firefox` (Installs Firefox browser)         | `sudo snap install spotify` (Installs Spotify music player)     | `sudo dpkg -i slack.deb` (Installs Slack messaging app)          |


**Similarities:**
- Handle software packages on Linux systems
- Support installation, upgrading, and removal of packages
- Manage dependencies and resolve conflicts automatically

**Differences:**
- `apt` and `dpkg` are specific to Debian-based systems, while `snap` is more universal
- `apt` and `dpkg` rely on repositories for package management, while `snap` uses self-contained packages
- `snap` offers isolation and security benefits by bundling dependencies with packages


- Managing services (`systemctl`)

| Action                  | `systemctl` Command                                          | Description                                                          | Example                              |
|-------------------------|--------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------|
| Start a Service         | `sudo systemctl start service_name`                          | Starts the specified service                                         | `sudo systemctl start nginx`         |
| Stop a Service          | `sudo systemctl stop service_name`                           | Stops the specified service                                          | `sudo systemctl stop nginx`          |
| Restart a Service       | `sudo systemctl restart service_name`                        | Restarts the specified service                                       | `sudo systemctl restart nginx`       |
| Enable a Service        | `sudo systemctl enable service_name`                         | Enables the specified service to start at boot                        | `sudo systemctl enable nginx`        |
| Disable a Service       | `sudo systemctl disable service_name`                        | Disables the specified service from starting at boot                   | `sudo systemctl disable nginx`       |
| Check Service Status    | `sudo systemctl status service_name`                         | Displays the status of the specified service                           | `sudo systemctl status nginx`        |
| View Service Logs       | `sudo journalctl -u service_name`                            | Displays logs related to the specified service                         | `sudo journalctl -u nginx`            |
| List All Services       | `sudo systemctl list-unit-files --type=service`              | Lists all available services                                          | `sudo systemctl list-unit-files --type=service` |
| View Service Unit File  | `sudo systemctl cat service_name`                            | Displays the content of the unit file for the specified service       | `sudo systemctl cat nginx`            |
| Reload Service Settings | `sudo systemctl reload service_name`                         | Reloads the configuration of the specified service                     | `sudo systemctl reload nginx`         |
| View Active Services    | `sudo systemctl list-units --type=service --state=active`    | Lists all currently active services                                   | `sudo systemctl list-units --type=service --state=active` |

    - Editing system files (`nano`, `vi`)
  | Action                  | `nano` Command                             | `vi` Command                               | Description                                               | Example                                            |
|-------------------------|--------------------------------------------|--------------------------------------------|-----------------------------------------------------------|----------------------------------------------------|
| Open/Edit a File        | `nano /path/to/file`                       | `vi /path/to/file`                         | Opens the specified file for editing                       | `nano /etc/nginx/nginx.conf`                       |
| Save and Exit           | `Ctrl + O`, then `Enter`, then `Ctrl + X`  | `:wq` or `:x`                              | Saves changes and exits the editor                           | `Ctrl + O`, `Enter`, `Ctrl + X` (in nano)          |
| Exit Without Saving     | `Ctrl + X`                                 | `:q!`                                      | Exits the editor without saving changes                      | `Ctrl + X` (in nano) or `:q!` (in vi)             |
| Move Cursor             | Arrow keys                                 | Arrow keys or `hjkl` keys                  | Moves the cursor within the file                             | Arrow keys or `hjkl` keys                         |
| Insert/Edit Text        | Type directly                              | Press `i` to enter insert mode, then type  | Allows inserting or editing text in the file                 | Type directly (in nano) or `i` then type (in vi)   |
| Delete Text             | `Backspace` or `Delete` keys               | `x` or `dd`                                | Deletes characters or lines of text                           | `Backspace` or `Delete` (in nano) or `x` or `dd` (in vi) |
| Save Changes            | `Ctrl + O`, then `Enter`                   | `:w` or `:wq`                              | Saves changes to the file                                     | `Ctrl + O`, `Enter` (in nano) or `:w` (in vi)      |
| Exit Insert Mode        | `Ctrl + X`                                 | `Esc`                                      | Exits insert mode (if applicable)                             | `Ctrl + X` (in nano) or `Esc` (in vi)             |
| Search for Text         | `Ctrl + W`, then type search query         | `/search_term`                             | Searches for a specific text within the file                  | `Ctrl + W`, type search query (in nano)            |
| Undo                    | `Ctrl + Shift + _`                         | `u`                                        | Undoes the last change made to the file                        | `Ctrl + Shift + _` (in nano) or `u` (in vi)       |
| Redo                    | `Alt + U`                                  | `Ctrl + R`                                 | Redoes the last undone change                                  | `Alt + U` (in nano) or `Ctrl + R` (in vi)        |
| Open New/Blank File     | `nano`                                     | `vi` or `vim`                              | Opens a new or blank file for editing                          | `nano` (to open a new file in nano)                |
| Save As                 | `Ctrl + O`, then `Enter`, then enter filename | `:w filename`                           | Saves the current file with a new name                         | `Ctrl + O`, `Enter`, enter filename (in nano)       |
| Copy Text               | `Alt + 6`, then move cursor                | `yy`                                       | Copies selected text (highlight text then use command)         | `Alt + 6`, move cursor (in nano) or `yy` (in vi)  |
| Paste Text              | `Ctrl + U`                                 | `p`                                        | Pastes copied text                                             | `Ctrl + U` (in nano) or `p` (in vi)               |

    - Performing other administrative actions that require heightened permissions
  - Allows users to temporarily execute commands with administrative privileges by verifying their identity with a password.
  
- **Usage:**
  - Prefix commands needing elevated privileges with `sudo`.
  
- **Security:**
  - Reduces risks by limiting administrative access.
  
- **Configuration:**
  - Managed via `sudoers` file for user permissions.



## ***Top Sudo commands***
| Command                              | Purpose and Use                                                  | Example(s)                                       |
|--------------------------------------|------------------------------------------------------------------|--------------------------------------------------|
| sudo apt update                      | Refreshes the list of available packages                         | sudo apt update                                  |
| sudo apt upgrade                     | Upgrades all installed packages to their latest versions         | sudo apt upgrade                                 |
| sudo apt install <package>           | Installs a new package                                           | sudo apt install nginx                          |
| sudo apt remove <package>            | Removes a package                                                | sudo apt remove nginx                           |
| sudo apt purge <package>             | Removes a package along with its configuration files             | sudo apt purge nginx                            |
| sudo apt autoremove                  | Removes automatically installed dependency packages              | sudo apt autoremove                             |
| sudo dpkg -i <package.deb>           | Installs a .deb package file                                     | sudo dpkg -i package.deb                        |
| sudo dpkg -r <package>               | Removes a package installed via .deb file                        | sudo dpkg -r nginx                              |
| sudo systemctl restart <service>     | Restarts a system service                                        | sudo systemctl restart apache2                  |
| sudo systemctl start <service>       | Starts a system service                                          | sudo systemctl start nginx                      |
| sudo systemctl stop <service>        | Stops a running system service                                   | sudo systemctl stop apache2                     |
| sudo systemctl enable <service>      | Enables a service to start automatically on boot                 | sudo systemctl enable nginx                     |
| sudo systemctl disable <service>     | Disables a service from starting automatically on boot           | sudo systemctl disable apache2                  |
| sudo systemctl status <service>      | Shows the status of a system service                             | sudo systemctl status nginx                    |
| sudo systemctl reload <service>      | Reloads configuration changes for a running service              | sudo systemctl reload apache2                  |
| sudo journalctl                      | Displays system logs                                            | sudo journalctl -u nginx                         |
| sudo chown <user>:<group> <file>     | Changes the ownership of a file or directory                    | sudo chown root:root /etc/nginx/nginx.conf      |
| sudo chmod <permissions> <file>      | Changes the permissions of a file or directory                   | sudo chmod 644 /var/www/html/index.html         |
| sudo rm <file>                       | Removes (deletes) a file                                         | sudo rm /var/log/nginx/access.log               |



## Introduction to Administrative Privileges: A Comparison Guide for Beginners

| **Operating System/Environment** | **Equivalent Concept**                          | **Description and Background**                                                                                                                                                                                                             |
|----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Unix-like Systems (Linux, BSD)**| `sudo`                                          | `sudo` (superuser do) is a command used in Unix-like operating systems to allow a permitted user to execute commands with elevated privileges, typically as the root user or another specified user. It verifies the user's identity with a password, enhancing security by limiting administrative access.  |
| **Windows**                      | Run as Administrator                           | Windows allows users to execute programs or commands with elevated privileges by right-clicking and selecting "Run as administrator". This is necessary for tasks requiring administrative rights to system settings or files.            |
| **macOS**                        | `sudo`                                          | macOS, based on Unix, also utilizes `sudo` for similar purposes as in Unix-like systems. It provides a secure method for authorized users to perform administrative tasks without needing to switch user contexts entirely.              |
| **Kubernetes**                   | `kubectl`                                       | `kubectl` is the Kubernetes command-line tool that allows administrators to interact with Kubernetes clusters. Administrative tasks require proper authentication and authorization, ensuring secure management of cluster resources. |
| **Docker**                       | Docker Commands (`docker`)                      | Docker provides a `docker` command-line interface where users can execute container management commands. On Unix-like systems, these commands often require `sudo` or membership in the `docker` group for elevated privileges.    |
| **Android**                      | Root Access                                     | Root access on rooted Android devices grants users administrative privileges to modify system settings, install custom software, and perform advanced system-level operations not typically available to standard users.       |
| **IBM z/OS**                     | Authorized Program Facility (APF)               | APF on IBM z/OS enables authorized programs to run with elevated privileges, bypassing normal security checks. This is crucial for system utilities and applications that require unrestricted access to system resources.          |
| **VMS (OpenVMS)**                | Privileged Access                               | VMS provides privileged access mechanisms that allow authorized users to execute commands with enhanced privileges beyond their standard permissions. This is essential for managing system-wide configurations and operations.    |
| **IBM z/VM**                     | Superuser Privileges                            | On IBM z/VM mainframes, superuser privileges grant users administrative capabilities to oversee and control virtual machines and system resources. This ensures efficient management and operation of the virtualized environment. |
