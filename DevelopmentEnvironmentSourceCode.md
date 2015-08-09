# Folder Structure #
So now that you have your tools setup, you will want to pull down the latest source code for Moving Pictures. Before you do that though, you will have to decide where you want your projects to be stored. You can setup your project and solution files anywhere, but the default location for Visual Studio Projects is "`My Documents\Visual Studio 2008\Projects`". Any location will do if you would rather not work from there. To give you a little visibility, this is the folder structure I am recommending:

![http://moving-pictures.googlecode.com/svn/wiki/Images/folders.png](http://moving-pictures.googlecode.com/svn/wiki/Images/folders.png)

So go ahead and create your folder structure. Create the `PluginDev` folder and the `MediaPortal` and `Moving Pictures` folders below that. These three are all you need to do manually, everything else will automatically be pulled down by TortoiseSVN.

# Getting the MediaPortal Source Code #
### Checking Out ###
Now that you have your folders created, we need to pull down the latest code for the Moving Pictures and MediaPortal projects. MediaPortal is a dependency of Moving Pictures, so let's start with that. Right click the MediaPortal folder you created previously and click "SVN Checkout". If you do not see this you most likely either do not have TortoiseSVN installed or it is not setup properly.

![http://moving-pictures.googlecode.com/svn/wiki/Images/checkout_popup.png](http://moving-pictures.googlecode.com/svn/wiki/Images/checkout_popup.png) ![http://moving-pictures.googlecode.com/svn/wiki/Images/checkout.png](http://moving-pictures.googlecode.com/svn/wiki/Images/checkout.png)

### Picking Your Repository ###

The only thing you need to change on this popup is the "URL of Repository" field. You have a choice though, you can go with the latest, greatest source code from the MediaPortal project (sometimes called the SVN version), or you can go with the source code from the most recent release. If you want the latest, greatest (and possibly buggy) MediaPortal code, cut and paste the first URL listed below into the "URL of Repository" field, then click OK.

Using the very latest code base from MediaPortal, may not be the best idea though. Most of the users of Moving Pictures are going to be running the plug-in against the _latest release_ of MediaPortal, not the SVN version, so it may be a better idea to go with the code from the latest release. If this is the route you want to go (I recommend this) then cut and paste the second URL below into the "URL of Repository" field. **Don't hit OK yet though!** Click the "..." button to pop up the repository browser, **right click and refresh the "tags" node** and pick the most recent version. At the time of writing, the latest version is 1.0.1, but there may be a newer release by now. Pick the newest.

```
https://sources.team-mediaportal.com/svn/public/trunk
```

![http://moving-pictures.googlecode.com/svn/wiki/Images/tags.png](http://moving-pictures.googlecode.com/svn/wiki/Images/tags.png)

Once you have picked the latest version of the MediaPortal code, click OK. Back on the Checkout Dialog the "URL of Repository" field will automatically be updated with your selection, so now click OK to start the checkout. MediaPortal is a bit large so this may take a few minutes depending on your connection speed.

# Getting the Moving Pictures Source Code #

Alright so now that you have retrieved the source code for MediaPortal, you will need to get the source code for Moving Pictures. The Moving Pictures source code is also hosted in a subversion repository so the procedure is virtually identical. In fact it's even a bit easier because, as of the time of this writing, there have been no Moving Pictures releases (that's what we are trying to change)! This means that you don't have to pick which code base to work from. So just right click the Moving Picture folder you created previously, and click "SVN Checkout. The "URL of Repository" field should be populated with the following URL:

```
http://moving-pictures.googlecode.com/svn/trunk/
```

![http://moving-pictures.googlecode.com/svn/wiki/Images/checkout_popup.png](http://moving-pictures.googlecode.com/svn/wiki/Images/checkout_popup.png) ![http://moving-pictures.googlecode.com/svn/wiki/Images/checkout.png](http://moving-pictures.googlecode.com/svn/wiki/Images/checkout.png)

Click OK and wait for the checkout to complete. This should be significantly faster than the MediaPortal checkout.

## [Next Page >>](DevelopmentEnvironmentIDE.md) ##