`apt/apt-get [options] [command] [package(s)]`

#### **options:** 
- `-y`: Automatically answers "yes" to all prompts during execution.
- `-s`: Simulates the command without making any changes to the system, useful for previewing the result before execution.

#### **update commands**:
- **`update`**: Updates the package lists for available software packages from the configured repositories.
- **`dietpi-update`**: Specifically updates DietPi OS packages. 
#### **upgrade commands:**
- **`upgrade`**: Upgrades all the installed packages to the latest versions.
- **`full-upgrade`**: Installs the latest versions of the packages installed on the system. Requires an `update` beforehand to ensure new versions are available.
- **`dist-upgrade`**: Performs an upgrade while handling changing dependencies and may remove less important packages to make space for necessary ones.

#### **Other Package Commands:**
- **`download`**: Downloads the specified binary package to the current directory.
- **`reinstall`**: Reinstalls a package to reset it to its default state.
- **`remove`**: Removes a package but leaves its configuration files.
- **`check`**: Updates the package cache and checks for broken dependencies.
- **`purge`**: Removes a package and its configuration files.
- **`clean`**: Cleans the system by removing cached package files that were downloaded during installation.
- **`show`**: Displays detailed information about a package, including its installation status, version, description, dependencies, and other metadata.
- **`list`**: Lists details (version, architecture, repository source) about installed or available packages.

#### **System Control:**
- **`shutdown [OPTIONS] [TIME] [MESSAGE]`**: Shuts down the system. Example: `sudo shutdown -h now` to halt immediately.
- **`reboot`**: Reboots the system. Example: `shutdown -r now` or `reboot`.
- **`update & upgrade`**: Update and upgrade packages in one command:

```shell
  sudo apt update && sudo apt upgrade -y
```


#linuxcommand 