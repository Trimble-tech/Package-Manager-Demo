# Sandboxed Packages
As an alternative to traditional package management, there is also a few different methods to install packages inside of a sandbox. A sandbox is the equivalent of putting part of the igloo on an island separate from the rest of the structure. This adds security and makes installation more consistent on different systems but adds complexity.

## Flatpak
- Primarily used for user applications
- *Runtime sandbox*: the application lives on the local filesystem within the flatpak installation directory. Applications are given their own runtime code to depend on and can only touch parts of the system the user specifies.
- Not often installed on a system by default but is easy to get running. The method is distribution specific, so refer <https://flathub.org/setup> for more information.

### Example Commands
- **Search for a package**: `flatpak search PACKAGENAME`
- **Install a package**: `flatpak install PACKAGENAME`
- **Remove a package**: `flatpak remove PACKAGENAME`

## Snap
- Can be used for server or desktop applications.
- *Filesystem sandbox*: the application lives in its own filesystem that mounts on the system, typically this mount happens on boot. Run `lsblk` and you can see the different apps mounted.
- More complex software like server systems can be developed more easily and consistently on Snap as the filesystem sandbox avoids permission or file access issues.
- Mounting the filesystem or accessing it initially can be slow on some systems.

### Example Commands:
- **Search for a package**: `snap search PACKAGENAME`
- **Install a package**: `sudo snap install PACKAGENAME`
- **Remove a package**: `sudo snap remove PACKAGENAME`