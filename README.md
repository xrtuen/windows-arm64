# Resources for Windows 10/11 on ARM64
## Most items found here are experimental and in some cases may work better in Windows 11.

### VS Build Tools
Microsoft offers ARM64 builds for command line utilities, you may still be required to install the x86 versions to run in emulation mode for some packages to work correctly.
- [VS Build Tools - Direct Link](https://aka.ms/vs/17/release/vs_BuildTools.exe)

### OpenSSL
Compiling OpenSSL requires NASM, an x86 assembler, which as you might guess is rather frustrating on an ARM64 architecture.  At the moment this installer is an actual rainbow unicorn.
- [OpenSSL Installer - Download Page](https://slproweb.com/products/Win32OpenSSL.html)

### Python 3
Python 3, support for ARM64 was just added and installer builds are popping up for pre-release builds.  You may want to check the official site's windows pre-releases to see if there is a more up to date version available than the one listed here.
- [Python Windows Download Page](https://www.python.org/downloads/windows/)
- [Python 3.11.0a5 Installer - Download Page](https://www.python.org/downloads/release/python-3110a5/) (Feb 3, 2022)
- 
