# Home Assistant Add-on: MariaDB

```
vvvvvvvv WARNING vvvvvvvv
```
> This is a fork of the official add-on!
>
> This version uses tmpfs to store MariaDB database in-memory. The Memory storage engine is not suitable, because that [can't handle TEXT columns](https://mariadb.com/kb/en/memory-storage-engine/) in the recorder [database](https://www.home-assistant.io/docs/backend/database/#schema).
>
> The size of the tmpfs is hardcoded in the HA/Docker configuration file, can't be set from the add-on's configuration. Currently it is **200MB**.
>
> If you use the built-in SQLite with ```db_url: 'sqlite:///:memory:'``` recorder configuration and fed up with the uncountable ```sqlite3.OperationalError: cannot commit - no transaction is active``` errors in your HA log, give this add-on a try.

```
^^^^^^^^ WARNING ^^^^^^^^
```

MariaDB database for Home Assistant.

![Supports aarch64 Architecture][aarch64-shield] ![Supports amd64 Architecture][amd64-shield] ![Supports armhf Architecture][armhf-shield] ![Supports armv7 Architecture][armv7-shield] ![Supports i386 Architecture][i386-shield]

## About

You can use this add-on to install MariaDB, which is an open-source (GPLv2 licensed) database.  MariaDB can be used as the database backend for Home Assistant. For more information, please see [MariaDB][mariadb]

[aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[armhf-shield]: https://img.shields.io/badge/armhf-yes-green.svg
[armv7-shield]: https://img.shields.io/badge/armv7-yes-green.svg
[mariadb]: https://mariadb.com
[i386-shield]: https://img.shields.io/badge/i386-yes-green.svg
