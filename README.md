CentOS6.4環境
===================================

## 環境構成

### Provision 
Puppet (そのうちAnsibleで書きなおす)

## Set Up
### git clone
```
$ git clone git@github.com:chocopie116/vagrant_centos6.4.git
```
### vagrant up
```
$ cd vagrant_centos6.4
$ vagrant up
```
## Login
### demouser
```
$ ssh demouser@192.168.56.111
```
### vagrant
```
$ vagrant ssh
```
## Users

| OS user | pass | 続DB | 接続Port |  DB user |  DB pass | 用途 |
|:-----------:|:------------:|:------------:|:------------:|:------------:|:------------:|:------------:|
| root | vagrant | - | 3306 |  root | vagrant | root |
| vagrant | vagrant | - | - | - | - | vagrant用ユーザ |
| demouser | demouser | groupwork | 3306 | demouser | demopass | 開発ユーザ |

## Packages   
##### mysql
自動起動
/var/lib/mysql/my.cnf  
##### sshd
vagrant demouser
##### iptables
自動起動
port22,80 allow
##### httpd
自動起動
/etc/httpd/conf/httpd.conf
##### mongodb
自動起動

