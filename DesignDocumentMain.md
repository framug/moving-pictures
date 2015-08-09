# Introduction #
This document contains detailed descriptions of the different components of Moving Pictures. The descriptions, while making reference to specific classes, should be done at a functional level, rather than a technical level. This document should explain _how Moving Pictures works_. It should not describe the code itself, that is what code comments are for.


# [Core Services](DesignDocumentCoreServices.md) #
This section explains the details of the core sub-systems of Moving Pictures. These components are actually all generalized and could be reused by other plug-ins. The purpose of these components is to provide generic services to the rest of the plug-in. In the future these components will most likely be abstracted to a separate package so other people can base plug-ins on this framework. _No direct link to any MediaPortal code should exist in these components._

# [Data Providers](DesignDocumentDataProviders.md) #
The data provider subsystem is one of the integral parts of Moving Pictures. These components retrieve meta-data and artwork from online to provide movie details for the user. They should not handle any local parsing information and they should be total agnostic in regards to what they are providing movie information for. The output of this subsystem is populated Movie (DBMovieInfo) objects.

# [Movie Importer](DesignDocumentMovieImporter.md) #
These components handle the process of turning a list of files into useful information in the database. These components read directly from the disk, they use the Data Provider components as a service and the output is a database full of meta-data relating to files on disk. If there is a heart to the plug-in, this is it. This is the component the creates all the magic.

# Configuration Screen #
This section covers the design of the Configuration screen and it's various components. This user interface layer sits on top of all above components to provide interaction with the user. There should be very little if any core logic in these classes, the only provide the _presentation_ of the underlying components.

# Media Portal UI #
This section of course covers the presentation layer in the MediaPortal application itself. This covers how things are displayed, and what components are available to the skinner. This combined with the [Skin Designer's Guide](SkinDesignersGuide.md) should give someone an intimate understanding of how the GUI functions and how it interacts with the skin layer.