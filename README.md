# Shopware 6 development template

This repository is a template for local development and enables you to create a running Shopware 6 instance.
Use this setup for developing directly on Shopware 6 or for developing plugins for Shopware 6.

The installation guide, together with the complete documentation, is available at [docs.shopware.com](https://docs.shopware.com/en/shopware-platform-dev-en/getting-started).


## Deploy your development environment on Okteto

First, download your Okteto credentials into your local machine:

```console
$ okteto login https://shopworks.okteto.dev/
$ okteto namespace
```

Second, deploy your development instance of Shopware:

```console
okteto stack deploy
```

## Develop with Okteto

Connect to your remote development environment with the command below. This will keep you code synchronized, and open a remote shell into the development container.

```
$ okteto up
```

If this is the first time you use your environment, run the commands below to initialize it from the remote shell. It'll take about 5 minutes, just enough to go grab some ☕.

```console
root@shopware-86b5c9979c-p9m8z:/app# ./psh.phar install
```

Run the following command from the remote shell to start shopware:

```console
root@shopware-86b5c9979c-p9m8z:/app# /opt/docker/bin/entrypoint.sh supervisord
```

## Debug from your local machine

1. Open the project in PHP Storm
1. Go to Preferences -> Languages and Frameworks -> PHP -> Debug and verify the following configuration settings:
    - `Debug port`: 9003
    - `Can Accept External Connections` is checked
1. Press on the "Start Listening for PHP Debug Connections" button.
1. Add a break point in the source code.
1. Enable [debugging in your browser](https://www.jetbrains.com/help/phpstorm/zero-configuration-debugging.html#activate-debugger-on-server).
1. Browse to the page.
