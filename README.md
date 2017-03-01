Token Translation Service Role
==============================

Configure and start the [WaTTS](https://github.com/indigo-dc/tts).

This role has been specifically developed to be used for the deployment of the *WaTTS* in the framework of the *INDIGO-DataCloud* project.

Role Variables
--------------

 - `deb_get_url`, `rpm_get_url` (optional): Define these to manually download
   the respective packages instead of using the INDIGO-DC repository

 - `indigo_repo`, `indigo_centos_repo_url`, `indigo_ubuntu_repo_url`,
   `indigo_pgp_key_url`: Use these to override how to access the INDIGO repository

 - `watts_pkg_name` (default: "tts"), `watts_service_name` (default: "watts")

 - `start_at_boot` (default: `no`) Whether to enable the WaTTS to be started at boot

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
   - Using the official vault:
   
     ```sh
      # ansible-galaxy install indigo-dc.tts
     ```
 - Give it a try:
 
   ```yaml
   - hosts: tts-server
      roles:
      - indigo-dc.tts
        start_at_boot: yes
   ```

   Then you can run it, e.g. using the provided sample playbook:

   ```sh
    $ ansible-playbook sample/example.yml --inventory=sample/inventory
   ```
   Of course, you will need to adapt
   [sample/inventory](https://github.com/indigo-dc/ansible-role-tts/tree/master/sample/inventory)
   according to your needs, or leave the `--inventory` option out and use the default `/etc/ansible/hosts`.

   See also: [sample/example.yml](https://github.com/indigo-dc/ansible-role-tts/tree/master/sample/example.yml).

License
-------

Apache Licence v2 [1]

[1]: http://www.apache.org/licenses/LICENSE-2.0
