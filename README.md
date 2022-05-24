# dev-help
For quick development I have collect some dev solutions

# PG command for mac
![pg-command](https://user-images.githubusercontent.com/18096618/169646141-00b5c7b4-6b4b-497a-be20-fa4a33f82e24.jpg)

If you installed using HomeBrew:, to check status `brew info postgres`

To migrate existing data from a previous major version of PostgreSQL run: `brew postgresql-upgrade-database`
  
# Install/ Uninstall
Uninstall pg: `gem uninstall pg`

Uninstall postgres: `brew uninstall postgres`


Nuke the postgres folder which might be lingering with a bunch of stale stuff it in: `rm -rf /usr/local/var/postgres`

Reboot (maybe unnecessary)

Reinstall pg: `brew install postgres`


I use brew services which has simplified my life in so many ways: `brew install services`


And start pg with it: `brew services start postgresql`


Reinstall the gem: `gem install pg`

