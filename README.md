# Shopware 6 development template

This repository is a template for local development and enables you to create a running Shopware 6 instance.
Use this setup for developing directly on Shopware 6 or for developing plugins for Shopware 6.

The installation guide, together with the complete documentation, is available at [docs.shopware.com](https://docs.shopware.com/en/shopware-platform-dev-en/getting-started).


## Deploy your development environment on Okteto Cloud

First, download your Okteto Cloud credentials into your local machine:

```console
$ okteto login
$ okteto namespace
```

Second, deploy your dev copy of Shopware:

```console
okteto stack deploy
```

## Develop with Okteto

Connect to your remote development environment with the command below. This will keep you code synchronized, and open a remote shell into the development container.

```
$ okteto up
```

If this is the first time you use your environment, run the command below to initialize it:

```
bin/console setup
```


