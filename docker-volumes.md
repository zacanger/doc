# Docker Volumes

## Two Types of Volumes

* Data volume
* Container data volume

## Basics

### Union file system

Read-only based file system, every time you write to a new layer with the file,
it will have a new copy for the file and keep the old file in the previous
layer. So, never write keys into the container.

Because docker uses the union file system, when it needs a mutable state of
something. Volume comes to help.

## Data Volume

Two ways to initialize volumes.

1. `docker run -it --name <something> -v /data <image> <command>`, -v means volume
2. `VOLUME` in the docker file

In order to inspect the volumes, run `docker inspect -f {{.Volumes}} <name>`.

## Container Data Volume

### Simple Sample

1. Starts a volume container with the normal data volume.
2. Then start the application which needs a volume using `--volumes-from <target>`
  to starts the application.

```
┌───────────────────────────────────────────────────────────────┐
│┌────────────────┐                                             │
││  HOST MACHINE  │                                             │
│└────────────────┘                                             │
│┌────────────────────────────┐  ┌─────────────────────────────┐│
││        ┌──────────┐        │  │        ┌──────────┐         ││
││        │postgresql│        │  │        │ pg-data  │         ││
││        └──────────┘        │  │        └──────────┘         ││
││┌─────────────────────────┐ │  │ ┌─────────────────────────┐ ││
│││/var/lib/postgresql/data │◀┼──┼▶│/var/lib/postgresql/data │ ││
││└─────────────────────────┘ │  │ └─────────────────────────┘ ││
││                            │  │              ▲              ││
│└────────────────────────────┘  └──────────────┼──────────────┘│
│                               ┌───────────────┘               │
│                               ▼                               │
│            ┌──────────────────────────────────────┐           │
│            │    /var/lib/docker/vfs/dir/<sha>     │           │
│            └──────────────────────────────────────┘           │
└───────────────────────────────────────────────────────────────┘
```

### About permissions

Anything after the VOLUME instructions in a Dockerfile will not able to make
changes to the volume.

```Dockerfile
FROM debian:wheezy
RUN useradd foo
VOLUME /data
RUN touch /data/x
RUN chown -R foo:foo /data
```

The code above will not work. Instead, it need to be look like:

```Dockerfile
FROM debian:wheezy
RUN useradd foo
RUN mkdir /data; touch /data/x; chown -R foo:foo /data
VOLUME /data
```

## Garbage Collecting Volumes

The volume will only get deleted when running `docker rm -v`, so the `-v` is
always required. The other way is running the docker container with `-rm`.

But, if some other container is linking to the volume, even if we runs the `rm`
with `-v` flag, it will also not able to delete the volume.

When running out of space with a lot of zombie volumes, we can use
[Docker Volume Manager](https://github.com/cpuguy83/docker-volumes) to clean up.

