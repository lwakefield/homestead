# Lawrence's fork of Laravel Homestead

I like the way Laravel Homestead is setup, but it feels like it is just a
glorified wrapper for Vagrant. This fork removes the homestead commands, leaving
the Vagrant goodies.

This also adds adminer as a database manager. Make sure to update your
`/etc/hosts` file.

To add a new site edit `homestead.yaml`
```
folders:
  - map: ~/your/project/path/newsite
    to: /home/vagrant/newsite
...
sites:
  - map: newsite.dev
    to /home/vagrant/newsite 

```

Then update your `/etc/hosts` file
```
192.168.10.10 newsite.dev
```

Similary you can add databases by editting `homestead.yaml`
```
databases:
  - yournewdatabase
```
