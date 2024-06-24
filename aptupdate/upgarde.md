## sudo apt update
- What it does: It updates the list of available packages and their versions, but it does not install or upgrade any packages.
W- hy it's useful: This ensures that your system knows about the latest versions of the packages you have installed or that are available for installation.
H- ow it works: It fetches the latest package information from the repositories listed in /etc/apt/sources.list and other sources.

## sudo apt upgrade
- What it does: It installs the latest versions of all the packages currently installed on your system.
- Why it's useful: This keeps your system up to date with the latest features, improvements, and security patches.
- How it works: After apt update has been run and the package information is up-to-date, apt upgrade will download and install the updated packages.