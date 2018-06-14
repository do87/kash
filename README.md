# Kash

## What is Kash?

Kash helps you to easly sh into a container running inside a kubernetes pod

## Installation

### MacOS & Linux

Assuming `/usr/local/bin` is in your `PATH`, simply run:

    wget "https://raw.githubusercontent.com/do87/kash/master/kash" -O /usr/local/bin/kash && chmod +x /usr/local/bin/kash

## How does it work?

run `kash` to list all pods running in the namespace you're pointing to

Example:

    $ kash
    some-service-1
    some-service-2
    app-worker-0
    app-worker-1

To filter, simply add part of the pod name, i.e.

    $ kash service-1
    Pod some-service-1 Found, Checking containers
    Please specify a container from:
    service-1-nginx
    service-1-api

Because `service 1` has more than 1 container, we need to specify the container name (can be a wild card too)

    $ kash service-1 api
    Pod some-service-1 Found
    Entering container service-1-api in pod some-service-1...
    / #
