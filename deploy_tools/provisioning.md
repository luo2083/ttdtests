Provisioning a new site
========================
## Required packages:
* nginx
* Python 3.6.6
* virtualenv + pip
* Git

eg,on centos7:
    yum -y update
    yum install "Developments tools"
    yum install nginx python3.6-venv

## Nginx virtual host config
* see nginx.template.conf
* replace DOMAIN with , e.g,lechangagriculture.cn

## Systemd service
* see qunicorn-systemd.template.service
* replace DOMAIN with , e.g,lechangagriculture.cn

## Folder structure:
Assume we have a user account at /home/username
/home/username
└── sites
    ├── DOMAIN1
    │    ├── .env
    │    ├── db.sqlite3
    │    ├── manage.py etc
    │    ├── static
    │    └── virtualenv
    └── DOMAIN2
         ├── .env
         ├── db.sqlite3
         ├── etc