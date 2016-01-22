SUP (Service Up)
================
This is a script which check a service status to make sure that it is running. If the service is off, this script will start it to keep the service running.

WARNING: You have to execute this application as root or another user which is allowed to execute commands to manage services, such as systemctl.

Installation
============
```sh
$ sudo su -
$ cd /tmp/
$ wget https://github.com/luoldrigues/sup/archive/master.zip
$ unzip master.zip; cd sup-master
$ mv sup /usr/local/bin
$ sup --help
```

Help
====
```sh
$ sup --help
Usage: sup <SERVICE> {COMMAND} [OPTIONS...]

COMMAND:
  keepup           Try to KEEP the service UP

OPTIONS:
  -h, --help       Show this help
  -v, --verbose    Verbosely list processed
      --usage      Give a short usage message
      --version    Print program version

Examples:
   sup httpd keepup --verbose
   sup mariadb keepup -v
   sup firewalld keepup -v
   sup --help

You might use this program in your crontab
Cron example:
  */15 * * * * /usr/local/bin/sup mariadb keepup
  The line above execute every 15 minutes to check the MariaDB service
  For more details see 'man crontab'
```

Usage
=====
```sh
$ sup --usage
Usage: sup <SERVICE> {keepup} [--help] [--verbose] [--usage] [--version]

Examples:
   sup httpd keepup --verbose
   sup mariadb keepup -v
   sup firewalld keepup
   sup --help
```

Version
=======
```sh
$ sup --version
sup version 0.2
GNU License <http://gnu.org/licenses/gpl.html>.
This is a free software! You are allowed to change and redistribute it for free.
Written by Luan Rodrigues - https://github.com/luoldrigues/sup
```

Compatible
==========
- Red Hat 7
- Centos 7
- Fedora 7

