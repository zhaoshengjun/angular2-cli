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