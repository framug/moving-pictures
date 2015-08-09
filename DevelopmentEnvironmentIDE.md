# Setting up your Visual Studio Solution #
### Introduction ###
So now that you have the source code for Moving Pictures and MediaPortal, you need to setup a work environment by creating a Visual Studio Solution. There are currently two C# Projects that make up the Moving Pictures application and there are over a dozen that make up the MediaPortal application. We will be loading both Moving Pictures projects and a subset of the MediaPortal projects.

You might be wondering why a solution file for Moving Pictures is not committed to Subversion. If you work on any other MediaPortal plug-ins you could add them to the same Visual Studio Solution you are using here for Moving Pictures. For example it would make sense to have the MP-TVSeries project loaded in the same Solution as Moving Pictures if you occasionally do a few bug fixes for that project. This setup may not be the desired setup for everyone though, different people will be working on different projects, so only the project files for Moving Pictures are committed to Subversion, and everyone is free to setup their Solution file as they see fit.

### Creating the Solution ###
Creating your own solution is pretty easy. In Windows Explorer browse to the Moving Pictures folder that you recently pulled the source code into and go to the "MovingPictures" sub folder. You will see the MovingPictures project file (with the extension .csproj). Double click the file to launch it in Visual Studio 2008. In opening the project, Visual Studio will also create a Solution to host this project in. Not so hard right?

![http://moving-pictures.googlecode.com/svn/wiki/Images/project_loc.png](http://moving-pictures.googlecode.com/svn/wiki/Images/project_loc.png)

Now we need to save the solution to an appropriate folder. On the right side of the screen you will see the Solution Explorer and in this panel at the top you will see a node for the newly created solution. Click this node so that it's highlighted then click the save icon on the task bar. **Don't click OK on the save dialog yet though!** We want to change the location of the Solution. By default it will be placed in the same directory as the Moving Pictures project, but we will be using multiple projects in the solution. So go back up to the PluginDev directory you created earlier and save your solution here. You probably will want to change the name to something more generic as well (like PluginDev.sln).

![http://moving-pictures.googlecode.com/svn/wiki/Images/sol_explorer.png](http://moving-pictures.googlecode.com/svn/wiki/Images/sol_explorer.png) ![http://moving-pictures.googlecode.com/svn/wiki/Images/save_solution.png](http://moving-pictures.googlecode.com/svn/wiki/Images/save_solution.png)

### Adding Additional Projects ###
Now that you have created your solution you are almost done. All that is left is to add the remaining projects to the solution. Currently your solution only contains the primary MovingPictures project, but you will also need the MovingPicturesConfigTester project and the MediaPortal projects that Moving Pictures depends on. If you expand the "References" node of the existing MovingPictures project in the Solution Explorer you can see all the dependencies of the project. Some of these are .NET assemblies but a few are MediaPortal assemblies. You can satisfy these dependencies by adding the corresponding projects to the solution. At the time of this writing the only MediaPortal dependencies required by Moving Pictures are Core, Databases, and Utils. These in turn depend on DirectShowLib and MediaPortal.Support projects though so you will need to add all five.

![http://moving-pictures.googlecode.com/svn/wiki/Images/missing_assemblies.png](http://moving-pictures.googlecode.com/svn/wiki/Images/missing_assemblies.png) ![http://moving-pictures.googlecode.com/svn/wiki/Images/add_project.png](http://moving-pictures.googlecode.com/svn/wiki/Images/add_project.png)

So let's get these projects added. Right click the solution node in the Solution Explorer and click Add -> Existing Project. In the dialog you will need to navigate to one of the six project files listed below, select it and click OK. Then rinse and repeat, add each project in the list:

**NOTE: The tester project has been moved and there is one additional Moving Pictures project required for a working development environment. This document will be updated with details, but in the meantime, just make sure you add all projects under the Moving Pictures folder. You should have everything you need, it is just organized slightly differently.**

```
PluginDev\MovingPictures\Testing\MovingPicturesConfigTester\MovingPicturesConfigTester.csproj
PluginDev\MovingPictures\Cornerstone\Cornerstone.csproj
PluginDev\MovingPictures\Cornerstone.MP\Cornerstone.MP.csproj

PluginDev\MediaPortal\Core\Core.csproj
PluginDev\MediaPortal\Database\Database.csproj
PluginDev\MediaPortal\Dialogs\Dialogs.csproj
PluginDev\MediaPortal\DirectShowLib\DirectShowLib.csproj
PluginDev\MediaPortal\MediaPortal.Support\MediaPortal.Support.csproj
PluginDev\MediaPortal\RemotePlugins\RemotePlugins.csproj
PluginDev\MediaPortal\Utils\Utils.csproj
```

Once you have these projects added to your environment your References for the MovingPictures project should be free of warning icons, like the image below. If you see any warnings, this probably means additional dependencies have been added since the time of this writing. Don't panic, just browse through the MediaPortal folder structure and find the project Visual Studio is complaining about. You might also want to double check the references for the other MediaPortal projects. Again, at the time of this writing, the projects listed above are all that is required, but additional dependencies may have been added to any of these projects over the last few months.

![http://moving-pictures.googlecode.com/svn/wiki/Images/ok_assemblies.png](http://moving-pictures.googlecode.com/svn/wiki/Images/ok_assemblies.png)

# [Next Page >>](DevelopmentEnvironmentIDE2.md) #