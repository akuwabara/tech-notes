# Clean Up Unused Docker Resources

Docker provides `prune` commands for removing unused resources.

## Containers

Use the following command to remove stopped containers.

```bash
$ docker container prune
```

## Images

Use the following command to remove dangling images.

```bash
$ docker image prune
```

## Networks

Use the following command to remove unused networks.

```bash
$ docker network prune
```

## All Unused Resources without Volumes

Use the following command to remove unused containers, networks, and images.

```bash
$ docker system prune
```

By default, volumes are not removed.

If unused volumes should also be removed, use the following command:

```bash
$ docker system prune --volumes
```