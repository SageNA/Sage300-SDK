# Sage 300 Web SDK

The Sage 300 Web SDK (SDK) includes productivity tools (wizards) for the generation of Web 
UIs in an MVC framework, documentation, samples and utilities.

The Sage 300 ISV and Business Partner community has applications, add-ons, and plug-ins to 
the Sage 300 application. These are very exciting and are the life blood to the community and 
were built with the Sage 300 SDK (non-web) in order to ensure compatibility with Sage 
frameworks and the Sage 300 application.

These applications will need to be re-written for Sage 300’s web screens. The SDK will provide 
assistance in getting screens developed quicker by creating a Visual Studio solution based 
upon the structures which Sage 300 uses internally. It will also generate code for a screen or 
report based upon a business view or a report or a dynamic query.

## Ecosystem Benefits

All tools can only be so much to everyone in order to consider everyone’s base needs while 
providing functionality that is easy to use. The open sourcing of the SDK will allow the 
community to extend, enhance and tailor this SDK to their specific needs.

Sage wants this community to be successful in the conversion of their applications to the web 
paradigm. The open sourcing of the SDK will allow those who wish to contribute to the SDK 
to do so in a way that not only addresses their needs, but potentially the needs of others as well. 
With this participation, Sage hopes to have a couple of outcomes:

* Engagement and Excitement
--* Get ISVs and Partners involved by allowing an ownership stake
--*	Generate excitement not only for themselves, but as an example for others to participate and 
contribute as well
--*	The community can make the SDK more robust
*	Faster Pace to Improve/Enhance/Extend the SDK
--*	Everyone benefits (Sage too!)
--*	The SDK potentially gets uncompleted sections and areas to be completed

## Folders and Contents

### docs

The **docs** folder contains the documentation for the SDK and contains the following sub-
folders in order to segregate the documentation:

* development
* patterns
* presentations
* standards
* upgrades
* utilities
* webapi
* wizards

### samples

The **samples** folder contains sample projects, which are stand-alone, runnable versions of 
different screens and reports within the Sage 300 application. These samples are to provide 
implementation knowledge.

### src

The **src** folder contains the source files which comprise the SDK and contains the following 
sub-folders in order to segregate the source:

* utilities
* wizards

### LICENSE.md

A read-only file for displaying the MIT Copyright notice

### README.md

A read-only version for displaying SDK information (this page!)

### VERSION.md

A read-only version for displaying the current version of the SDK

## Management

This section will discuss management and the collaboration model of the repository

### Administration

The administration of the repository is performed by Sage’s DevOps team located in Richmond BC.

### Anonymous Users

The repository is read-only for anonymous users which means that these users cannot “push” 
any changes into the repository.

### Collaborators

Collaborators are Sage assigned developers and personnel which have write/push access to 
the repository.

### Collaboration Model (Fork and Pull)
In the Fork and Pull Model, any GitHub member (anonymous user) can fork this public 
repository, which will create another repository where modifications can be applied 
to the forked repository without the changes affecting the original repository until 
a pull-request is submitted and evaluated by a collaborator who may or may not merge 
the changes.

