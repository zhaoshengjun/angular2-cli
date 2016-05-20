# Angular Cli

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

