# ZEROPS RECIPES

The concept of pre-prepared skeletons demonstrates the way how to set up and use technologies Zerops is supporting.

## ADMINER 4.8.1

[Adminer](https://www.adminer.org/en) is a full-featured database management tool written in PHP. Conversely to phpMyAdmin, it consist of a single file ready to deploy to the target server. Adminer is available for MySQL, MariaDB, PostgreSQL, SQLite, MS SQL, Oracle, Elasticsearch, MongoDB and others via plugin.

## Zerops import syntax

```yaml
services:
- hostname: adminer
  type: php-apache@8.0
  mode: NON_HA
  documentRoot: public
  buildFromGit: https://github.com/zeropsio/recipe-adminer
  enableSubdomainAccess: true
```

See the [Zerops documentation](https://docs.zerops.io/documentation/export-import/project-service-export-import.html) to understand how to use it.
