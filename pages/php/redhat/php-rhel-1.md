---
layout: page-steps
language: PHP
title: RHEL
permalink: /php/rhel/
redirect_from:
  - /php/
  - /php/rhel/step/
  - /php/rhel/step/1
---

> In this section, you will get SQL Server vNext running on RedHat Enterprise Linux. After that you will install the necessary dependencies to create PHP apps with SQL Server

## Step 1.1 Install SQL Server
{% include partials/install_sql_server_linux_rhel.md %}

## Step 1.2 Install PHP and other required packages


```terminal
    wget https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
    wget http://rpms.remirepo.net/enterprise/remi-release-7.rpm
    rpm -Uvh remi-release-7.rpm epel-release-latest-7.noarch.rpm
    subscription-manager repos --enable=rhel-7-server-optional-rpms
    yum update
    yum install php70-php httpd php-cli php-common php-devel php-fpm php-mbstring php-mcrypt php-pear
    yum groupinstall "Development Tools"
```

> You have successfuly installed PHP on your RHEL machine! 

## Step 1.3 Install the ODBC Driver and SQL Command Line Utility for SQL Server

{% include partials/install_sqlcmd_linux_rhel.md %}

