# Git Configuration
## Identity
```
$ git config --global user.name "Abigail B. Carft"
$ git config --global user.email "abc@xyz.com"
```
## Editor
Configure the default text editor that will be used when Git needs you to type in a message. If not configured, Git uses the system's default editor.
```
$ git config --global core.editor vim
```
## Default Branch Name
Configure the branch name Git creates when you create a new repository with `git init`.
```
$ git config --global init.defaultBranch main
```
## Check Your Settings
- `git config --list` lists all the settings Git can find.
- `git config <key>` checks what Git thinks a specific key's value is. For example, `git config core.editor` checks the default editor.
