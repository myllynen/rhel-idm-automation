# RHEL IdM Automation

[![License: GPLv3](https://img.shields.io/badge/license-GPLv3-brightgreen.svg)](https://www.gnu.org/licenses/gpl-3.0)

Ansible playbooks for RHEL IdM automation.

## Contents

* [inventory](inventory) | [doc](https://github.com/freeipa/ansible-freeipa#ansible-inventory-file)
  * Example inventory
* [vars_ad.yml](vars_ad.yml) | [doc](https://github.com/freeipa/ansible-freeipa/blob/master/README-trust.md),
  [vars_ca.yml](vars_ca.yml) | [doc](https://github.com/freeipa/ansible-freeipa/tree/master/roles/ipaserver#certificate-system-variables),
  [vars_dns.yml](vars_dns.yml) | [doc](https://github.com/freeipa/ansible-freeipa/tree/master/roles/ipaserver#dns-variables),
  [vars_ipa.yml](vars_ipa.yml) | [doc](https://github.com/freeipa/ansible-freeipa/tree/master/roles/ipaserver#base-variables)
  * Vars files for playbooks
* [vault_ipa.yml](vault_ipa.yml) | [doc](https://github.com/freeipa/ansible-freeipa#ansible-inventory-file)
  * Unencrypted example vault file
* [ipa_server_install.yml](ipa_server_install.yml) | [doc](https://github.com/freeipa/ansible-freeipa/tree/master/roles/ipaserver)
  * Playbook to install IdM master server
* [ipa_replica_install.yml](ipa_replica_install.yml) | [doc](https://github.com/freeipa/ansible-freeipa/tree/master/roles/ipareplica)
  * Playbook to install IdM replicas
* [ipa_server_configure.yml](ipa_server_configure.yml) | [doc](https://github.com/freeipa/ansible-freeipa)
  * Playbook to install IdM replicas
* [ipa_adtrust_setup.yml](ipa_adtrust_setup.yml) | [doc](https://github.com/freeipa/ansible-freeipa/blob/master/README-trust.md)
  * Playbook to setup IdM AD trust
* [ipa_data_setup.yml](ipa_data_setup.yml) | [doc](https://github.com/freeipa/ansible-freeipa)
  * Playbook to setup IdM identity and policy data
* [ipa_client_install.yml](ipa_client_install.yml) | [doc](https://github.com/freeipa/ansible-freeipa/tree/master/roles/ipaclient)
  * Playbook to install IdM clients
* [ipa_backup_create.yml](ipa_backup_create.yml) | [doc](https://github.com/freeipa/ansible-freeipa/tree/master/roles/ipabackup)
  * Playbook to create IdM server backup
* [ipa_backup_restore.yml](ipa_backup_restore.yml) | [doc](https://github.com/freeipa/ansible-freeipa/tree/master/roles/ipabackup)
  * Playbook to restore IdM server backup
* [ipa_cluster_update.yml](ipa_cluster_update.yml) | [doc](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/installing_identity_management/update-downgrade-ipa_installing-identity-management#updating_idm_packages)
  * Playbook to update IdM master/replica servers

Depending on the environment and requirements, separate vars files,
group vars, variables defined in an inventory, or some other approach
might be warranted. These examples aim to provide a known-good starting
point for common installation types.

## Quick Usage Example

To install IPA/IdM master server, replicas, and connect clients:

```
# Edit inventory and settings to suite local environment
vi inventory vars_ipa.yml vars_data.yml
# By default no AD trust, use internal CA, no DNS setup
less vars_ad.yml vars_ca.yml vars_dns.yml
# Install IPA/IdM master server
ansible-playbook -i inventory ipa_server_install.yml
# Install IPA/IdM replicas
ansible-playbook -i inventory ipa_replica_install.yml
# Configure IPA/IdM server and replicas
ansible-playbook -i inventory ipa_server_configure.yml
# Setup IPA/IdM identity and policy data
ansible-playbook -i inventory ipa_data_setup.yml
# Backup and update IPA/IdM server and replicas
ansible-playbook -i inventory ipa_backup_create.yml
ansible-playbook -i inventory ipa_cluster_update.yml
# Connect clients to IPA/IdM
ansible-playbook -i inventory ipa_client_install.yml
```

## See Also

See also
[https://github.com/freeipa/ansible-freeipa](https://github.com/freeipa/ansible-freeipa).

See also
[https://console.redhat.com/ansible/automation-hub/repo/published/redhat/rhel_idm](https://console.redhat.com/ansible/automation-hub/repo/published/redhat/rhel_idm).

See also
[https://github.com/myllynen/rhel-ansible-roles](https://github.com/myllynen/rhel-ansible-roles).

## License

GPLv3+
