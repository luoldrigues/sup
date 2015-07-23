SUP (Service Up)
================
Check a specified service status to keep it running.

PS: You should execute this application using root user or other user which is allowed to execute commands to restart services (using: systemctl)

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
sup version 0.1
GNU License <http://gnu.org/licenses/gpl.html>.
This is a free software! You are allowed to change and redistribute it for free.
Written by Luan Rodrigues - https://github.com/luoldrigues/sup
```

Compatible
==========
- Red Hat 7
- Centos 7
- Fedora 7

