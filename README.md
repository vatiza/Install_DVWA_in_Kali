# Install DVWA on kali linux



## Installation
Open terminal dload dvwa from github and put the directroy ``` cd /var/www/html/ ```

```bash
cd /var/www/html/ 
```
```bash
sudo git clone https://github.com/digininja/DVWA.git
```
```bash
sudo chmod -R 777 DVWA
```
```bash
cd DVWA/config
```
```bash
sudo cp config.inc.php.dist config.inc.php
```
 config.inc.php set username and password \
``` username= admin``` \
```password=password```
```bash
sudo nano config.inc.php
```
```bash
sudo service mysql start
```
open mySql server \
``` default have no password press enter```

```bash
sudo mysql -u root -p  
```
create new database : 
```bash
create database dvwa;
```
create user in database:
```bash
create user 'admin'@'127.0.0.1' identified by 'password';
```
grant all permission on user 
```bash
grant all privileges on dvwa.* to 'admin'@'127.0.0.1' identified by 'password';
```
mysql ``` exit``` now  

```bash
sudo service apache2 start
```

my php version 8.1. you have deferent.
check you php version. open new terminal  write command 

```bash
cd /etc/php/
```
ls (show all file and folders in this directory)


```bash
sudo nano /etc/php/8.1/apache2/php.ini

```
nano (ctrl+W- search) fopen, set fopen=On { allow_url_fopen = On and allow_url_fopen = On } save (ctrl+x) yes(y) press enter

```bash
sudo service apache2 reload
```
# Done 

## Usage
goto browser insert url- ``` https://localhost/DVWA``` 

```python
open DVWA click(setup/ResetDb) and see the bottom create/resetDB btn then click the btn
```
### --------WOOW DVWA installed-------



[Rakib](https://www.facebook.com/v4tiza)
