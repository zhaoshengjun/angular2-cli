# Angular2 CLI Quick Refence

Angular2 CLI quick reference, including hidden gems/unfinished implmentations etc.

## ng new

Create a new project using the name provided as the root folder unless `--directory` has been used.

###syntax

    ng new <project-name> [options]

### options
Options | Alias | Default |  Description  | Notes
--- | --- | --- | --- | --- |
`--dry-run` | `-d` | `false` |  only output the files created and operations performed, do not actually create the project. |
`--verbose` | `-v`|  `false` | Output more information. |
`--blueprint` | `-b` | `ng2` | select the blueprint to generate project file.  |  currently `ng2` looks like the only option available for project. 
`--skip-npm` | `-sn` | `false` |  do not run `npm` command after project files have been created. |
`--skip-bower` | `-sb` | `true`  | do not run `bower` command after project files have been created. |
`--skip-git` | `-sg` | `false`  | do not run `git` command after project files have been created. |
`--directory` | `-dir` |   | specify the parent directory. | 
`--source-dir` | `-sd` | `src`  | specify the folder name to store the actual source files. |
`--prefix` | `p` | `app`  | specify the prefix. | currently not working.
`--mobile` |  | false  | provide mobile template. | currently not working

## ng init

Create a new project in current folder unless `--directory` has been used.

###syntax

    ng init <project-name> [options]
    ng i <project-name> [options]

### options
Options | Alias | Default |  Description  | Notes
--- | --- | --- | --- | --- |
`--dry-run` | `-d` | `false` |  only output the files created and operations performed, do not actually create the project. |
`--verbose` | `-v`|  `false` | Output more information. |
`--blueprint` | `-b` | `ng2` | select the blueprint to generate project file.  |  currently `ng2` looks like the only option available for project. 
`--skip-npm` | `-sn` | `false` |  do not run `npm` command after project files have been created. |
`--skip-bower` | `-sb` | `true`  | do not run `bower` command after project files have been created. |
`--skip-git` | `-sg` | `false`  | do not run `git` command after project files have been created. | Though you will get an warning message, it still WORKS. 
`--source-dir` | `-sd` | `src`  | specify the folder name to store the actual source files. |
`--prefix` | `p` | `app`  | specify the prefix. | currently not working.
`--mobile` |  | false  | provide mobile template. | currently not working

## ng generate

Generate files based on tempaltes (AKA scaffolding)

###syntax

    ng generate <blueprint> [options]
    ng g <blurprint> [options]

### blueprint
Blurprint | Alias |   Description  | Result
--- | --- | --- | --- | --- |
`class` | `cl` |  Generate Class | `/NAME/NAME.ts`<br> `/NAME/NAME.spec.ts`
`component` | `c` |  Generate Component | `/NAME/index.ts`<br>`/NAME/shared/index.ts`<br>`/NAME/NAME.component.ts`<br>`/NAME/NAME.component.css`<br>`/NAME/NAME.component.html`<br>`/NAME/NAME.component.spec.ts`<br>
`directive` | `d` |  Generate Directive | `/NAME/index.ts`<br>`/NAME/NAME.directive.ts`<br>`/NAME/NAME.directive.spec.ts`
`pipe` | `p` |  Generate Pipe | `/NAME/index.ts`<br>`/NAME/NAME.pipe.ts`<br>`/NAME/NAME.pipe.spec.ts`
`route` | `r` |  Generate Route | `/+NAME/index.ts`<br>`/+NAME/shared/index.ts`<br>`/+NAME/NAME.component.ts`<br>`/+NAME/NAME.component.css`<br>`/+NAME/NAME.component.html`<br>`/+NAME/NAME.component.spec.ts`<br>
`service` | `cl` |  Generate Service | `/NAME/NAME.ts`<br>`/NAME/NAME.spec.ts`

### options
Options | Alias | Default |  Description  | Notes
--- | --- | --- | --- | --- |
`--dry-run` | `-d` | `false` |  only output the files created and operations performed, do not actually create the project. |
`--verbose` | `-v`|  `false` | Output more information. |
`--pod` | `-p` | `false` |   |   
`--classic` | `-c` | `false` |   |
`--dummy` | `-dum`, `-id` | `false`  |  |
`--in-repo-addon` | `--in-repo`, `-ir` |   |  | 

## ng serve

Builds and serves your app, rebuilding on file changes.

