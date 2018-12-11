Instructions to set up a decent Linux development environment over Windows using WSL.

1. Install Windows Subsystem for Linux ([Instructions](https://docs.microsoft.com/en-us/windows/wsl/install-win10)). I downloaded the version called simply `Ubuntu` from the store
2. Install [Hyper.js](https://hyper.is) and modify the settings (Ctrl + ,) to open a WSL shell.
```
  shell: 'wsl.exe',
  shellArgs: ['~'],
```
3. Install Atom on Windows
4. Configure atom to use LF line endings by default ([Instructions](https://discuss.atom.io/t/set-default-line-endings-to-unix-on-windows-workstation/12691/15))
5. Create a symlink from home in bash to source directory in windows
```
ln -s /mnt/c/Users/Alfonso/Source ~/Source
```
6. Set up git. Some considerations
  * Disable auto CRLF to ensure not to miss issues with file encodings
    ```
    git config --global core.autocrlf false
    ```
  * Create the SSH keys in windows (e.g. Users/%user%/.ssh) and create a symbolic link to this folder from linux.
