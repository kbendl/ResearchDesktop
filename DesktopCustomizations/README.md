# Desktop Customizations
This section contains ideas and implementations how to change a plain Linux desktop into a Research Desktop. This involves adding icons to the desktop and also modifying the global application menu. The goal is to provide users with a desktop that makes it easy to run scientific applications and workflows.  
Most of the tools are based on the [MATE Desktop Environment](https://mate-desktop.org/) but can be adapted for other desktop environments.

## Interactive Job
New users find it hard to run an interactive job in the batch system. One way to get users to try running in the batch system is to initially hide the functionality behind an icon on the desktop. Here is an animation how this could look like. Note that the command that is used to launch the interactive job is printed into the terminal. This allows new users to learn how to launch on interactive job themselves. 

<img src="https://github.com/RobertHenschel/ResearchDesktop/blob/main/DesktopCustomizations/InteractiveJob/interactiveJob.gif" width="75%">

All scripts and icons to implement this functionality are available in the [InteractiveJob directory](./InteractiveJob/README.md) in this repository. This page also contains a guide how to implement this functionality in your cluster. One tool to push configuration out to all users is to use the [Desktop Customer](https://www.cendio.com/resources/docs/tag/tldc.html) that ships with ThinLinc. A guide how to use the Desktop Customizer is available in the [ThinLinc Community](https://community.thinlinc.com/t/how-can-i-customise-the-desktop-environment-within-a-thinlinc-session/717).

## ThinDrive / Shared Folder
Most users would like to share files and folders from a users laptop or workstation with the HPC system. Tools like [WinSCP](https://winscp.net/), [FileZilla](https://filezilla-project.org/) and [Cyberduck](https://cyberduck.io/) make this pretty easy for users. However, these solutions only allow moving files from one system to the other, creating a copy of the data in that process. If users want to simply browse files and directories from their laptop on the Research Desktop, tools like [ThinDrives](https://www.cendio.com/resources/docs/tag/client_options_local_devices.html) make this possible.

<img src="https://github.com/RobertHenschel/ResearchDesktop/blob/main/DesktopCustomizations/ThinDrive/thinDrive.gif" width="75%">

The script and icon to implement this functionality are available in the [ThinDrive directory](./ThinDrive/README.md). If you provide your own documentation, consider replacing the link in the script to point to your documentation rather than the one provided by Cendio.

## Graphical Application on a Compute Node
Most graphical applications can be run directly on the desktop, but there are applications that require more resources than a shared desktop environment can provide. Such applications can be launched in the batch system and the graphical user interface will be displayed on the desktop. Depending on the configuration of the batch system and the desktop, users will see no difference between launching an application on desktop or through the batch system.

<img src="https://github.com/RobertHenschel/ResearchDesktop/blob/main/DesktopCustomizations/AppOnComputeNode/FijiOnComputeNode.gif" width="75%">

All scripts and icons to implement this functionality are available in the [AppOnComputeNode directory](./AppOnComputeNode/README.md) in this repository. This page also contains a guide how to implement this functionality in your cluster. 
