!!! note "TODO - VS Code? other OSes?"

## In Visual Studio on Windows

If you are looking at creating a .Net Core Web App in Visual Studio, please follow the steps below:

1.  Create a new Solution.

2.  Select the ASP.Net Core Web Application option. Press next. Make sure you have selected the latest version of .Net Core (currently 2.0 as of 23/02/2018)

3.  Select empty - this makes it easier for us to add the standard bits that we need without worrying about introducing unused files.

## Front-end

Note that this is only applicable if you have a UI!
It is also worth noting that by default, if you did not create an empty project, that VS will use Bower to manage your front end packages. This is no longer recommended as Bower has been deprecated.

!!! note "TODO: the install node step isn't needed every time - it should be in environment setup"

1.  Install node on system : either go to https://nodejs.org/en/download/ to install it directly, or if you want to use a command line package manager go to https://chocolatey.org/

2.  By default, VS comes with its own version of node installed, but this is outdated. To use the version you installed on your system, select tools -> options -> projects and solutions
    -> web package management -> external web tools and add the location of node (default is `C:\Program Files\nodejs`). Make sure this is at the top of the list.
    This only needs to be done once per system install, not project.

3.  Add the contents of the `frontend` folder of our [boilerplate repo](https://github.com/UniversityOfNottingham/dotnet-boilerplate).

* package.json
* gulpfile.js
* Add a new folder to the project called "js" and add main.js from the boilerplate
* Add a new folder called "sass" add style.scss from boilerplate

4.  Other classes then need to go into their own folders (Controllers, Services, ViewModels, Entities etc).

Some current examples of projects which follow our currently defined pattern are:

* OwnVehicles
* DECSYS.Survey
* SPMIC (revamp branch only)
