# MariaDB plugin for Dokku

## Installation

```
git clone https://github.com/partlab/dokku-plugins ~/partlab-dokku-plugins
cp -r ~/partlab-dokku-plugins/mariadb /var/lib/dokku/plugins/mariadb
cd /var/lib/dokku/plugins
dokku plugins-install
```

## Commands

```
$ dokku help
     mariadb:create <app>            Create a MariaDB container
     mariadb:delete <app>            Delete specified MariaDB container
     mariadb:info <app>              Display container informations
     mariadb:link <app> <container>  Link an app to a MariaDB container
     mariadb:logs <app>              Display last logs from MariaDB container
```

## Simple usage

Create a new Container:

```
$ dokku mariadb:create foo            # Server side
$ ssh dokku@server mariadb:create foo # Client side

-----> mariadb container created: mariadb/foo

       Host: aaa.bbb.ccc.ddd
       Username: root
       Private ports: 3306
```

## Advanced usage

### Deleting containers:

```
dokku mariadb:delete foo
```

### Linking an app to a specific container:

```
dokku mariadb:link foo bar
```

### MariaDB logs (per container):

```
dokku mariadb:logs foo
```

### MariaDB information:

```
dokku mariadb:info foo
```
