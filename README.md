# Install odoo (v15) on a new Ubuntu environment and config with pycharm 

### Install pycharm
_Community version_
```
sudo snap install pycharm-community --classic
```
_Professional version_
```
sudo snap install pycharm-professional --classic
```
_Educational version_
```
sudo snap install pycharm-educational --classic
```

### Install PostgreSQL and create a database
_Install PostgreSQL_
```
sudo apt-get install postgresql
```
_Create a database_
```
sudo su - postgres -c "createuser -s <database name>"
sudo su postgres
-----------------------------------------------------
psql
ALTER ROLE odoo13 WITH PASSWORD '<databse password>';
exit
-----------------------------------------------------
```
### Install Wkhtmltopdf
```
sudo wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb
sudo dpkg -i wkhtmltox_0.12.5-1.bionic_amd64.deb
sudo apt install -f
```
### Install git
```
sudo apt-get install git
```
***Let turn your pycharm on and create a project (venv environment)***
### Open terminal on pycharm and clone oddoo15 into pycharm's project
```
git clone https://github.com/odoo/odoo --depth 1 --branch 15.0
```
### Install file requirement.txt or pycharm can do it for you
```
sudo pip3 install -r <path>/requirement.txt
```
You can check it again, just make sure everything's normal
__"CTRL+ALT+S" >> Project: || name project || >> Python Interpreter__


