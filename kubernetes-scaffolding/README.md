## Kubernetes scaffolding

### Idea

Sometimes, it's useful to generate a kubernetes object to launch it in the cluster with minimal setup. It requires some googling every time, because we have different specs and versions for each entity. It'll be much easier to have an utility that will generate templates for manifests to configure only needed fields.

The command will be looking like this:

```bash
$ sk8fold pod --image ubuntu:latest > pod.yaml
$ sk8fold deployment --num-containers=2 > deployment.yaml
$ sk8fold service --type NodePort > service.yaml
```

### Configuration

Environment variables:

- `SK8FOLD_DIRECTORY` - the directory where all templates will be placed

### Notes
