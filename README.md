# Self Development Help
For quick development I have collect some dev solutions

# SHELL
Which shell you are using check `echo $SHELL`

# Git & Github

✏️ How to Push an Existing Project to GitHub?

- `git init`
- `git add .`
- `git commit -m 'Added my project'`
- `git remote add origin git@github.com:github_user-name/project-repo-name.git`
- `git push -u origin master`
- `git push -u -f origin master // for forcely push`

[Link here](https://www.digitalocean.com/community/tutorials/how-to-push-an-existing-project-to-github)

# PG command for mac
![pg-command](https://user-images.githubusercontent.com/18096618/169646141-00b5c7b4-6b4b-497a-be20-fa4a33f82e24.jpg)
Create a local server by PG-Admin - [See here](https://stackoverflow.com/questions/53267642/create-new-local-server-in-pgadmin)

### Problem
This sometimes happens when brew does a postgres upgrade, causing the data files to become incompatible with the new server.
In my case, it happened when upgrading from 13 to 14.3.

**OS X/Homebrew:**

Try running `postgres -D /usr/local/var/postgres`, it will give you a much more verbose output if postgres fails to start. [Link here](https://stackoverflow.com/questions/13410686/postgres-could-not-connect-to-server)

If you recently upgraded postgres to latest version, you can run the below command to upgrade your postgres data directory retaining all data: `brew postgresql-upgrade-database`. [Link here](https://stackoverflow.com/questions/17822974/postgres-fatal-database-files-are-incompatible-with-server)

| Command | Description |
| ------ | ------ |
| `brew services list` | All install status to see from Homebrew |
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

# Deployment - Vue/heroku
How to deploy a vue-static project deploy in heroku in production mode, `full config, create, run, and deploy`.

| :warning: Regarding Previous Versions.          |
|:---------------------------|
| The package name changed from `vue-cli` to `@vue/cli`. If you have the previous `vue-cli` (1.x or 2.x) package installed globally, you need to uninstall it first with `npm uninstall vue-cli -g` or `yarn global remove vue-cli`.  |


1. Install Veu CLI by **npm** or **yarn** `npm install -g @vue/cli` or `yarn global add @vue/cli`
2. Check Vue version `vue --version` and any help of cammand `vue --help`
3. Make a project of Vue `vue create project-name` and select by it one pacage manager like`npm` or `yarn`.
4. Go to project directory `cd /project_dir` and run `yarn serve`
5. To create a production build, run `yarn build`.
6. For convenience, this can be added to `package.json` scripts. [Link here](https://stackoverflow.com/questions/47034452/how-to-run-production-site-after-build-vue-cli)
```json
"scripts": {
    "serve": "vue-cli-service serve",
    "build": "vue-cli-service build",
    "lint": "vue-cli-service lint",
    "production": "vue-cli-service serve --mode production"
  }
```
and run `yarn run production`.<br>
7. Deployment [Heroku](https://cli.vuejs.org/guide/deployment.html#heroku) and [read doc here](https://cli.vuejs.org/guide/deployment.html)



### Ruby on Rails - [Help](https://github.com/plabon-asad/study-with-ror)
