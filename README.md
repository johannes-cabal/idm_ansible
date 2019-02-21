IDM_ANSIBLE
================

**This role is still under active development.**

Install and configure Red Hat IdM on a RHEL 7 system.
Configure a RHEL 7 system be be DISA STIG compliant. CAT I findings will be correceted and audited by default. CAT II and II findigs can be enabled by setting the appropriate variables to `yes`.

This role is based on [Red Hat Enterprise Linux 7 Product Documentation](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/linux_domain_identity_authentication_and_policy_guide/p.install).


Requirements
------------

RHEL 7. Other versions are not supported.

Role Variables
--------------
# Vars listing:
# vault_rhn_user
# vault_rhn_password

rhn_registration: false

idm_repositories:
  - rhel-7-server-extras-rpms
  - rhel-7-server-optional-rpms
| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `rhn_registration` | `false` | Subscribe to RHN - requires a Pool ID|
| `rhn_pool_name` | `no` | Desired pool ID to attach machine to when subscribing to RHN |
| `vault_rhn_user` | `no` | RHN user name - used for RHN registration (store in vault) |
| `vault_rhn_password` | `no` | RHN user password - user for RHN registration (store in vault) |

<!-- idm_fqdn
idm_admin_password
idm_password
idm_domain
idm_realm
idm_services
idm_repositories
idm_packages
common_packages -->

Dependencies
------------

None

Example Playbook
----------------


License
-------

MIT
