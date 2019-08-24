---
uid: linuxWindows
---

# Linux and Windows platform differences

When developing applications to work with the Edge Data Store, there is no difference in expected behavior between Linux and Windows installations. There are some differences in how Edge Data Store is installed between Linux and Windows, to follow best practices on both platforms.

## Windows file locations

Program binaries are placed in the C:\Program Files\OSIsoft\EdgeDataStore directory by default. for information about changing this location see the [installation](#installationOverview) documentation. 

Configuration, log, and data files are placed under C:\ProgramData\OSIsoft\EdgeDataStore\ This is not configurable. This folder structure will not be automatically removed during uninstallation.  For information about clearing these files, see the [installation](#installationOverview) documentation.

Key material for configuration files' encrypted secrets is stored using the Windows DPAPI in a secure Windows store. This is not configurable.

## Linux file locations

Program binaries are placed in the /opt/EdgeDataStore directory.  Configuration, log, and data files are placed under /usr/share/OSIsoft/EdgeDataStore. This folder structure will not be automatically removed during uninstallation. For information about clearing these files, see the [installation](#installationOverview) documentation.

Key material for configuration files' encrypted secrets are stored using limited access files under /usr/share/OSIsoft/EdgeDataStore. File locations for Linux are not user configurable.

When the Debian installer is used the Edge Data Store is installed using the service identity osisoft.edgedatastore.service. If you have a need to restart the service from the Linux command line you can use the following command:

```bash
sudo systemctl restart osisoft.edgedatastore.service
```

