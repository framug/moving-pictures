# About This Document #
### Introduction ###
This document will walk you through setting up your development environment to contribute to the Moving Pictures project. If you follow this guide, you should be able to retrieve the latest version of the source code, make bug fixes or enhancements, and submit your changes. This guide details a development environment utilizing Visual Studio 2008 Express and Tortoise SVN, both available for free. It is of course possible to use the full version of Visual Studio along with a source control plug-in such as VisualSVN, but this is not covered here.

### Table of Contents ###
  * [About This Document](DevelopmentEnvironmentMain#About_This_Document.md)
  * [Prerequisites](DevelopmentEnvironmentMain#Prerequisites.md)
  * [Folder Structure](DevelopmentEnvironmentSourceCode#Folder_Structure.md)
  * [Getting the MediaPortal Source Code](DevelopmentEnvironmentSourceCode#Getting_the_MediaPortal_Source_Code.md)
  * [Getting the Moving Pictures Source Code](DevelopmentEnvironmentSourceCode#Getting_the_Moving_Pictures_Source_Code.md)
  * [Setting up your Visual Studio Solution](DevelopmentEnvironmentIDE#Setting_up_your_Visual_Studio_Solution.md)
  * [Testing Your Setup](DevelopmentEnvironmentIDE2#Testing_Your_Setup.md)
  * [Submitting Changes](DevelopmentEnvironmentIDE2#Submitting_Changes.md)
  * [Comments](DevelopmentEnvironmentIDE2#Comments.md)


---


# Prerequisites #
As mentioned above, you will at a minimum need two tools to work with the Moving Pictures source code, in addition to the the .NET Framework 2.0 SDK. Once you get going though you might want to consider grabbing a program to browse the Moving Pictures database. Any app that can read a SQLite3 database will do.

### .NET Framework 2.0 SDK ###
MediaPortal has a few unique assembly references that are not included with a standard Visual Studio Express 2008 installation. These assemblies are included in the .NET 2.0 SDK available from Microsoft, so before you get started you will need to install this SDK. Please note that the .NET 3.5 SDK does **not** include the required assemblies, you specifically need the 2.0 SDK. You can download the installer for this here:

http://www.microsoft.com/downloads/details.aspx?familyid=FE6F2099-B7B4-4F47-A244-C96D69C35DEC

### Visual Studio 2008 ###
All project files for Moving Pictures are in the Visual C# 2008 Project file format. Because Moving Pictures is currently targeted for .NET 2.0, it is possible to use earlier versions of Visual Studio. This is not covered by this guide, and if you choose to use an earlier version, _please do not overwrite the 2008 project files_.

If you do not already have it installed, you will need to install Visual C# before you proceed with the rest of this guide. Visual C# is a subset of Visual Studio, and it is the only portion of Visual Studio you will need. Throughout this document though, these terms will be used interchangeably. Don't get confused, all you need is Visual C#. A walk through for the Visual Studio installation is outside the scope of this guide, but you should not need anything beyond a standard install of the Visual Studio. The Express edition of Visual Studio 2008 is available from Microsoft, free of charge at the following URL, again, you will only need the Visual C# component:

http://www.microsoft.com/express/download/

### TortoiseSVN ###
We will be using TortoiseSVN for retrieving the latest source code and changes from the Subversion repositories for both MediaPortal and Moving Pictures. There are many other Subversion clients you could use, TortoiseSVN just happens to be our favorite. You will need TortoiseSVN installed before proceeding with this guide. You can get the latest version of TortoiseSVN from the following URL:

http://tortoisesvn.net/downloads

## [Next Page >>](DevelopmentEnvironmentSourceCode.md) ##