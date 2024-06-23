

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
    - Managing services (`systemctl`)
    - Editing system files (`nano`, `vi`)
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
