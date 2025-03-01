# RELEASE NOTES

## 0.2.2 (Aug 2, 2021)

IMPROVEMENTS:

- **New Resource:** `centrify_federatedgroup`
- **New Data Resource:** `centrify_federatedgroup`

BUG FIXES:

- `mapping` argument is updated from block to map. Refer to document and example for details.
- Updated example for `centrify_globalgroupmappings`
- `bulkupdate` argument for `centrify_globalgroupmappings` resource is defaulted to true now
- `client_secret` argument for `centrify_webapp_oidc` resource is optional and sensitive now

## 0.2.0 (June 23, 2021)

IMPROVEMENTS:

- Port from terraform-provider-centrifyvault to terraform-provider-centrify
- Change provider name from `centrifyvault` to `centrify`
- Rename all resources from `centrifyvault_*` to `centrify_*`. To keep backwards compatibility, existing `centrifyvault_*` can still be used but will be removed in the future.
  - `centrifyvault_user` -> `centrify_user`
  - `centrifyvault_role` -> `centrify_role`
  - `centrifyvault_policy` -> `centrify_policy`
  - `centrifyvault_manualset` -> `centrify_manualset`
  - `centrifyvault_passwordprofile` -> `centrify_passwordprofile`
  - `centrifyvault_authenticationprofile` -> `centrify_authenticationprofile`
  - `centrifyvault_connector` -> `centrify_connector`
  - `centrifyvault_vaultdomain` -> `centrify_domain`
  - `centrifyvault_vaultsystem` -> `centrify_system`
  - `centrifyvault_vaultdatabase` -> `centrify_database`
  - `centrifyvault_vaultaccount` -> `centrify_account`
  - `centrifyvault_vaultsecret` -> `centrify_secret`
  - `centrifyvault_vaultsecretfolder` -> `centrify_secretfolder`
  - `centrifyvault_sshkey` -> `centrify_sshkey`
  - `centrifyvault_desktopapp` -> `centrify_desktopapp`
  - `centrifyvault_directoryservice` -> `centrify_directoryservice`
  - `centrifyvault_directoryobject` -> `centrify_directoryobject`
  - `centrifyvault_multiplexedaccount` -> `centrify_multiplexedaccount`
  - `centrifyvault_service` -> `centrify_service`
  - `centrifyvault_cloudprovider` -> `centrify_cloudprovider`
  - `centrifyvault_webapp_saml` -> `centrify_webapp_saml`
  - `centrifyvault_webapp_oauth` -> `centrify_webapp_oauth`
  - `centrifyvault_webapp_oidc` -> `centrify_webapp_oidc`
  - `centrifyvault_webapp_generic` -> `centrify_webapp_generic`
- Rename all data resources from `centrifyvault_*` to `centrify_*`. To keep backwards compatibility, existing `centrifyvault_*` can still be used but will be removed in the future.
  - `centrifyvault_user` -> `centrify_user`
  - `centrifyvault_role` -> `centrify_role`
  - `centrifyvault_policy` -> `centrify_policy`
  - `centrifyvault_policyorder` -> `centrify_policyorder`
  - `centrifyvault_manualset` -> `centrify_manualset`
  - `centrifyvault_passwordprofile` -> `centrify_passwordprofile`
  - `centrifyvault_authenticationprofile` -> `centrify_authenticationprofile`
  - `centrifyvault_connector` -> `centrify_connector`
  - `centrifyvault_vaultdomain` -> `centrify_domain`
  - `centrifyvault_vaultdomainreconciliation` -> `centrify_domainreconciliation`
  - `centrifyvault_vaultdomainconfiguration` -> `centrify_domainconfiguration`
  - `centrifyvault_vaultsystem` -> `centrify_system`
  - `centrifyvault_vaultdatabase` -> `centrify_database`
  - `centrifyvault_vaultaccount` -> `centrify_account`
  - `centrifyvault_vaultsecret` -> `centrify_secret`
  - `centrifyvault_vaultsecretfolder` -> `centrify_secretfolder`
  - `centrifyvault_sshkey` -> `centrify_sshkey`
  - `centrifyvault_desktopapp` -> `centrify_desktopapp`
  - `centrifyvault_directoryservice` -> `centrify_directoryservice`
  - `centrifyvault_directoryobject` -> `centrify_directoryobject`
  - `centrifyvault_multiplexedaccount` -> `centrify_multiplexedaccount`
  - `centrifyvault_service` -> `centrify_service`
  - `centrifyvault_cloudprovider` -> `centrify_cloudprovider`
  - `centrifyvault_globalgroupmappings` -> `centrify_globalgroupmappings`
  - `centrifyvault_globalworkflow` -> `centrify_globalworkflow`
  - `centrifyvault_webapp_saml` -> `centrify_webapp_saml`
  - `centrifyvault_webapp_oauth` -> `centrify_webapp_oauth`
  - `centrifyvault_webapp_oidc` -> `centrify_webapp_oidc`
  - `centrifyvault_webapp_generic` -> `centrify_webapp_generic`

