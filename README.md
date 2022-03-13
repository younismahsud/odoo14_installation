# Odoo 14 installation
How to install Odoo 14 on ubuntu 20.04
#### Step #1: Update the server
```
sudo apt-get update
sudo apt -y upgrade
```
#### Step #2: Install packages and libraries
```
sudo apt install git python3-pip build-essential wget python3-dev libpq-dev python3-venv python3-wheel libxslt-dev libzip-dev libldap2-dev libsasl2-dev python3-setuptools node-less
```
#### Step #3: Create a system user for Odoo 14
`sudo useradd -m -d /opt/odoov14 -U -r -s /bin/bash odoov14`
#### Step #4: Install Postgresql server
`sudo apt install postgresql`
#### Step #5: Create Postgresql user for Odoo 14
`sudo su - postgres -c "createuser -s odoov14"`
#### Step #6: Set the password for Odoov14 Postgresql user
```
sudo su postgres
psql
ALTER ROLE odoov14 WITH PASSWORD 'odoov14';
```
Press ctrl + Z to exist this and then execute `exit` command to exist postgres user
