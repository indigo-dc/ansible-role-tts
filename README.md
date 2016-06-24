Token Translation Service Role
==============================

Configure and start the [TTS](https://github.com/indigo-dc/tts).

This role has been specifically developed to be used for the deployment of the *TTS* in the framework of the *INDIGO-DataCloud* project.

Role Variables
--------------

 - `config_dir` (default `"/etc/tts"`) Where to put configuration
 - `deb_get_url` (required) Where to get the Ubuntu package from
 - `rpm_get_url` (required) Where to get the CentOS package from
 - `start_at_boot` (default: `no`) Whether to enable the TTS to be started at boot
 
Requirements
------------
 - *CentOS 7* or *Ubuntu 14.04 LTS* on the nodes are explicily supported
 - Anything using *yum*+*systemd* or *apt*+*upstart* should also be fine

Example Playbook
----------------

 - Install the role
   - From the repo:
   
     ```sh
      # ansible-galaxy install -r sample/requirements.yml
     ```
   - Using the official vault (coming soon):
   
     ```sh
      # ansible-galaxy install indigo-dc.tts
      ```
 - Try it out:
 
   ```yaml
   - hosts: tts-server
      roles:
      - indigo-dc.tts
        deb_get_url: "http://example.org/tts.deb"
        rpm_get_url: "http://example.org/tts.rpm"
   ```

   ```sh
    $ ansible-playbook sample/test.yml --inventory=sample/inventory
   ```
   Of course, you will need to adapt
   [sample/inventory](https://github.com/indigo-dc/ansible-role-tts/tree/master/sample/test.yml)
   according to your needs, or leave the `--inventory` option out and use the default `/etc/ansible/hosts`.

   See also: [sample/test.yml](https://github.com/indigo-dc/ansible-role-tts/tree/master/sample/test.yml).

License
-------

Apache Licence v2 [1]

[1]: http://www.apache.org/licenses/LICENSE-2.0
