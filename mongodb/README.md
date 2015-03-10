# MongoDB plugin for Dokku

## Installation

```
git clone https://github.com/partlab/dokku-plugins ~/partlab-dokku-plugins
cp -r ~/partlab-dokku-plugins/mongodb /var/lib/dokku/plugins/mongodb
cd /var/lib/dokku/plugins
dokku plugins-install
```

## Commands

```
$ dokku help
     mongodb:create <app>            Create a MongoDB container
     mongodb:delete <app>            Delete specified MongoDB container
     mongodb:info <app>              Display container informations
     mongodb:link <app> <container>  Link an app to a MongoDB container
     mongodb:logs <app>              Display last logs from MongoDB container
```

## Simple usage

Create a new Container:

```
$ dokku mongodb:create foo            # Server side
$ ssh dokku@server mongodb:create foo # Client side

-----> mongodb container created: mongodb_foo

       Docker image:   mongodb/foo
       Container name: mongodb_foo
       Database:       foo
```

## Advanced usage

### Deleting containers:

```
dokku mongodb:delete foo
```

### Linking an app to a specific container:

```
dokku mongodb:link foo bar
```

### MongoDB logs (per container):

```
dokku mongodb:logs foo
```

### MongoDB information:

```
dokku mongodb:info foo
```
