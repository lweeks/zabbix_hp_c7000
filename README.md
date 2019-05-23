# zabbix_hp_c7000
HP C7000 Blade System template for Zabbix

Based on the C7000 Chassis template by Vladimir Marakshin. https://share.zabbix.com/cat-server-hardware/hp/c7000-chassis

This has been updated to work with Zabbix 4.2. It has had some Russian
changed to English, and added the Onboard Administrators to the discovery
rule. It also only discovers device bays that have a device in them.

Note that the original template required the HP/CPQ MIBs, and still
does. It does not use numeric OIDs.

The MIB files can be downloaded from HPE. This link worked to reach the
MIB Kit when this was uploaded:

https://support.hpe.com/hpsc/doc/public/display?docLocale=en_US&docId=emr_na-c04272529

At least the cpqhost.mib and cpqrack.mib MIBs must be installed in your
Zabbix server/proxy (the host that executes the SNMP checks). On a
CentOS/RHEL system, that is in /usr/share/snmp/mibs. After they are
installed, the Zabbix server/proxy must be restarted.
