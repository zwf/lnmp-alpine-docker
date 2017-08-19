# LNMP test docker images

### Intro

A TEST LNMP docker environment for preview a php webapp. The whole project should not be used in production environment,because all the configs are not considering the safety factors, the only target is easy and fast to setup a environment for preview a php webapp.

### Architecture

There are 3 containers: nginx, php-fpm, mysql(MariaDB). All of the containers are from alpine linux image.
```
browser <-> nginx container <-> php container <-> mysql(MariaDB) container
            |                   |                 |
            └─ ./app/website/ ──┘                 └─ ./app/dbfile/
```

### Directory Structure

```
├── app
│   ├── dbfile // mysql dbfiles
│   ├── log
│   │   ├── mysqllog // mysql logs
│   │   └── nginxlog // nginx logs
│   └── website // webapp files
└── configs
    ├── mysql // mysql config
    ├── nginx // nginx config
    └── php // php config
```

### Run

* install Docker and Docker Compose

