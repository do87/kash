# Kash

`kash` enables you to quickly get into a container running in a kubernetes pod

Current `kash` release relies on both [kubectl](https://kubernetes.io/docs/tasks/kubectl/install) and [fzf](https://github.com/junegunn/fzf)

If you wish to use the older version of `kash` without `fzf` dependency, please refer to [kash v1.0](https://github.com/do87/kash/tree/v1.0)

## Installation

### MacOS & Linux

Assuming `/usr/local/bin` is in your `PATH`, simply run:

    wget "https://raw.githubusercontent.com/do87/kash/v2.0/kash" \
      -O /usr/local/bin/kash && chmod +x /usr/local/bin/kash

## How does it work?

run `kash` to list all pods running in the namespace you're pointing to

Example:

    $ kash
    [pods prompt]

To filter, simply add part of the pod name, i.e.

    $ kash service-1
    Pod some-service-1 Found
    Choose a container:
    [containers prompt]

It's also possible to filter by pod and container name by running:

    $ kash service-1 api
    Pod some-service-1 Found
    Entering container service-1-api in pod some-service-1...
    / #
