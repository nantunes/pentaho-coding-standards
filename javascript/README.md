# Javascript Pentaho Coding Standards

Pentaho enforces Javascript coding standards and style through both the [JSHint](http://jshint.com) and [JSCS](http://jscs.info) tools.

You can configure your IDE using the instructions below to to ensure your contributions conform to the standard.

## JSHint

JSHint is a tool that helps to detect errors and potential problems in your JavaScript code.

It uses a special .jshintrc file for its configuration. JSHint will start looking for this file in the same directory as the file that's being linted. If not found, it will move one level up the directory tree all the way up to the filesystem root.

This enables to use the Pentaho config globally, per project or even scoped (having the intended projects under the same folder, e.g. ~/dev/pentaho).

### Installation

1. Install [JSHint](http://jshint.com/install/):
2. Clone this repository;
2. Create a .jshintrc where you need it (folder, project, home, etc.);
3. Use "extends" property to refer pentaho.jshintrc file:

```json
{
    "extends": "/%CLONED-REPO-LOCATION%/javascript/pentaho.jshintrc"
}
```

#### IntelliJ IDEA:

1. IntelliJ IDEA supports realtime code inspection with JSHint [out of the box](https://www.jetbrains.com/webstorm/help/jshint.html).

#### Sublime Text 3:

1. If not already install, add [Package Manager](https://packagecontrol.io/installation) plugin;
2. Use Package Manager to install [JSHint Gutter](https://github.com/victorporof/Sublime-JSHint).

#### Eclipse:

1. Follow the instructions of [jshint-eclipse](http://github.eclipsesource.com/jshint-eclipse/install.html); 
2. The plugin bundles an old version of JSHint, so it's recommended to configure it to use the current version.
3. It also only supports the .jshintrc file located at the root of the eclipse project.

#### Additional Information

1. [JSHint Mojo](https://github.com/cjdev/jshint-mojo) is a maven plugin.

## JSCS

JSCS is a code style linter for programmatically enforcing a Javascript style guide.

It uses a special .jscsrc file for its configuration. JSCS will start looking for this file in the same directory as the file that's being linted. If not found, it will move one level up the directory tree all the way up to the filesystem root.

This enables to use the Pentaho config globally, per project or even scoped (having the intended projects under the same folder, e.g. ~/dev/pentaho).

### Installation

1. Install [JSCS](http://jscs.info/overview#installation):
2. Install [jscs-preset-pentaho](https://www.npmjs.com/package/jscs-preset-pentaho);
3. Create a .jscsrc where you need it (folder, project, home, etc.);
4. Set "preset" property to "pentaho":

```json
{
    "preset": "pentaho"
}
```

**Note:** Currently jscs-preset-pentaho needs to be installed locally in the project, with ```npm install jscs-preset-pentaho```. There is a PR (https://github.com/jscs-dev/node-jscs/pull/1807) to allow global node modules (so it can be installed only once with ```npm install -g jscs-preset-pentaho```).

#### IntelliJ IDEA:

1. IntelliJ IDEA supports realtime code inspection with JSCS [out of the box](https://www.jetbrains.com/webstorm/help/jscs.html).

#### Sublime Text 3:

1. If not already install, add [Package Manager](https://packagecontrol.io/installation) plugin;
2. Use Package Manager to install [SublimeLinter](http://sublimelinter.readthedocs.org/en/latest/installation.html);
3. Use Package Manager to install [SublimeLinter-jscs](https://github.com/SublimeLinter/SublimeLinter-jscs/).

#### Eclipse:

Currently there is no reliable Eclipse plugin for JSCS.
