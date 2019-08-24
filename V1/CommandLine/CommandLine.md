---
uid: commandLine
---

# Command line configuration of Edge Data Store

Configuration and administration of the Edge Data Store on Linux and Windows can also be accomplished using the edgecmd command line tool. On Windows it is located in the directory:

```cmd
C:\Program Files\OSIsoft\EdgeDataStore\edgecmd.exe
```

You should specify the full path when using it on Windows.

On Linux the utility is installed in:

```bash
 /opt/OSIsoft/EdgeDataStore/edgecmd
```

On Linux it can be accessed without using the full path. For the sake of simplicity the utility for the rest of this topic will be referred to as edgecmd, even though it is named edgecmd.exe on Windows and edgecmd on Linux.

Most configurations options that can be done using REST can also be done using the edgecmd utility and command line arguments. Generally the configuration and administrative REST interfaces are exposed via the command line. Access to reading and writing data to the Edge Data Store Storage Component - OMF Ingress and SDS Read/Write capabilities are only available using the REST API.

