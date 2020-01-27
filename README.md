目录结构：

```bash
docker/
├── build
│   └── php
│       └── Dockerfile
├── conf
│   ├── mysql
│   │   └── docker.cnf
│   ├── nginx
│   │   ├── conf.d
│   │   │   └── default.conf
│   │   └── nginx.conf
│   └── php
│       ├── php
│       │   └── php.ini
│       └── php-fpm
│           ├── php-fpm.conf
│           ├── php-fpm.conf.default
│           └── php-fpm.d
│               ├── docker.conf
│               ├── www.conf
│               ├── www.conf.default
│               └── zz-docker.conf
├── data
├── docker-compose.yml
├── log
│   ├── mysql
│   ├── nginx
│   └── php
├── README.md
└── www
```