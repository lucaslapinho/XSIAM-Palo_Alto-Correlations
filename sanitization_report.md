# Sanitization Report

## Summary

- Correlations discovered: 146
- Importable JSON files generated: 146
- Vendors identified: 20
- Rules requiring sanitization: 34
- Rules requiring manual review: 0

Only sanitization categories are recorded. Original sensitive values are intentionally excluded.
Public product identifiers, MITRE ATT&CK references, technical domains, and detection indicators are retained when required by the rule logic.

## Sanitized Rules

### `Airflow/slp_airflow_dag_failure_detected.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Airflow/slp_airflow_s3_dag_failure_detected.json`

Removed or replaced:

- Email addresses and account identifiers
- Hostnames, service accounts, applications, and internal resource names
- Internal integration identifiers

### `AWS/aws_critical_ec2_instances_stop_ou_terminate.json`

Removed or replaced:

- Cloud resource identifiers
- Hostnames, service accounts, applications, and internal resource names

### `AWS/aws_iam_user_creation.json`

Removed or replaced:

- Email addresses and account identifiers

### `Cisco/cisco_switch_multiplos_logins_bem_sucedidos_em_varios_switches_8_em_1h.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Cortex/ctx_broker_vm_cluster_down.json`

Removed or replaced:

- Organization and client names

### `Cortex/ctx_falha_nos_broker_vms.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Cortex/ctx_suspicious_code_hosting_download_followed_by_msi_installation.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Cortex/endpoint_monitorado_online_copy.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Cortex/endpoint_monitorado_online.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Fortigate/ftg_local_user_account_created.json`

Removed or replaced:

- Organization and personal names

### `Imperva/ipv_new_site_created_on_waf.json`

Removed or replaced:

- Organization and personal names
- Organization-specific domains and tenant names

### `Imperva/ipv_removing_ssl_from_site.json`

Removed or replaced:

- Organization and personal names
- Organization-specific domains and tenant names

### `Imperva/ipv_site_removed_from_waf.json`

Removed or replaced:

- Organization and personal names
- Organization-specific domains and tenant names

### `Imperva/ipv_site_waf_disabled.json`

Removed or replaced:

- Organization and personal names
- Organization-specific domains and tenant names

### `Linux/lnx_external_key_based_access.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names
- Internal IP addresses

### `Linux/lnx_privilege_escalation.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Microsoft 365/o365_copilot_bot_has_been_created.json`

Removed or replaced:

- Organization and client names

### `Microsoft 365/o365_public_or_external_sharing_link_created.json`

Removed or replaced:

- Email addresses and account identifiers

### `Microsoft 365/o365_success_login_outside_brazil.json`

Removed or replaced:

- Email addresses and account identifiers
- Hostnames, service accounts, applications, and internal resource names
- Organization-specific domains and tenant names

### `Microsoft 365/o365_suspicious_external_teams_chat_from_known_tenant.json`

Removed or replaced:

- Organization-specific domains and tenant names

### `Microsoft EntraID/azure_login_outside_allowed_regions.json`

Removed or replaced:

- Organization and personal names
- Organization-specific domains and tenant names
- Organization-specific rule naming

### `Microsoft EntraID/ms_suspicious_useragent_login_detected.json`

Removed or replaced:

- Email addresses and account identifiers
- Hostnames, service accounts, applications, and internal resource names

### `Trend Micro/trd_visionone_detection_critical.json`

Removed or replaced:

- Organization and personal names

### `Trend Micro/trd_visionone_detection_high.json`

Removed or replaced:

- Organization and personal names

### `Trend Micro/trd_visionone_detection_medium.json`

Removed or replaced:

- Organization and personal names

### `Windows/ms_user_added_to_monitored_group.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Windows/thm_exposed_passwords_in_command_lines.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Windows/win_ad_multiple_user_creations_sailpoint_error.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Windows/win_ad_multiple_user_creations_sailpoint.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Windows/win_ad_multiple_user_creations.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Windows/win_ad_multiple_user_deletions.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Windows/win_ad_multiple_users_disabled.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

### `Windows/win_mass_account_disablement_by_sailpoint_service_account.json`

Removed or replaced:

- Hostnames, service accounts, applications, and internal resource names

