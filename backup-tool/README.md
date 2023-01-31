## Backup tool

### Idea

Sometimes there is an urgent need to make some experiment with a file or folder. Usually, consequences are overlooked and the damage is introduced to the given folder. It may be related to the fact that some changes in files or even files themselves are lost. So it'll be nice to have a simple tool to backup given folder and then immediately rub your hands to start experiments.

There are some features that it'll be cool to support with this tool:

- versioning of backups
- expanding provided path to build a key
- use the metadata file to keep information about kept backups
- support clean command (rm)
- restore the content

```bash
$ backup the .
$ backup list
$ backup show versions .
$ backup restore version=3 .
```

If there are several versions of backups, the `version` argument is required.

### Configuration

Environment variables:

- `BACKUP_TOOL_DIRECORY` - the directory to kept all backups

### Notes

- It's possible to add option to compress and archive backups
