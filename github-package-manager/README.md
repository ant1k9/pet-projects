## GitHub package manager

### Idea

To explore new tools it's often helpful to try them immediately, that's why it'll be helpful to provide only a link to a repository and get a binary automatically. To implement this idea it's possible to create setups for different languages and run several commands:

- git clone <repo>
- try to compile/prepare all binaries in this repo
- move this binary to a temporary directory
- if the tool is useful move it to the persistent directory

When we persist new binaries we need to remember the origin repo for them, so we need to keep metadata like this:

```yaml
---
https://github.com/awesome/repo:
    - run-me
    - do-something
    - ...
```

There are several commands that will be helpful for this utility:

```bash
$ gpackage install <repo> --language go
$ gpackage delete <repo>
$ gpackage list
```

### Configuration

Environment variables:

- `GPACKAGE_DIRECTORY` - the directory for persistent binaries and metadata

### Notes
