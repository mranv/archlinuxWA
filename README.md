# Wazuh Agent for Arch Linux

## Overview

The Wazuh Agent is designed to protect Arch Linux systems with advanced threat prevention, detection, and response capabilities. This repository contains the PKGBUILD and necessary files to build and install the Wazuh Agent package from the Arch User Repository (AUR).

## Package Details

- **Package Base:** wazuh-agent
- **Version:** 4.8.0-1
- **Description:** Wazuh Agent actively protects Arch Linux systems with advanced threat prevention, detection, and response capabilities.
- **Upstream URL:** [Wazuh](https://wazuh.com/)
- **Maintainer:** madara125 (MrHacker) at aur git.
- **Contributor** Anubhav Gain (mranv)

## Dependencies

The following dependencies are required for building the Wazuh Agent package:

- autoconf
- automake
- base-devel
- brotli
- cmake
- curl
- expect
- fakeroot
- gawk
- gcc
- gnupg
- inetutils
- libsigsegv
- libtool
- make
- nodejs
- perl
- perl-base
- python
- sudo

## Installation

### Cloning the Repository

To get started, clone the repository:

```bash
git clone https://github.com/mranv/wazuh-agent-archlinux
cd wazuh-agent-archlinux
```

### Building the Package

Build the package using `makepkg`:

```bash
makepkg -si
```

### Installing the Package

Once the package is built, install it using `pacman`:

```bash
sudo pacman -U wazuh-agent-4.8.0-1-any.pkg.tar.zst
```

## Files in the Repository

- **PKGBUILD**: The build script for creating the Wazuh Agent package.
- **README.md**: This README file.
- **wazuh-agent-\*.aarch64.rpm.sig**: Signature files for aarch64 RPM packages.
- **wazuh-agent-\*.x86_64.rpm.sig**: Signature files for x86_64 RPM packages.
- **wazuh-agent.install**: Script to be run after the package is installed.

## Common Issues

### Agent Fails to Start

Some users have reported issues with the Wazuh Agent failing to start due to problems with `wazuh-execd` or `ossec.conf` errors. Ensure that your configuration files are correct and try restarting the service:

```bash
sudo systemctl restart wazuh-agent
```

If the problem persists, review the logs for any error messages:

```bash
journalctl -u wazuh-agent
```

## Contributing

If you encounter any issues or have suggestions for improvements, please report them on the AUR package page or submit a pull request.

## Contact

For any queries or support, you can contact the maintainer Anubhav Gain (@mranv).
