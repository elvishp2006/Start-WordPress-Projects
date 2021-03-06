# Start WordPress Projects

Automation for creating new projects in WordPress to localhost with apache and virtual hosts.

  > Very useful for developers, facility for creating new projects.

# Possibilities

  * Cloning a project at the time of installation.
  * Import an existing project in directory.
  * Import an existing database.
  * Replace urls at the time of installation.
  * Create a clean install of WordPress, with only the necessary files.
  * Multisite support.
  * WP Config already set.
  * htaccess already set.

### Version
2.0.1

### Installation
 Go to the project directory
```sh
$ cd Start-WordPress-Projects/
```
Create in current directory, the config.conf file and alter variables of configuration. To be not overwritten in any updates.
```sh
$ cp config-sample.conf config.conf
```

Create an alias to make life easier, add at the end of file the following command.
```sh
$ echo alias addsite=\"$(pwd)/addsite.sh \$1 \$2\" >> ~/.bashrc
```
```sh
$ echo alias delsite=\"$(pwd)/delsite.sh \$1 \$2\" >> ~/.bashrc
```
```sh
$ source ~/.bashrc
```

After all set settings. Add command in the terminal to add new project.

```sh
$ addsite your-project.dev database_name
```

To remove a project just type the following command in the terminal.

```sh
$ delsite your-project.dev database_name
```
