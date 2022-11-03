Config for a fly app that runs a [mysql server docker
container](https://hub.docker.com/_/mysql) that is accessible
publicly.

Use the [MySQL fly.io
guide](https://fly.io/docs/app-guides/mysql-on-fly/) but edit the
fly.toml to look like [this](./fly.toml)

Before deploying do the following
```bash
# Create a volume within the fly app
fly volumes create mysqldata --size 1 # gb

# Set MYSQL_ROOT_PASSWORD. It's required.
fly secrets set MYSQL_ROOT_PASSWORD=password
```
