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

| Command                                                                                                               | Description                                                       |
| --------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| <code>proj dir [&lt;project_name&gt;]</code>                                                                          | Displays a project's directory.                                   |
| <code>proj config get&#124;set [&lt;project_name&gt;] &lt;property&gt; [&lt;value&gt;]</code>                         | Gets or sets configurations at a user or project level.           |
| <code>proj init &lt;project_name&gt;</code>                                                                           | Initializes a project's directory structure.                      |
| <code>proj list</code>                                                                                                | Lists projects currently managed by proj.                         |
| <code>proj start &lt;project_name&gt; [((&lt;aem_instance_name&gt; [&lt;port&gt;]) &#124; &lt;alias&gt;)...]</code>   | Starts a project using its start script.                          |
| <code>proj stop &lt;project_name&gt; [(&lt;aem_instance_name&gt; &#124; &lt;alias&gt;)...]</code>                     | Stops a project using its stop script.                            |
| <code>proj setup-aem &lt;project_name&gt;</code>                                                                      | Sets up one or more AEM instances.                                |
| <code>proj setup-dispatcher &lt;project_name&gt;</code>                                                               | Configures Apache Dispatcher for one or more AEM instances.       |
| <code>proj profile &lt;project_name&gt; [&lt;aem_instance_name&gt;]</code>                                            | Opens jvisualvm connected to the pid AEM is currently running on. |
| <code>proj status</code>                                                                                              | Lists information about running AEM instances for each project.   |
| <code>proj alias list&#124;set&#124;delete &lt;project_name&gt; [&lt;alias&gt; [&lt;aem_instance_name&gt;...]]</code> | Manages aliases for starting/stopping multiple AEM instances.     |

## Configurations
The following configurations can be added using the `proj config set ...` command.

| Configuration                     | Description                                                                 |
| --------------------------------- | --------------------------------------------------------------------------- |
| aem.default.jar                   | The default AEM jar to use when setting up a new AEM instance.              |
| aem.default.instance.name         | The default AEM instance name.                                              |
| aem.default.instance.type         | The default AEM instance type.                                              |
| aem.default.production.ready.mode | The default value when prompted to install AEM in production ready mode.    |
| aem.default.author.port           | The default port when installing an author instance.                        |
| aem.default.author.debug.port     | The default debug port when installing an author instance.                  |
| aem.default.publish.port          | The default port when installing a publish instance.                        |
| aem.default.publish.debug.port    | The default debug port when installing a publish instance.                  |
| aem.default.dispatcher.module     | The default dispatcher module to use when setting up a dispatcher instance. |