###syntax

    ng serve [options]
    ng s [options]
   
### options
Options | Alias | Default |  Description  | Notes
--- | --- | --- | --- | --- |
`--port` | `-p` | 4200 |  Define the port of the website. |
`--host` | `-H`|  `localhost` | Define the host name | 
`--proxy` | `-pr`, `-pxy` |  | Define the proxy  |   
`--insecure-proxy` | `--inspr` | `false` |  Set the proxy self-signed SSL certificates |
`--watcher` | `-w` | `events`  | Set watcher mode |
`--live-reload` | `-lr` | true  | Set if use live-reloading feature | 
`--live-reload-host` | `-lrh` | `localhost`  | Set live-reloading host | 
`--live-reload-base-url` | `-lrbu` |  baseURL | Set live-reloading base url | 
`--live-reload-port` | `-lrp` | 49152  | Set live-reloading port | 
`--environment` | `-e` | `development`  | Set environment variable | use `-dev` for development,`prod` for production 
`--output-path` | `-op`,`-out` | `dist`  | Set output folder path when in production mode | 
`--ssl` |  | `false`  | Set if use SSL | 
`--ssl-key` |  | `ssl/server.key`  | Set SSL key path | 
`--ssl-cert` |  | `ssl/server.crt`  | Set SSL certification path | 

## ng test

Runs your app's test suite.

###syntax

    ng test [options]
    ng t [options]
   
### options
Options | Alias | Default |  Description  | Notes
--- | --- | --- | --- | --- |
`--environment` | `-e` | test |  Set the environment variable. |
`--config-file` | `-c`, `-cf`|   | Specify the test configuration file | 
`--server` | `-s` | `false` |  Set the server | Not working yet  
`--host` | `-H` |  |  Set the host name |
`--test-port` | `-tp` | 7357 |  Set the port number when running with server |
`--module` | `-m` |  |  Specify the test module to run |
`--watcher` | `-w` | `events`  | Set watcher mode |
`--launch` |  | `false`  | Set the browsers to use for launching tests | 
`--reporter` | `-r` | `tap`  | Specify the test reporter to use | available values: tap, dot, xunit 
`--silent` |  | `false`  | Suppress any output except for the test report | 
`--test-page` |  |   | Set the test page to invoke | 
`--path` |  |   | Reuse an existing build at given path | 
`--query` |  |   | A query string to append to the test page URL | 

##ng lint

  Lints code in existing project

###Syntax

    ng lint

###Note

This will use `tslint.json` file as configration file to lint the code.

## ng build

Builds your app and places it into the output path (dist/ by default).

###syntax

    ng build [options]
    ng b [options]
   
### options
Options | Alias | Default |  Description  | Notes
--- | --- | --- | --- | --- |
`--environment` | `-e`, `-dev`, `-prod` | development |  Set the environment variable. |
`--ourput-path` | `-o`| `dist/`  | Specify the output folder | 
`--watch` | `-w` | `false`  | Use watching mode |
`--watcher` |  |   | Specify watcher name |
`--suppress-sizes` |  | `false`  | Suppress file sizes |

## ng github-pages:deploy

Build the test app for production, commit it into a git branch, setup GitHub repo and push to it.

###syntax

    ng github-pages:deploy [options]
    ng gh-pages:deploy [options]
   
### options
Options | Alias | Default |  Description  | Notes
--- | --- | --- | --- | --- |
`--message` |  | `new gh-pages version` |  The commit message to include with the build, must be wrapped in quotes. |
`--environment` | | `production`  | The Angular environment to create a build for | 
`--branch` |  | `gh-pages`  | The git branch to push your pages to |
`--skip-build` |  | `false`  | Skip building the project before deploying |
`--gh-token` |  |  | Github token |
`--gh-username` |  |  | Github user name |

##ng e2e

    Run e2e tests in existing project

###Syntax

    ng e2e

##ng doc

     Opens the official Angular documentation for a given keyword (on [angular.io](https://angular.io) webiste).

###Syntax

    ng doc <keyword>

##ng format

      Formats code in existing project

###Syntax

    ng format

##ng version

      Outputs angular-cli version

###Syntax

    ng version [options]
    ng v [options]
    ng -v [options]

### options
Options | Alias | Default |  Description  | Notes
--- | --- | --- | --- | --- |
`--verbose` |  | `false` |  Output detail information |    