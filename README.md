# ZEROPS RECIPES

The concept of pre-prepared skeletons demonstrates the way how to set up and use technologies Zerops is supporting.

## ADMINER 4.8.1

[Adminer](https://www.adminer.org/en) is a full-featured database management tool written in PHP. Conversely to phpMyAdmin, it consist of a single file ready to deploy to the target server. Adminer is available for MySQL, MariaDB, PostgreSQL, SQLite, MS SQL, Oracle, Elasticsearch, MongoDB and others via plugin.

## Zerops import syntax

```yaml
services:
# Service will be accessible through zcli VPN under: http://adminer
- hostname: adminer
  # Type and version of a used service.
  type: php-apache@8.0+2.4
  # Whether the service will be run on one or multiple containers.
  # Since this is a utility service, using only one container is fine.
  minContainers: 1
  maxContainers: 1
  # Repository that contains Adminer code with deploy instructions.
  buildFromGit: https://github.com/zeropsio/recipe-adminer@main
```

See the [Zerops documentation](https://docs.zerops.io/documentation/export-import/project-service-export-import.html) to understand how to use it.
