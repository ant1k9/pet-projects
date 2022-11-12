## Alias manager

### Idea

To ease the creation for new CLI tools it makes sense to create a tool which will manage code snippets. To add a new command you just need to create a snippet and you've get autocomplete from the box.

The possible implementation is a tool that creates simple shell scripts that would have autocomplete later in the fish shell.

```bash
$ aliasme add builder run go
$ aliasme rm builder run # works recursively
$ aliasme edit builder run go
```

Running the add commands the CLI will open the VIM editor with the template like this:

```bash
#!/usr/bin/env bash
# Description: the command description (optional)

echo TODO
```

A newly created command will be like this:

```bash
#!/usr/bin/env bash
aliasme run <command-name> $*
```

To work with options and flags there will be a command to configure options for any existing command:


```bash
$ aliasme options builder run go
```

### Configuration

Environment variables:

- `ALIASME_DIRECTORY` - the directory where all snippets live

### Notes

- Add synchronization through the dotfiles repository
