# Redis plugin for Dokku

## Installation

```
git clone https://github.com/partlab/dokku-plugins ~/partlab-dokku-plugins
cp -r ~/partlab-dokku-plugins/redis /var/lib/dokku/plugins/redis
cd /var/lib/dokku/plugins
dokku plugins-install
```

## Commands

```
$ dokku help
     redis:create <app>              Create a Redis container
     redis:delete <app>              Delete specified Redis container
     redis:info <app>                Display container informations
     redis:link <app> <container>    Link an app to a Redis container
     redis:logs <app>                Display last logs from Redis container
```

## Simple usage

Create a new Container:

```
$ dokku redis:create foo            # Server side
$ ssh dokku@server redis:create foo # Client side

-----> redis container created: redis_foo

       Docker image:   redis/foo
       Container name: redis_foo
```

## Advanced usage

### Deleting containers:

```
dokku redis:delete foo
```

### Linking an app to a specific container:

```
dokku redis:link foo bar
```

### Redis logs (per container):

```
dokku redis:logs foo
```

### Redis information:

```
dokku redis:info foo
```
