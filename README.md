 **************************Sudo**************************************
**Definition:** = Command in Unix-like systems allowing users to execute commands with administrative privileges by granting temporary administrative privileges.
**Purpose:** = sudo (superuser do) is a command used in Unix-like operating systems (including Linux) to allow a permitted user to execute commands with elevated privileges, typically as the root user or another specified user.
**Use:** = It is primarily used for system administration tasks such as installing or removing system-wide packages (apt, snap, dpkg), managing services (systemctl), editing system files (nano, vi), and performing other administrative actions that require heightened permissions.
**Use** = sudo allows users to temporarily execute commands with administrative privileges by verifying their identity with a password, ensuring secure and controlled system management. (Tesaile everytime sudo kunai command hane paxi admin password magxa)
**Usage**: Prefix commands needing elevated privileges with sudo.
**Security**: Reduces risks by limiting administrative access.
**Configuration**: Managed via sudoers file for user permissions.


***Top Sudo commands***
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



