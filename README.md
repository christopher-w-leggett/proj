# Proj
Proj is a personal tool that helps manage multiple AEM projects.  Proj helps define a standard project directory structure and provides a way to easily setup, start, stop and profile AEM instances.

## Setup
Setup for Proj is very simply as it is simply a collection of bash scripts.  The steps below show all that is needed to setup Proj.

1. Clone this git repository to the location you would like the Proj tool to live.
2. Set the `PROJ_PROJECTS_HOME` environment variable to the location you would like to place the managed AEM projects. (ex. `/Users/<user>/Documents/projects`)
3. Set the `PROJ_HOME` environment variable to the location of the cloned git repository.
4. Add the `PROJ_HOME` enviornment variable to your `PATH`.
5. Run `proj help` to verify a successful setup.

## Commands
As mentioned earlier Proj is just a collection of bash scripts that are organized into separate commands.  These commands are listed below along with a short description of what each does.  For more detailed information about a specific command please run `proj help <command>`.

| Command                                                    | Description                                                       |
| ---------------------------------------------------------- | ----------------------------------------------------------------- |
| `proj dir [<project_name>]`                                | Displays a project's directory.                                   |
| `proj init <project_name>`                                 | Initializes a project's directory structure.                      |
| `proj list`                                                | Lists projects currently managed by proj.                         |
| `proj start <project_name> [(<aem_instance> [<port>])...]` | Starts a project using its start script.                          |
| `proj stop <project_name> [<aem_instance_name>...]`             | Stops a project using its stop script.                            |
| `proj setup-aem <project_name> [-j <aem_jar>]`             | Sets up one or more AEM instances.                                |
| `proj profile <project_name> [<aem_instance_name>]`             | Opens jvisualvm connected to the pid AEM is currently running on. |