See the article on [Forking](http://guides.github.com/activities/forking/).

## Forking and Branches

This section describes the branches for the repository and the fork procedures for an 
anonymous user.
 
### Fork

While a collaborator uses a forked repository for making changes to the public branches, an 
anonymous user can only submit changes to the public repository via a pull-request.
 
Therefore, an anonymous user will:

* Fork the public repository in GitHub
* Clone the fork down to their local machine
* Make changes locally
* Commit to the local repository
* Push everything up to the fork on GitHub
* Submit a pull-request, which is evaluated by Sage Collaborators for inclusion into the 
public repository. 

### Development Branch

The development branch, **develop**, is just what the name implies as it contains the 
in-progress contents of the SDK that is being worked on for the next release.

Sage collaborators are pushing changes and potentially merging anonymous user pull-requests 
for the next version of the SDK.
 
> **Only Sage collaborators can make changes to this branch**

This is the branch to be accessed based upon the question “Get me the in-progress 
version of the SDK that is not ready for release, but is to be released with the 
next version of the SDK”.

### Current Branch

The current branch, **master**, is the branch which holds the current release/version 
of the SDK.

This is the branch to be accessed based upon the question “Get me the current version 
of the SDK”.

> **Sage collaborators may push changes to this branch in response to defects or 
issues either discovered internally or externally. Any changes to this branch 
are also made in the develop branch**

> **Only Sage collaborators can make changes to this branch**

### Release Branches

The release branches (i.e. **release-2017**, **release-2017.1**, etc.) contains 
the contents for that particular release/version of the SDK.
 
When the next version of the SDK is released, the **master** branch is copied into, 
for example, the **release-2017** branch, the **develop** branch is copied to 
**master** and the **develop** branch then becomes the basis for the next release.

develop --> master --> release-…

There is only one in-progress version branch: **develop**

There is only one current version branch: **master**

There are to be numerous version branches: **release-2017**, **release-2017.1**, 
**release-2017.2**, etc.

> **Only Sage collaborators can make changes to these branches**

## Approval Timeline

The approval process for changes submitted by anonymous users are performed by Sage 
collaborators who review any changes for inclusion into the SDK based upon the value 
added to the SDK for the benefit of all users.
 
Therefore, it is extremely important to provide as much useful information and rational 
to support the request being added into the SDK. And, not all requests may be added to 
the SDK. But, the good news with open source software is that the submitter can still 
enjoy their version of the SDK which includes the modification being requested.

Depending upon the SDK roadmap, Sage collaborators are working throughout the development 
cycle on changes and enhancements in the roadmap and will want to potentially include 
any requests and issues that are discovered and presented by anonymous users.

Sage collaborators review any pull requests or issues submitted to the Repository 
on a bi-weekly basis. 

## Release Cycle

The SDK follows the release cycle established in the roadmap for the Sage 300 
Application. Therefore, new versions of the SDK are released when the Sage 300 
Application is released.

## Wizards

The following sections will cover topics such as building, installing, uninstalling 
and the debugging of the SDK.

### How to Build the Sage 300 UI Wizard Package

The following steps illustrate how to build the package:

* Load the **Sage300UIWizardPackage** solution
* Select **Build\Build Solution**
* The package will be successfully built to the output folder specified by the 
solution configuration (Debug or Release). The **Sage300UIWizardPackage.vsix** is 
the artifact that will be used to the install the package.

> **Building the package does not install the package**

### How to Install the Sage 300 UI Wizard Package

The following steps illustrate how to install the package:

* The package must first be built as demonstrated in the prior section
* Locate the **Sage300UIWizardPackage.vsix** file and run this file
* Select **Yes** to install the plug-in

> **If the package is already installed, it must be uninstalled first**

### How to Uninstall the Sage 300 UI Wizard Package

The following steps illustrate how to uninstall the package from Visual Studio:

* Load Visual Studio
* Select **Tools\Extensions and Updates…**
* Search for and select the **Sage 300 UI Wizard Package**
* Select the **Uninstall** button
* Select **Yes** to confirm uninstallation of the package
* Select **Yes** to re-start Visual Studio
* The package has been uninstalled

> **This step is only required if the package is installed**

### How to Run the Sage 300 UI Wizard Package in Debug Mode

The following steps illustrate how to run the package in debug mode from within Visual Studio:

* Load the **Sage300MenuExtension** solution
--*	This a solution which contains both wizard projects and other information to allow 
the Visual Studio plug-in to be debugged
* Right-Click on the **Sage300MenuExtension** project in order to display the 
properties page for this project
* Select the **Debug** Tab to display the properties for debugging
* In the **Start Action** section, select the **Start external program** option and enter 
the following information into the textbox: 
--*	C:\Program Files (x86)\Microsoft Visual Studio 12.0\Common7\IDE\devenv.exe

> Location and version of **devenv.exe** may be different than what is specified above 
based upon Version of Visual Studio and installation location

* In the **Start Options** section, enter the following information into the **Command line arguments** textbox:
--*	/rootsuffix Exp
* Run the solution to start debugging!

## License

See the LICENSE.md file