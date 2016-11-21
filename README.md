# `dc`

`dc` is a proto utility written in bash to encapsulate basic commands for projects in Canic interactive machine devbox21.com.

Future plans will include a rewrite in `nodejs` and web GUI with local terminal CLI.

Usage:
  dc command [project environment arguments]

# Commands:

## System

### `i, init`

Init the environment with all needed components, no need to use on this system.

```
$ dc init
```

### `m, make, m8, make8`

Make the project by building directory structure and docker-compose.yml for three environments, dev, stage and prod.

```
$ dc make myproj drupal7
$ dc make8 myproj drupal8
$ dc makew myproj wordpress
```

### `l, list`

List all projects.

```
$ dc list
```

### `a, archive`

Archive project, remove from active tree.

```
$ dc archive myproj
```

### `d, delete`

delete whole project structure

```
$ dc delete myproj
```

## Drupal

### `d7, drupal-7, d8, drupal-8`

Install fresh drupal in project for environment.

```
    $ dc drupal-7 myproj dev
    $ dc drupal-8 myproj8 dev
```

### `dr, drush`

Execute drush commands on project in environment.

```
$ dc drush myproj dl views
```

## Docker

### `s, start`

Start project containers for environment.

```
$ dc start myproj dev
```

### `r, restart`

Restart project containers for environment.

```
$ dc restart myproj prod
```

### `k, kill`

Kill project containers for environment.

```
$ dc kill myproj stage
```

### `st, status`

Gives status of the project containers for environment or all containers.

```
$ dc status
$ dc status myproj
```

## Git

### `gc, git-clone`

git clone repository in project for environment.

```
$ dc git-clone myproj dev git@bitbucket.org:user/project.git
```

### `gco, git-checkout`

git checkout branch in project for environment.

```
$ dc git-checkout myproj dev master
```

### `gba, git-branch-all`

git show all branches in project for environment.

```
$ dc git-branch-all myproj dev
```

### `gp, git-pull`

git pull latest code in project for environment.

```
$ dc git-pull myproj dev
```

### `gst, git-status`

git status of remote repository in project for environment.

```
$ dc git-status myproj dev
```

## MySQL

### `dbl, db-list`

List all available databases in project.

```
$ dc db-list
```

### `dbi, db-import`

Import database in project for environment.

```
$ dc db_import myproj dev myprojdump_20161118-0941.sql
```

### `dbe, db-export`

Export database from project in environment to databases directory.

```
$ dc db-export myproj dev
```

Have a wish, suggestion? Mail me macmladen@gmail.com

Carpe diem.
