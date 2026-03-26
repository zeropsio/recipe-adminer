# Zerops x Adminer

![adminer](https://github.com/zeropsio/recipe-shared-assets/blob/main/covers/svg/cover-adminer.svg)

## Deploy on Zerops

You can either use the import button or the import file to add Adminer to your Zerops project.

### Using Import in GUI

Click **Import Services** in the project details and paste:

```yaml
services:
  - hostname: adminer
    type: php-apache@8.4
    enableSubdomainAccess: true
    buildFromGit: https://github.com/zeropsio/recipe-adminer
```

### Using Import File

The same configuration is available as [`zerops-import.yml`](https://github.com/zeropsio/recipe-adminer/blob/main/zerops-import.yml).

See the [Zerops documentation](https://docs.zerops.io/references/import) and [`zerops.yml`](https://github.com/zeropsio/recipe-adminer/blob/main/zerops.yml) to understand how it works.

## About Adminer

[Adminer](https://www.adminer.org/) (v5.4.2) is a full-featured database management tool written in PHP. It consists of a single file ready to deploy to the target server. Adminer supports MySQL, MariaDB, PostgreSQL, SQLite, MS SQL, Oracle, Elasticsearch, MongoDB and others via plugin.

## Production vs. Development

- For production environments, it is not advisable to make Adminer publicly accessible. Consider either disabling **Public Access through the Zerops.io subdomain** after deployment in GUI or directly setting `enableSubdomainAccess` to `false` in the import file.
- To access Adminer in production, use a [VPN](https://docs.zerops.io/references/vpn) through [zcli](https://docs.zerops.io/references/cli). Once connected, Adminer will be available at `http://adminer.zerops` (or whatever hostname you set).

---

Need help setting your project up? Join [Zerops Discord community](https://discord.com/invite/WDvCZ54).
