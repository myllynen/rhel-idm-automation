# RHEL IdM Automation

[![License: GPLv2](https://img.shields.io/badge/license-GPLv2-brightgreen.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html)
[![License: GPLv3](https://img.shields.io/badge/license-GPLv3-brightgreen.svg)](https://www.gnu.org/licenses/gpl-3.0)

Ansible playbooks for RHEL IdM automation.

## Contents

* [inventory](inventory)
  * Example inventory
* [vars_ad.yml](vars_ad.yml), [vars_ca.yml](vars_ca.yml),
  [vars_dns.yml](vars_dns.yml), [vars_ipa.yml](vars_ipa.yml)
  * Vars files for playbooks
* [vault_ipa.yml](vault_ipa.yml)
  * Unencrypted example vault file
* [ipa_server_install.yml](ipa_server_install.yml)
  * Playbook to install IdM master server
* [ipa_replica_install.yml](ipa_replica_install.yml)
  * Playbook to install IdM replicas
* [ipa_adtrust_setup.yml](ipa_adtrust_setup.yml)
  * Playbook to setup IdM AD trust
* [ipa_client_install.yml](ipa_client_install.yml)
  * Playbook to install IdM clients
* [ipa_server_backup_create.yml](ipa_server_backup_create.yml)
  * Playbook to create IdM server backup
* [ipa_server_backup_restore.yml](ipa_server_backup_restore.yml)
  * Playbook to restore IdM server backup
* [ipa_update_servers.yml](ipa_update_servers.yml)
  * Playbook to update IdM master/replica servers

Depending on the environment and requirements, separate vars files,
group vars, variables defined in an inventory, or some other approach
might be warranted. These examples aim to provide a known-good starting
point for common installation types.

## See Also

See also
[https://github.com/myllynen/rhel-ansible-roles](https://github.com/myllynen/rhel-ansible-roles).

## License

GPLv2+
