Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

* `tempest_undercloud`: false/true - whether to run tempest on installed undercloud
* `tempest_overcloud`: false/true - whether to run tempest on installed overcloud
* `tempest_source`: rdo/upstream - Where to take tempest sources from - RDO package or upstream git repo
* `tempest_format`: venv/packages - Which tempest installation to use - either install python virtual environment
                    with installed there python modules from requirements file, or to use installed with RDO RPM packages
* `tempest_log_file` - name of log file for tempest run
* `test_regex` - tests regular expression for testr run, i.e. ".*smoke" 
* `run_tempest`: false/true - to run tempest or not


Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    ---
    - name:  Run tempest
      hosts: undercloud
      gather_facts: no
      roles:
        - tripleo-tempest

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
