Ansible Role for NTP
====================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-ntp.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-ntp)
 [![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-ntp.svg)](https://github.com/pantarei/ansible-role-ntp)
 [![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-ntp.svg)](https://github.com/pantarei/ansible-role-ntp/blob/master/LICENSE)
 [![Ansible Role](https://img.shields.io/ansible/role/6131.svg)](https://galaxy.ansible.com/detail#/role/6131)

Ansible Role for NTP Management.

Requirements
------------

This role require Ansible 1.9 or higher.

This role was designed for Ubuntu Server 14.04 LTS.

Role Variables
--------------

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">parameter</th>
<th align="left">required</th>
<th align="left">default</th>
<th align="left">choices</th>
<th align="left">comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left">ntp_driftfile</td>
<td align="left">yes</td>
<td align="left">/var/lib/ntp/ntp.drift</td>
<td align="left"></td>
<td align="left">Specify the name and path of the frequency file.</td>
</tr>
<tr class="even">
<td align="left">ntp_statsdir</td>
<td align="left">no</td>
<td align="left">/var/log/ntpstats</td>
<td align="left"></td>
<td align="left">Specify the directory path for files created by the statistics facility.</td>
</tr>
<tr class="odd">
<td align="left">ntp_statistics</td>
<td align="left">no</td>
<td align="left">loopstats peerstats clockstats</td>
<td align="left"></td>
<td align="left">Enables writing of statistics records.</td>
</tr>
<tr class="even">
<td align="left">ntp_filegen</td>
<td align="left">no</td>
<td align="left"><ul>
<li>loopstats file loopstats type day enable</li>
<li>peerstats file peerstats type day enable</li>
<li>clockstats file clockstats type day enable</li>
</ul></td>
<td align="left"></td>
<td align="left">Configures setting of generation file set name.</td>
</tr>
<tr class="odd">
<td align="left">ntp_server</td>
<td align="left">yes</td>
<td align="left"><ul>
<li>0.ubuntu.pool.ntp.org</li>
<li>1.ubuntu.pool.ntp.org</li>
<li>2.ubuntu.pool.ntp.org</li>
<li>3.ubuntu.pool.ntp.org</li>
<li>ntp.ubuntu.com</li>
</ul></td>
<td align="left"></td>
<td align="left">Specify one or more NTP servers.</td>
</tr>
<tr class="even">
<td align="left">ntp_restrict</td>
<td align="left">yes</td>
<td align="left"><ul>
<li>-4 default kod notrap nomodify nopeer noquery</li>
<li>-6 default kod notrap nomodify nopeer noquery</li>
<li>127.0.0.1</li>
<li>::1</li>
</ul></td>
<td align="left"></td>
<td align="left">Access control configuration; see <a href="http://support.ntp.org/bin/view/Support/AccessRestrictions" class="uri">http://support.ntp.org/bin/view/Support/AccessRestrictions</a> for details.</td>
</tr>
</tbody>
</table>

Dependencies
------------

-   [hswong3i.apt](https://galaxy.ansible.com/detail#/role/5970)

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.ntp }

License
-------

-   Code released under [MIT](https://github.com/hswong3i/ansible-role-ntp/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

