# RHEL IdM Automation

[![License: GPLv2](https://img.shields.io/badge/license-GPLv2-brightgreen.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)
[![License: GPLv3](https://img.shields.io/badge/license-GPLv3-brightgreen.svg)](https://www.gnu.org/licenses/gpl-3.0)

Ansible playbooks and roles for RHEL IdM automation.

## Contents

* [inventory](inventory)
  * Example vars file to install IdM server/replicas/clients
* [vars_ipa.yml](vars_ipa.yml)
  * Example vars file to install IdM server/replicas/clients
* [vault_ipa.yml](vault_ipa.yml)
  * Unencrypted vault file
* [ipa_server_install.yml](ipa_server_install.yml)
  * Example playbook to install IdM master server
* [ipa_replica_install.yml](ipa_replica_install.yml)
  * Example playbook to install IdM replicas
* [ipa_adtrust_setup.yml](ipa_adtrust_setup.yml)
  * Example playbook to setup IdM AD trust
* [ipa_client_install.yml](ipa_client_install.yml)
  * Example playbook to install IdM clients
* [ipa_server_backup_create.yml](ipa_server_backup_create.yml)
  * Example playbook to create IdM server backup
* [ipa_server_backup_restore.yml](ipa_server_backup_restore.yml)
  * Example playbook to restore IdM server backup

Depending on the environment and requirements, separate vars files,
group vars, variables defined in the inventory, or some other approach
might be warranted. These examples aim to provide a known-good start
point for common installation types.

## See Also

See also
[https://github.com/myllynen/rhel-ansible-roles](https://github.com/myllynen/rhel-ansible-roles).

## License

GPLv2+
