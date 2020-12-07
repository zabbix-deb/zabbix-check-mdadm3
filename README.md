# zabbix-check-mdadm3

## Description

mdadm monitoring scripts for [zabbix](https://zabbix.com)-agent.

This repository provides a low level discovery script, which discover mdadm devices and a second script which get the array state and faulty disk count.

**Note**: This is yet another rewrite of [zabbix-check-mdadm](https://github.com/zabbix-deb/debs/tree/master/debs/zabbix-check/zabbix-check-mdadm) respectively [zabbix-check-mdadm2](https://github.com/zabbix-deb/zabbix-check-mdadm2), but this time we read the data from sysfs, instead of parsing "/proc/mdstat" and "mdadm -D". Also this version is written in POSIX sh, so no dependencies for python et cetera.

## Usage

* Clone this repo and build the debian package yourself with `LANG=C debuild -us -uc -b; dh clean`
**or**
* Install it directly from @istoph's [repository](https://blog.chr.istoph.de/repository/)
**or**
* Clone this repo and install the script and config by hand

## Dependencies

* POSIX sh

## Licence

New BSD License/BSD 3-Clause License (see [debian/copyright](debian/copyright))

## Template for the Zabbix frontend

A template for the Zabbix frontend can be found, as usual in our packages, in [/usr/share/doc/${package_name}/examples](examples/)

