# Self Development Help
For quick development I have collect some dev solutions

# SHELL
Which shell you are using check `echo $SHELL`

# PG command for mac
![pg-command](https://user-images.githubusercontent.com/18096618/169646141-00b5c7b4-6b4b-497a-be20-fa4a33f82e24.jpg)

### Problem
This sometimes happens when brew does a postgres upgrade, causing the data files to become incompatible with the new server.
In my case, it happened when upgrading from 13 to 14.3.

**OS X/Homebrew:**

Try running `postgres -D /usr/local/var/postgres`, it will give you a much more verbose output if postgres fails to start. [Link here](https://stackoverflow.com/questions/13410686/postgres-could-not-connect-to-server)

If you recently upgraded postgres to latest version, you can run the below command to upgrade your postgres data directory retaining all data: `brew postgresql-upgrade-database`. [Link here](https://stackoverflow.com/questions/17822974/postgres-fatal-database-files-are-incompatible-with-server)

| Command | Description |
| ------ | ------ |
| `brew info postgres` | Status check |
| `psql --version` | Version check |
| `brew postgresql-upgrade-database` | To migrate existing data from a previous major version of PostgreSQL |
| `gem uninstall pg` | Uninstall pg |
| `brew uninstall postgres` | Uninstall brew postgres |
| `rm -rf /usr/local/var/postgres` | Nuke the postgres folder which might be lingering with a bunch of stale stuff it in |
| `brew install postgres` | Reinstall pg |
| `gem install pg` | Reinstall gem |
| `psql -U username` | PG login by terminal |
| `\l` or `\list` | To view all of the defined databases on the server you can use. [Link here](https://chartio.com/resources/tutorials/how-to-list-databases-and-tables-in-postgresql-using-psql/) |
| `DROP DATABASE db-name;` | After login console you can delete database|
| `pg_dump name_of_database > name_of_backup_file.bak` | Backup your database [Link here](https://stackoverflow.com/questions/43018658/how-to-delete-postgresql-database-on-linux)|
| `psql empty_database < backup_file.bak` | To restore database [Link here](https://stackoverflow.com/questions/43018658/how-to-delete-postgresql-database-on-linux)|

### Ruby on Rails - [Help](https://github.com/plabon-asad/study-with-ror)
