---
layout: post
title:  "Linux Commands"
date:   2015-09-01
desc: "Linux and MySQL"
keywords: "linux,mysql,安装,install"
categories: [Python]
tags: [Linux]
icon: fa-database
---


```
[root@ rhel5 local]#tar -zxv -f cmake-2.8.4.tar.gz
[root@ rhel5 local]#cd cmake-2.8.4
[root@ rhel5 cmake-2.8.4]#./configure
[root@ rhel5 cmake-2.8.4]#make
[root@ rhel5 cmake-2.8.4]#make install
```


```
[root@ rhel5~]#mkdir -p /usr/local/mysql                 //安装mysql 
[root@ rhel5~]#mkdir -p /usr/local/mysql/data            //存放数据库
```

(3)创建mysql用户及用户组

```
[root@ rhel5~]groupadd mysql
[root@ rhel5~]useradd -r -g mysql mysql
```

(4)安装mysql

```
[root@ rhel5 local]#tar -zxv -f mysql-5.5.10.tar.gz
[root@ rhel5 local]#cd mysql-5.5.10
```

```
[root@ rhel5 mysql-5.5.10]#cmake . 
-DCMAKE_INSTALL_PREFIX=/usr/local/mysql
-DMYSQL_DATADIR=/usr/local/mysql/data
-DDEFAULT_CHARSET=utf8
-DDEFAULT_COLLATION=utf8_general_ci 
-DEXTRA_CHARSETS=all 
-DENABLED_LOCAL_INFILE=1
```

```
[root@ rhel5 mysql-5.5.10]#make
[root@ rhel5 mysql-5.5.10]#make install
```


* -DCMAKE_INSTALL_PREFIX=/usr/local/mysql 

* -DINSTALL_DATADIR=/usr/local/mysql/data  

* -DDEFAULT_CHARSET=utf8                    

* -DDEFAULT_COLLATION=utf8_general_ci  


`PATH=$PATH:$HOME/bin:/usr/local/mysql/bin:/usr/local/mysql/lib`

```
[root@ rhel5~]#source /root/.bash_profile
```


``` sql
mysql>GRANT ALL PRIVILEGES ON *.* TO 'root'@'%' IDENTIFIED BY '******' WITH GRANT OPTION;
```

