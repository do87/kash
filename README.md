# Kash

Kash enables you to quickly get into a container running in a kubernetes pod

## Installation

### MacOS & Linux

Assuming `/usr/local/bin` is in your `PATH`, simply run:

    wget "https://raw.githubusercontent.com/do87/kash/master/kash" \
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
