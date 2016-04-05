#### psinstconfapache(using ubuntu 14.04)
#####install
######intro
```
service httpd start
chkconfig httpd on
```
check listrning port
```
yum install lsof
lsof -i | grep httpd
```

#####configure access control
######intro
```
htpasswd -m -c filename username1      //-c : createfile
htpasswd -m filename username2
```
```
openssl req -x509 -nodes -deys 365 -newkey rsa:2048 -keyout /etc/httpd/ssl.apache.key -out /etc/httpd/ssl/apache.crt
openssl x509 -in apache.crt -text |less
```
