# Show a bug in wercker's cli

## In the CLI

```bash
$ wercker --verbose --environment docker.env build
$ wercker --verbose --environment docker.env deploy --deploy-target push
$ docker run -it sttts/wercker-deploy-bug
_temp                   linuxrc                 sys
bin                     media                   this-is-the-source-dir
dev                     mnt                     tmp
docker.env              proc                    usr
etc                     root                    var
home                    run                     wercker.yml
lib                     sbin
```

Note that there is the `this-is-the-source-dir` file. This was **not** copied into the output directory.
