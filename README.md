# Resources for Windows 10/11 on ARM64
## Most items found here are experimental, tool viability can change quickly.
## Take a moment and do your own search for more up to date options.

### VS Build Tools
Microsoft offers ARM64 builds for command line utilities, you may still be required to install the x86 versions to run in emulation mode for some packages to work correctly.
- [VS Build Tools - Direct Link](https://aka.ms/vs/17/release/vs_BuildTools.exe)

### OpenSSL
- [OpenSSL Installer - Download Page](https://slproweb.com/products/Win32OpenSSL.html)

### Python 3
Python 3, support for ARM64 was just added and installer builds are popping up for pre-release builds.  You may want to check the official site's windows pre-releases to see if there is a more up to date version available than the one listed here.
- [Python Windows Download Page](https://www.python.org/downloads/windows/)
- [Python 3.11.0a5 Installer - Download Page](https://www.python.org/downloads/release/python-3110a5/) (Feb 3, 2022)

### Java
Microsoft's OpenJDK builds appear to be the only working implementation at the moment. (Feb 2022)
- [Microsoft's OpenJDK Download Page](https://docs.microsoft.com/en-us/java/openjdk/download)

### .NET
- [.NET 6.0 Download Page](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)

### Visual Studio Code
This is the IDE of choice as the full Visual Studio IDE does not have a native ARM64 build and would run very slowly in x86 emulation mode, if it runs at all.
- [Visual Studio Code Download Page](https://code.visualstudio.com/#alt-downloads)

### PyCharm/IDEA
As of Feb 2022 this is possible but you won't have full functionality, it appears the JetBrains runtime is not yet viable on ARM64.  You can read the method yourself in the ticket [here](https://youtrack.jetbrains.com/issue/JBR-2074) but I'll write out the method as well.  I would highly suggest VSCode as an IDE instead for the time being.
- Install Microsoft's OpenJDK 11, make sure JAVA_HOME is set in your PATH.
- Install [PyCharm](https://www.jetbrains.com/pycharm/download/#section=windows)/[IDEA](https://www.jetbrains.com/idea/download/#section=windows).
- Delete the 'jbr' directory from PyCharm/IDEA's installation folder.
- Add --illegal-access=warn to pycharm.bat/idea.bat on the next line after the line containing %JAVA_EXE% near the bottom.
- Delete runnerw64.exe from the 'bin' directory in PyCharm/IDEA's installation folder.

You should be able to run PyCharm/IDEA with multiple warnings via pycharm.bat/idea.bat in the installation folder.
