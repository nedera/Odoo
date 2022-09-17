### Install Python 3 and its Dependencies
```
sudo apt update
sudo apt install software-properties-common
sudo add-apt-repository ppa:deadsnakes/ppa
sudo apt install python3.8
sudo apt install build-essential zlib1g-dev libncurses5-dev libgdbm-dev libnss3-dev libssl-dev libreadline-dev libffi-dev libsqlite3-dev wget libbz2-dev
sudo apt install python3-pip  wget python3-dev python3-venv python3-wheel libxml2-dev libpq-dev libjpeg8-dev liblcms2-dev libxslt1-dev zlib1g-dev libsasl2-dev libldap2-dev build-essential git libssl-dev libffi-dev libmysqlclient-dev libjpeg-dev libblas-dev libatlas-base-dev -y
```
### Install Wkhtmltopdf
```
sudo wget https://github.com/wkhtmltopdf/wkhtmltopdf/releases/download/0.12.5/wkhtmltox_0.12.5-1.bionic_amd64.deb
sudo dpkg -i wkhtmltox_0.12.5-1.bionic_amd64.deb
sudo apt install -f
```
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
ALTER ROLE <database name> WITH PASSWORD '<databse password>';
exit
-----------------------------------------------------
```

### Install git
```
sudo apt-get install git
```
***Let turn on your pycharm on and create a project (venv environment)***
### Open terminal on pycharm and clone oddoo15 into pycharm's project
```
git clone https://github.com/odoo/odoo --depth 1 --branch 15.0 --single-branch .
```
### Install file requirement.txt or pycharm can do it for you
```
pip3 install -r <path>/requirement.txt
```
You can check it again, just make sure everything's normal <br />
__"CTRL+ALT+S" >> Project: || project name || >> Python Interpreter__
<br />
<br />
![image](https://user-images.githubusercontent.com/93069334/190204212-69587569-5c69-4343-8498-9b19ebf61c22.png)
<br />
<br />
<br />
Create new folder name conf (odoo/conf), coppy the file name odoo.conf (debian/odoo.conf) and paste it in conf. You can change the name if you want (fill file "odoo.conf" coppy version) 
<br />
<br />
![image](https://user-images.githubusercontent.com/93069334/190202770-589e1d46-2e70-40c6-9444-9a530e1ca09c.png) ![image](https://user-images.githubusercontent.com/93069334/190207739-3c0a58f4-eaff-42ca-9642-69f6f3f3c3f6.png)
<br />
<br />
<br />
Last step, link __"|| project name ||/odoo/odoo-bin"__ and __"|| project name ||/conf/|| conf file ||__ with __Run >> Edit configuration__ (pycharm)
<br />
<br />
![image](https://user-images.githubusercontent.com/93069334/190212073-fd616210-f5e6-4f29-ba73-f3009e86b111.png)
<br />
<br />
<br />
### ERROR
module 'lib' has no attribute 'X509_V_FLAG_CB_ISSUER_CHECK'
```
pip install --upgrade pyOpenSSL
```
module 'werkzeug.routing' has no attribute 'NumberConverter'
```
pip freeze | grep Werkzeug
pip3 install Werkzeug==0.16.1  
```
Fall install pypsycopg2
```
pip install psycopg2-binary
```
