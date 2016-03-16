Ansible Role for NTP
====================

[![Build Status](https://travis-ci.org/vitalied/ansible-role-ntp.svg?branch=master)](https://travis-ci.org/vitalied/ansible-role-ntp)
[![GitHub tag](https://img.shields.io/github/tag/vitalied/ansible-role-ntp.svg)](https://github.com/vitalied/ansible-role-ntp)
[![GitHub license](https://img.shields.io/github/license/vitalied/ansible-role-ntp.svg)](https://github.com/vitalied/ansible-role-ntp/blob/master/LICENSE)
[![Ansible Role](https://img.shields.io/ansible/role/8536.svg)](https://galaxy.ansible.com/vitalied/ntp)

Ansible Role for NTP Management.

Requirements
------------

This role require Ansible 2.1 or higher.

This role was designed for Ubuntu Server 16.04 LTS.

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
<th>parameter</th>
<th>required</th>
<th>default</th>
<th>choices</th>
<th>comments</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ntp_server</td>
<td>yes</td>
<td><a href="https://github.com/vitalied/ansible-role-ntp/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Specify one or more NTP servers.</td>
</tr>
<tr class="even">
<td>ntp_restrict</td>
<td>yes</td>
<td><a href="https://github.com/vitalied/ansible-role-ntp/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Access control configuration; see <a href="http://support.ntp.org/bin/view/Support/AccessRestrictions">web page</a> for details.</td>
</tr>
<tr class="odd">
<td>ntp_broadcast</td>
<td>no</td>
<td><a href="https://github.com/vitalied/ansible-role-ntp/blob/master/defaults/main.yml">defaults/main.yml</a></td>
<td><ul>
<li><code>[]</code></li>
<li><code>list</code></li>
</ul></td>
<td>Specify one or more broadcast IPs.</td>
</tr>
</tbody>
</table>

Dependencies
------------

No additional role dependencies.

Example Playbook
----------------

    - hosts: all
      roles:
        - role: vitalied.ntp

License
-------

-   Code released under [MIT](https://github.com/vitalied/ansible-role-ntp/blob/master/LICENSE)
-   Docs released under [CC BY 4.0](http://creativecommons.org/licenses/by/4.0/)
