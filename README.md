# Zerops x Adminer
The concept of a utility tool illustrates how to set up and use the technologies supported by [Zerops](https://zerops.io).

<br />

![adminer](https://github.com/zeropsio/recipe-shared-assets/blob/main/covers/cover-adminer.png)

## Deploy on Zerops
You can add latest version Adminer to your project by clicking the "Import Services" button in the project details and then copying the provided code.

```yaml
services:
  - hostname: adminer
    type: php-apache@8.3
    buildFromGit: https://github.com/zeropsio/recipe-adminer
```
See the [Zerops documentation](https://docs.zerops.io/references/import) and [zerops.yaml](https://github.com/zeropsio/recipe-adminer/blob/main/zerops.yml) to understand how to use it.



<br/>
<br/>

## ADMINER

[Adminer](https://www.adminer.org/en) is a full-featured database management tool written in PHP. Conversely to phpMyAdmin, it consist of a single file ready to deploy to the target server. Adminer is available for MySQL, MariaDB, PostgreSQL, SQLite, MS SQL, Oracle, Elasticsearch, MongoDB and others via plugin.


## Production vs. development

- For production environments, it is not advisable to make Adminer publicly accessible. Consider either disabling ```Public Access through the Zerops.io subdomain```  after deployment in GUI  or directly setting `enableSubdomainAccess` to `false` in import file.
- To access Adminer in production environment you can use a  [VPN](https://docs.zerops.io/references/vpn) through [ZCLI](https://docs.zerops.io/references/cli). Once connected, Adminer will be available at the address `adminer.zerops` (or whatever hostname you set).

<br/>
<br/>

Need help setting your project up? Join [Zerops Discord community](https://discord.com/invite/WDvCZ54).