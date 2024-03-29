# GitUtils
This repo contains scripts and configs that may be useful with git work.

# Configs
All settings that are described in `global.gitconfig` file are applied to all your repositories. You can read about it [here](https://git-scm.com/docs/git-config).
Basically global .gitconfig is lacated here:`C:\Users\<user_name>`. 
To apply settings from `global.gitconfig` copy its content and paste to `C:\Users\<user_name>\.gitconfig`.

# Scripts
## Environment variable
To use scripts need to add scripts folder path to `Path` environment variable.

Run cmd as Asdministrator and paste the following string with specifying the real path to scripts folder: 
```bash
set PATH "%PATH%;<Path to scripts folder>
```
**Note**: Scripts use aliases from global `.gitconfig`. Need to update global `.gitconfig` to use them.

## Usage
To execute script go to parent folder with repositories and call git command with name of the script (without `git-` prefix):
```bash
git all <git-command>
```
# Developing
Scripts should always begin with
```bash
#!/bin/bash
```
Script file should be named with pattern `git-<git_command>` without extension, to be able to use it as simple git command: `git command`.
