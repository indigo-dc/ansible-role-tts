Token Translation Service Role
==============================

Configure and start the (TTS)[https://github.com/indigo-dc/tts].

This role has been specifically developed to be used for the deployment of the TTS in the framework of the INDIGO-DataCloud project.

Role Variables
--------------

 - `config_dir` (default `"/etc/tts"`) Where to put configuration
 - `deb_get_url` (required) Where to get the Ubuntu package from
 - `rpm_get_url` (required) Where to get the CentOS package from

Requirements
------------
 - *CentOS 7* or *Ubuntu 14.04 LTS* on the nodes

Example Playbook
----------------

See (sample/test.yml)[https://github.com/indigo-dc/ansible-role-tts/tree/master/sample/test.yml].

License
-------

Apache Licence v2 [1]

[1] http://www.apache.org/licenses/LICENSE-2.0

