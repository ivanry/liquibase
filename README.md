# Liquibase

Liquibase helps millions of teams track, version, and deploy database schema changes.

This repository contains the main source code for Liquibase. 

For more information about the product, how the project is run, and how you can contribute, 
see [the main project website](https://www.liquibase.org/).

## Quickstart

[Get started in 5 minutes](https://www.liquibase.org/get_started/index.html).

## Changelog

[Learn about the latest improvements](https://github.com/liquibase/liquibase/blob/master/changelog.txt).

## Want to help?

Want to file a bug, contribute some code, or improve documentation? Excellent! Read up on our
guidelines for [contributing](https://www.liquibase.org/community/index.html)!

# How to create AS400 DB i export
Run liquibase.integration.commandline.Main with following parameters:
- --changeLogFile=export/changelog.xml
- --url=jdbc:as400://0.0.0.0:000?package=testdb
- --driver=com.ibm.as400.access.AS400JDBCDriver
- --classpath=path/to/as400-driver/jt400.jar
- --username=user
- --password=pass
- --schemas=TESTDB
- --defaultSchemaName=TESTDB
- --liquibaseSchemaName=TESTDB
- --defaultCatalogName=TESTDB
- --dataOutputDirectory=export
- --includeSchema=true
- --logLevel=debug generateChangeLog

Check export result in folder "export"