BUG FIXES:

- `centrifyvault_connector` data source can properly query Connector with status='Active' parameter

## 0.1.6 (May 15, 2021)

IMPROVEMENTS:

- New `bulkupdate` argument for `centrifyvault_globalgroupmappings` resource.

## 0.1.5 (April 21, 2021)

FEATURES:

- **New Data Resource:** `centrifyvault_desktopapp`
- **New Data Resource:** `centrifyvault_service`

IMPROVEMENTS:

- Add support for importing resources

## 0.1.4 (April 9, 2021)

IMPROVEMENTS:

- Expose more attributes reference for all data source types.

BUG FIXES:

- `centrifyvault_connector` data source fail to run when Connector is not installed on AD joined machine.

## 0.1.3 (April 6, 2021)

FEATURES:

- **New Resource:** `centrifyvault_globalworkflow`
- **New Resource:** `centrifyvault_webapp_generic`
- **New Resource:** `centrifyvault_webapp_saml`
- **New Resource:** `centrifyvault_webapp_oauth`
- **New Resource:** `centrifyvault_webapp_oidc`
- **New Data Resource:** `centrifyvault_webapp_generic`
- **New Data Resource:** `centrifyvault_webapp_saml`
- **New Data Resource:** `centrifyvault_webapp_oauth`
- **New Data Resource:** `centrifyvault_webapp_oidc`

IMPROVEMENTS:

- `centrifyvault_connector` data source
  - Add `status`, `forest`, `version` and `vpc_identifier` search attributes
  - Add more attribute references.
- `centrifyvault_vaultaccount` resource
  - Add `workflow_enabled` and `workflow_approver` attributes
- `centrifyvault_desktopapp` resource
  - Add `workflow_enabled` and `workflow_approver` attributes
- `centrifyvault_vaultsecret` resource
  - Add `workflow_enabled` and `workflow_approver` attributes
- `centrifyvault_vaultsystem` resource
  - Add Agent Auth and Privilege Elevation Workflow related attributes: `agent_auth_workflow_enabled`, `agent_auth_workflow_approver`, `privilege_elevation_workflow_enabled` and `privilege_elevation_workflow_approver`.
  - Add Zone Role Workflow related attributes: `use_domainadmin_for_zonerole_workflow`, `enable_zonerole_workflow`, `use_domain_assignment_for_zoneroles`, `assigned_zonerole`, `use_domain_assignment_for_zonerole_approvers` and `assigned_zonerole_approver`.
- Replace `centrifyvault_vaultdomainreconciliation` with `centrifyvault_vaultdomainconfiguration`
  - Add `enable_zonerole_workflow`, `assigned_zonerole` and `assigned_zonerole_approver` attribute to `centrifyvault_vaultdomainconfiguration`
- `centrifyvault_vaultdomain` resource
  - Rename `enable_zone_role_cleanup` to `enable_zonerole_cleanup`
  - Rename `zone_role_cleanup_interval` to `zonerole_cleanup_interval`
  - Add `parent_id` and `forest_id` attributes
- Improve error message for all data sources when object can't be found.

BUG FIXES:

- `centrifyvault_vaultaccount` resource: `password` attribute causes apply action always update resource.
- Detect `challenge_rule` change in tenant for these Terraform managed resources: `resource_desktopapp`, `resource_sshkey`, `resource_vaultaccount`, `resource_vaultcloudprovider`, `resource_vaultsecret` and `resource_vaultsystem`.

## 0.1.2 (March 18, 2021)

BUG FIXES:

- Documentation links and file layout.

## 0.1.1 (March 14, 2021)

BUG FIXES:

- `connector_list` attribute in for `centrifyvault_vaultsystem` resource doesn't take effect during creation.
- Documentation links.

## 0.1.0 (March 14, 2021)

- Initial release
