Token Translation Service Role
==============================

Configure and start the [TTS](https://github.com/indigo-dc/tts).

This role has been specifically developed to be used for the deployment of the *TTS* in the framework of the *INDIGO-DataCloud* project.

Role Variables
--------------

 - `config_dir` (default `"/etc/tts"`) Where to put configuration
 - `deb_get_url` (required) Where to get the Ubuntu package from
 - `rpm_get_url` (required) Where to get the CentOS package from

Requirements
------------
 - *CentOS 7* or *Ubuntu 14.04 LTS* on the nodes are explicily supported
 - Anything using *yum*+*systemd* or *apt*+*upstart* will should also be fine

Example Playbook
----------------

### By cloning this repo
See [sample/test.yml](https://github.com/indigo-dc/ansible-role-tts/tree/master/sample/test.yml).

### By using `ansible-galaxy(1)` (coming soon)
```yaml
- hosts: tts-server
  roles:
    - indigo-dc.tts
```

License
-------

Apache Licence v2 [1]

[1]: http://www.apache.org/licenses/LICENSE-2.0

