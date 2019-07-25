---
uid: managementTools
---

# Tools for Managing the Edge System

## REST Tools

### curl

The documentation for the Edge System uses curl for configuration and management examples. curl is a command line tool supported on Windows and Linux that makes HTTP calls. It has a large range of capabilities that are very compact - any administrative or programming task using the Edge System can be accomplished using curl. curl can easily be scripted using BASH or Powershell on either Linux or Windows and is the recommended tool for managing the Edge System. Any system that can run the Edge System can support curl.

### Postman

For systems with Graphical UI components (Edge is supported on platforms that lack this capability) Postman is a very popular and effective REST tool. It is particularly useful for learning more about the Edge System REST APIs.

### C#, Python, Go

Any modern programming language can also be used to make REST calls to administer and write programs for the Edge System. Since the administrative and programming interfaces are unified in using REST, it is possible to write applications that both manage the Edge System and read and write data. The Diagnostics namespace, for example, can be accessed locally to monitor and act upon local system state if desired.

### System Tools

Many OSIsoft customers use Windows computers, even though they may deploy Linux devices to host Edge Storage. The Edge System can be installed and run on Windows 10, and the same custom applications developed on Windows should work on Linux, as long as the application development environment is supported on Linux. The Edge System has been designed to use platform independent programming. To facilitate working with Linux devices, Windows tools like PuTTY and WinSCP are very useful for copying files and accessing Linux command lines remotely.
