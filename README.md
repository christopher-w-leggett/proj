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

| Command   | Description |
| --------- | ----------- |
| dir       | Displays a project's directory. |
| init      | Initializes a project's directory structure. |
| list      | Lists projects currently managed by proj. |
| start     | Starts a project using its start script. |
| stop      | Stops a project using its stop script. |
| setup-aem | Sets up one or more AEM instances. |
| profile   | Opens jvisualvm connected to the pid AEM is currently running on. |