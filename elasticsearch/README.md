# Elasticsearch plugin for Dokku

## Installation

```
git clone https://github.com/partlab/dokku-plugins ~/partlab-dokku-plugins
cp -r ~/partlab-dokku-plugins/elasticsearch /var/lib/dokku/plugins/elasticsearch
cd /var/lib/dokku/plugins
dokku plugins-install
```

## Commands

```
$ dokku help
     elasticsearch:create <app>            Create a Elasticsearch container
     elasticsearch:delete <app>            Delete specified Elasticsearch container
     elasticsearch:info <app>              Display container informations
     elasticsearch:link <app> <container>  Link an app to a Elasticsearch container
     elasticsearch:logs <app>              Display last logs from Elasticsearch container
```

## Simple usage

Create a new Container:

```
$ dokku elasticsearch:create foo            # Server side
$ ssh dokku@server elasticsearch:create foo # Client side

-----> Elasticsearch container created: elasticsearch_foo

       Docker image:   elasticsearch/foo
       Container name: elasticsearch_foo
```

## Advanced usage

### Deleting containers:

```
dokku elasticsearch:delete foo
```

### Linking an app to a specific container:

```
dokku elasticsearch:link foo bar
```

### Elasticsearch logs (per container):

```
dokku elasticsearch:logs foo
```

### Elasticsearch information:

```
dokku elasticsearch:info foo
```
