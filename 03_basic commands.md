# Basic Commands
1. Update the package cache from repos
- **APT**: `sudo apt update`
- **DNF**: `sudo dnf clean all && sudo dnf makecache`
    - *Note that DNF refreshes cache automatically, so this **only** needs to be done if you encounter issues or add a repository.*
- **Pacman**: `sudo pacman -Sy`

2. Install system updates
- **APT**: `sudo apt upgrade` (consider running `sudo apt list --upgradable`)
- **DNF**: `sudo dnf update`
- **Pacman**: `sudo pacman -Su`

3. Find a package
- **APT**: `apt search PACKAGENAME`
- **DNF**: `dnf search PACKAGENAME`
- **Pacman**: `pacman -Ss PACKAGENAME`

4. Show information about packages
- **APT**: `apt show PACKAGENAME`
- **DNF**: `dnf info PACKAGENAME`
- **Pacman**: `sudo pacman -Su pkgfile && sudo pkgfile --update && sudo pkgfile -s PACKAGENAME`

5. Install a package
- **APT**: `sudo apt install PACKAGENAME`
- **DNF**: `sudo dnf install PACKAGENAME`
- **Pacman:** `sudo pacman -Su PACKAGENAME`

6. Remove a package
- **APT**: `sudo apt remove PACKAGENAME`
- **DNF**: `sudo dnf remove PACKAGENAME`
- **Pacman**: `sudo pacman -R PACKAGENAME`