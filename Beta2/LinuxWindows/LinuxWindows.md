---
uid: linuxWindows
---

# Linux and Windows Platform Differences

When developing applications that work with the Edge System, there is no difference in expected behavior between Linux and Windows installations.

There are some differences in how the Edge System is installed between Linux and Windows to follow best practices on both platforms.

## Windows File Locations

Program binaries are placed in the C:\Program Files\OSIsoft\EdgeSystem directory by default. See the [installation](#installationOverview) documentation for information about changing this location.

Configuration, log, and data files are placed under C:\ProgramData\OSIsoft\EdgeSystem\ - this is not configurable. This folder structure will not be automatically removed during uninstallation - see the [installation](#installationOverview) documentation for information about clearing these files.

Key material for configuration files' encrypted secrets are stored using the Windows DPAPI in a secure Windows store. This is not configurable.

## Linux File Locations

Program binaries are placed in the /opt/EdgeSystem directory.

Configuration, log, and data files are placed under /usr/share/OSIsoft/EdgeSystem. This folder structure will not be automatically removed during uninstallation - see the [installation](#installationOverview) documentation for information about clearing these files.

Key material for configuration files' encrypted secrets are stored using limited access files under /usr/share/OSIsoft/EdgeSystem.

File locations for Linux are not user configurable.
