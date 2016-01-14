Ansible Role for NTP
====================

[![Build Status](https://travis-ci.org/pantarei/ansible-role-ntp.svg?branch=master)](https://travis-ci.org/pantarei/ansible-role-ntp)
[![GitHub tag](https://img.shields.io/github/tag/pantarei/ansible-role-ntp.svg)](https://github.com/pantarei/ansible-role-ntp)
[![GitHub license](https://img.shields.io/github/license/pantarei/ansible-role-ntp.svg)](https://github.com/pantarei/ansible-role-ntp/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/6131.svg)](https://galaxy.ansible.com/detail#/role/6131)

Ansible Role for NTP Management.

Requirements
------------

This role require Ansible 2.0 or higher.

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
<td align="left"><a href="https://github.com/pantarei/ansible-role-ntp/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Configures setting of generation file set name.</td>
</tr>
<tr class="odd">
<td align="left">ntp_server</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-ntp/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Specify one or more NTP servers.</td>
</tr>
<tr class="even">
<td align="left">ntp_restrict</td>
<td align="left">yes</td>
<td align="left"><a href="https://github.com/pantarei/ansible-role-ntp/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td align="left"><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td align="left">Access control configuration; see <a href="http://support.ntp.org/bin/view/Support/AccessRestrictions">web page</a> for details.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: servers
      roles:
        - { role: hswong3i.ntp }

License
-------

-   Code released under [MIT](https://github.com/pantarei/ansible-role-ntp/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)

Author Information
------------------

-   Wong Hoi Sing Edison
    -   <https://twitter.com/hswong3i>
    -   <https://github.com/hswong3i>

