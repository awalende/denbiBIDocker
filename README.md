Role Name
=========

Installs the docker engine on Ubuntu 18.04 Bionic Cloud and configures its mtu and registry-mirror targeting the environment of the deNBI Cloud in Bielefeld.
It is not recommended to execute this role on non denbiBI instances since the provided registry is only usable from the denbi network.

Requirements
------------

Any Python Version needs to be installed prior. Probably works with 2.7 and 3.x.

Role Variables
--------------

defaults/main.yml:

| Variable		| Default		| Description			|
| ------------- |:-------------:| ---------------------:|
| defaultUser | ubuntu | The default user which will be added to the docker group. Needed for starting containers from userspace. |
| mtu | 1454 | Custom network MTU value for OpenStack based instances. |
| registry | https://docker.bi.denbi.de:8888 | Custom registry. The default is blocked when connected from foreign sources. |


Dependencies
------------

No dependencies right now.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - awalende.denbiBIDocker

License
-------

Apache 2.0

Author Information
------------------

M. Sc Alex Walender

[denBI.de](https://cloud.denbi.de)
