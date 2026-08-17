# Cortex XSIAM Correlation Rules

Import-ready, documented, and sanitized Cortex XSIAM correlation rules organized by technology vendor.

## GitHub Description

Import-ready and sanitized Palo Alto Cortex XSIAM correlation rules organized by technology vendor for the Detection Engineering community.

## Overview

The repository contains 146 standalone correlation rules across 20 vendors. Every rule is stored as a single-element JSON array so it can be reviewed and imported independently.
All rules are delivered with `is_enabled: false` to prevent activation before environment-specific review and testing.

## Repository Structure

```text
.
|-- Airflow/
|-- AWS/
|-- BeyondTrust/
|-- Cisco/
|-- Cortex/
|-- Fortigate/
|-- GIT/
|-- Imperva/
|-- Keycloak/
|-- Linux/
|-- Microsoft 365/
|-- Microsoft Defender/
|-- Microsoft EntraID/
|-- OpenCTI/
|-- Palo Alto NGFW/
|-- SailPoint/
|-- Tenable/
|-- Trend Micro/
|-- Windows/
|-- Wiz/
|-- manifest.json
|-- sanitization_report.md
`-- README.md
```

## Vendors

| Vendor | Description | Rules |
|---|---|---:|
| AWS | AWS CloudTrail, IAM, EC2, and cloud activity detections | 3 |
| BeyondTrust | BeyondTrust EPM and Password Safe detections | 10 |
| Cisco | Cisco network device and switch detections | 3 |
| Cortex | Cortex XDR and XSIAM platform detections | 24 |
| Fortigate | Fortinet FortiGate security detections | 12 |
| GIT | GitHub repository activity detections | 3 |
| Imperva | Imperva WAF detections | 4 |
| Keycloak | Keycloak authentication detections | 2 |
| Linux | Linux host and authentication detections | 4 |
| Microsoft 365 | Microsoft 365, Teams, Exchange, and SharePoint detections | 11 |
| Microsoft Defender | Microsoft Defender alert ingestion detections | 1 |
| Microsoft EntraID | Microsoft Entra ID identity and authentication detections | 13 |
| OpenCTI | OpenCTI threat intelligence workflow detections | 1 |
| Palo Alto NGFW | Palo Alto Networks NGFW operational detections | 1 |
| SailPoint | SailPoint IdentityNow detections | 3 |
| Tenable | Tenable cloud exposure detections | 5 |
| Trend Micro | Trend Micro Vision One detections | 5 |
| Windows | Windows endpoint and Active Directory detections | 38 |
| Wiz | Wiz cloud security alert detections | 1 |

## Importing a Rule

1. Open **Cortex XSIAM > Detection > Correlation Rules**.
2. Choose the import option and select one rule JSON file.
3. Replace every `<PLACEHOLDER>` with a value appropriate for the target environment.
4. Review the dataset, fields, schedule, suppression, severity, and MITRE ATT&CK mapping.
5. Test the query before enabling alert generation.

## Correlation Rules

### AWS

| Rule | Import File |
|---|---|
| AWS_Critical EC2 instances (Stop ou Terminate) | [`AWS/aws_critical_ec2_instances_stop_ou_terminate.json`](<AWS/aws_critical_ec2_instances_stop_ou_terminate.json>) |
| AWS_IAM User creation | [`AWS/aws_iam_user_creation.json`](<AWS/aws_iam_user_creation.json>) |
| AWS_Instance Accessed via SSM | [`AWS/aws_instance_accessed_via_ssm.json`](<AWS/aws_instance_accessed_via_ssm.json>) |

### BeyondTrust

| Rule | Import File |
|---|---|
| BYT_Brute Force Authentication Attempt Detected | [`BeyondTrust/byt_brute_force_authentication_attempt_detected.json`](<BeyondTrust/byt_brute_force_authentication_attempt_detected.json>) |
| BYT_User Add to Admin Group | [`BeyondTrust/byt_user_add_to_admin_group.json`](<BeyondTrust/byt_user_add_to_admin_group.json>) |
| BYT_User Removed from Admin Group | [`BeyondTrust/byt_user_removed_from_admin_group.json`](<BeyondTrust/byt_user_removed_from_admin_group.json>) |
| EPM_Elevated Command and Scripting Interpreter | [`BeyondTrust/epm_elevated_command_and_scripting_interpreter.json`](<BeyondTrust/epm_elevated_command_and_scripting_interpreter.json>) |
| EPM_Endpoint Added to Monitored Group | [`BeyondTrust/epm_endpoint_added_to_monitored_group.json`](<BeyondTrust/epm_endpoint_added_to_monitored_group.json>) |
| EPM_PowerShell Privilege Elevation Activity | [`BeyondTrust/epm_powershell_privilege_elevation_activity.json`](<BeyondTrust/epm_powershell_privilege_elevation_activity.json>) |
| EPM_Remote Access Tool Privilege Elevation Activity | [`BeyondTrust/epm_remote_access_tool_privilege_elevation_activity.json`](<BeyondTrust/epm_remote_access_tool_privilege_elevation_activity.json>) |
| EPM_Repeated Denied or Blocked Privilege Attempts | [`BeyondTrust/epm_repeated_denied_or_blocked_privilege_attempts.json`](<BeyondTrust/epm_repeated_denied_or_blocked_privilege_attempts.json>) |
| EPM_User-Writable Path Privilege Elevation Activity | [`BeyondTrust/epm_user_writable_path_privilege_elevation_activity.json`](<BeyondTrust/epm_user_writable_path_privilege_elevation_activity.json>) |
| MS_Admin Group Modified | [`BeyondTrust/ms_admin_group_modified.json`](<BeyondTrust/ms_admin_group_modified.json>) |

### Cisco

| Rule | Import File |
|---|---|
| Cisco Switch – MAC Flapping alto (≥70 em 10 min) | [`Cisco/cisco_switch_mac_flapping_alto_70_em_10_min.json`](<Cisco/cisco_switch_mac_flapping_alto_70_em_10_min.json>) |
| Cisco Switch – Múltiplos logins bem-sucedidos em vários switches (≥8 em 1h) | [`Cisco/cisco_switch_multiplos_logins_bem_sucedidos_em_varios_switches_8_em_1h.json`](<Cisco/cisco_switch_multiplos_logins_bem_sucedidos_em_varios_switches_8_em_1h.json>) |
| Dataset cisco_switch health check de ingestão | [`Cisco/dataset_cisco_switch_health_check_de_ingestao.json`](<Cisco/dataset_cisco_switch_health_check_de_ingestao.json>) |

### Cortex

| Rule | Import File |
|---|---|
| CTX_Broker VM Cluster Down | [`Cortex/ctx_broker_vm_cluster_down.json`](<Cortex/ctx_broker_vm_cluster_down.json>) |
| CTX_Critical Endpoints Disconnected | [`Cortex/ctx_critical_endpoints_disconnected.json`](<Cortex/ctx_critical_endpoints_disconnected.json>) |
| CTX_Deno JavaScript Execution from AppData or Temp Directory | [`Cortex/ctx_deno_javascript_execution_from_appdata_or_temp_directory.json`](<Cortex/ctx_deno_javascript_execution_from_appdata_or_temp_directory.json>) |
| CTX_Deno Runtime Remote JavaScript Execution with Allow-All Permissions | [`Cortex/ctx_deno_runtime_remote_javascript_execution_with_allow_all_permissions.json`](<Cortex/ctx_deno_runtime_remote_javascript_execution_with_allow_all_permissions.json>) |
| CTX_Disable Prevention Rule Created | [`Cortex/ctx_disable_prevention_rule_created.json`](<Cortex/ctx_disable_prevention_rule_created.json>) |
| CTX_Endpoint EDR Protection Manually Paused | [`Cortex/ctx_endpoint_edr_protection_manually_paused.json`](<Cortex/ctx_endpoint_edr_protection_manually_paused.json>) |
| CTX_Endpoint EDR Protection Paused | [`Cortex/ctx_endpoint_edr_protection_paused.json`](<Cortex/ctx_endpoint_edr_protection_paused.json>) |
| CTX_Endpoint EDR Protection Uninstall | [`Cortex/ctx_endpoint_edr_protection_uninstall.json`](<Cortex/ctx_endpoint_edr_protection_uninstall.json>) |
| CTX_Falha nos Broker VMs | [`Cortex/ctx_falha_nos_broker_vms.json`](<Cortex/ctx_falha_nos_broker_vms.json>) |
| CTX_MSBuild Outbound Network Connection to Public Infrastructure | [`Cortex/ctx_msbuild_outbound_network_connection_to_public_infrastructure.json`](<Cortex/ctx_msbuild_outbound_network_connection_to_public_infrastructure.json>) |
| CTX_New Prevention Policy Created | [`Cortex/ctx_new_prevention_policy_created.json`](<Cortex/ctx_new_prevention_policy_created.json>) |
| CTX_Potential Browser Credential and Session Cookie Theft | [`Cortex/ctx_potential_browser_credential_and_session_cookie_theft.json`](<Cortex/ctx_potential_browser_credential_and_session_cookie_theft.json>) |
| CTX_Prevention Policy Changed | [`Cortex/ctx_prevention_policy_changed.json`](<Cortex/ctx_prevention_policy_changed.json>) |
| CTX_PromptSnatcher Malicious Browser Extension Detected | [`Cortex/ctx_promptsnatcher_malicious_browser_extension_detected.json`](<Cortex/ctx_promptsnatcher_malicious_browser_extension_detected.json>) |
| CTX_RBAC_Role_Created | [`Cortex/ctx_rbac_role_created.json`](<Cortex/ctx_rbac_role_created.json>) |
| CTX_RBAC_Role_Edited | [`Cortex/ctx_rbac_role_edited.json`](<Cortex/ctx_rbac_role_edited.json>) |
| CTX_Stealer Behavior - Sensitive Wallet Data Staging in AppData | [`Cortex/ctx_stealer_behavior_sensitive_wallet_data_staging_in_appdata.json`](<Cortex/ctx_stealer_behavior_sensitive_wallet_data_staging_in_appdata.json>) |
| CTX_Suspicious Code Hosting Download Followed by MSI Installation | [`Cortex/ctx_suspicious_code_hosting_download_followed_by_msi_installation.json`](<Cortex/ctx_suspicious_code_hosting_download_followed_by_msi_installation.json>) |
| CTX_Suspicious Svchost Execution from Temporary Directory | [`Cortex/ctx_suspicious_svchost_execution_from_temporary_directory.json`](<Cortex/ctx_suspicious_svchost_execution_from_temporary_directory.json>) |
| CTX_Suspicious WScript to PowerShell to MSBuild Execution Chain | [`Cortex/ctx_suspicious_wscript_to_powershell_to_msbuild_execution_chain.json`](<Cortex/ctx_suspicious_wscript_to_powershell_to_msbuild_execution_chain.json>) |
| CTX_WordPress Suspicious PHP Write by Web Process | [`Cortex/ctx_wordpress_suspicious_php_write_by_web_process.json`](<Cortex/ctx_wordpress_suspicious_php_write_by_web_process.json>) |
| CTX_XDR Collector Failed | [`Cortex/ctx_xdr_collector_failed.json`](<Cortex/ctx_xdr_collector_failed.json>) |
| Endpoint Monitorado Online | [`Cortex/endpoint_monitorado_online.json`](<Cortex/endpoint_monitorado_online.json>) |
| Endpoint Monitorado Online (Copy) | [`Cortex/endpoint_monitorado_online_copy.json`](<Cortex/endpoint_monitorado_online_copy.json>) |

### Fortigate

| Rule | Import File |
|---|---|
| FGT_BGP Communication Failure | [`Fortigate/fgt_bgp_communication_failure.json`](<Fortigate/fgt_bgp_communication_failure.json>) |
| FTG_Antivirus Suspicious File Download | [`Fortigate/ftg_antivirus_suspicious_file_download.json`](<Fortigate/ftg_antivirus_suspicious_file_download.json>) |
| FTG_Conserve Mode Activated | [`Fortigate/ftg_conserve_mode_activated.json`](<Fortigate/ftg_conserve_mode_activated.json>) |
| FTG_DOS Policy Possible DDoS Attack (Copy) | [`Fortigate/ftg_dos_policy_possible_ddos_attack_copy.json`](<Fortigate/ftg_dos_policy_possible_ddos_attack_copy.json>) |
| FTG_High CPU Usage | [`Fortigate/ftg_high_cpu_usage.json`](<Fortigate/ftg_high_cpu_usage.json>) |
| FTG_High Memory Usage | [`Fortigate/ftg_high_memory_usage.json`](<Fortigate/ftg_high_memory_usage.json>) |
| FTG_IPS Allowed Signature Detected | [`Fortigate/ftg_ips_allowed_signature_detected.json`](<Fortigate/ftg_ips_allowed_signature_detected.json>) |
| FTG_Local User Account Created | [`Fortigate/ftg_local_user_account_created.json`](<Fortigate/ftg_local_user_account_created.json>) |
| FTG_Web Filter: Access to Malicious Category | [`Fortigate/ftg_web_filter_access_to_malicious_category.json`](<Fortigate/ftg_web_filter_access_to_malicious_category.json>) |
| REPORT-FTG_Successful RDP | [`Fortigate/report_ftg_successful_rdp.json`](<Fortigate/report_ftg_successful_rdp.json>) |
| REPORT-FTG_Web Filter: Access to AI Category | [`Fortigate/report_ftg_web_filter_access_to_ai_category.json`](<Fortigate/report_ftg_web_filter_access_to_ai_category.json>) |
| REPORT-FTG_Web Filter: Access to Suspicious Category | [`Fortigate/report_ftg_web_filter_access_to_suspicious_category.json`](<Fortigate/report_ftg_web_filter_access_to_suspicious_category.json>) |

### GIT

| Rule | Import File |
|---|---|
| GIT_Public Repository Created | [`GIT/git_public_repository_created.json`](<GIT/git_public_repository_created.json>) |
| GIT_Repository Created | [`GIT/git_repository_created.json`](<GIT/git_repository_created.json>) |
| GIT_Repository Unarchived | [`GIT/git_repository_unarchived.json`](<GIT/git_repository_unarchived.json>) |

### Imperva

| Rule | Import File |
|---|---|
| IPV_New Site Created on WAF | [`Imperva/ipv_new_site_created_on_waf.json`](<Imperva/ipv_new_site_created_on_waf.json>) |
| IPV_Removing SSL from Site | [`Imperva/ipv_removing_ssl_from_site.json`](<Imperva/ipv_removing_ssl_from_site.json>) |
| IPV_Site Removed from WAF | [`Imperva/ipv_site_removed_from_waf.json`](<Imperva/ipv_site_removed_from_waf.json>) |
| IPV_Site WAF Disabled | [`Imperva/ipv_site_waf_disabled.json`](<Imperva/ipv_site_waf_disabled.json>) |

### Keycloak

| Rule | Import File |
|---|---|
| KCK_High Volume Of Logins | [`Keycloak/kck_high_volume_of_logins.json`](<Keycloak/kck_high_volume_of_logins.json>) |
| KCK_Multiple Public IP Logins per User | [`Keycloak/kck_multiple_public_ip_logins_per_user.json`](<Keycloak/kck_multiple_public_ip_logins_per_user.json>) |

### Linux

| Rule | Import File |
|---|---|
| LNX_External Key-Based Access | [`Linux/lnx_external_key_based_access.json`](<Linux/lnx_external_key_based_access.json>) |
| LNX_Ngrok Free Usage | [`Linux/lnx_ngrok_free_usage.json`](<Linux/lnx_ngrok_free_usage.json>) |
| LNX_Privilege Escalation | [`Linux/lnx_privilege_escalation.json`](<Linux/lnx_privilege_escalation.json>) |
| LNX_Unexpected Process Running su for Privilege Escalation | [`Linux/lnx_unexpected_process_running_su_for_privilege_escalation.json`](<Linux/lnx_unexpected_process_running_su_for_privilege_escalation.json>) |

### Microsoft 365

| Rule | Import File |
|---|---|
| MS_Teams Federation Settings Modified | [`Microsoft 365/ms_teams_federation_settings_modified.json`](<Microsoft 365/ms_teams_federation_settings_modified.json>) |
| O365_Admin Privileges Granted | [`Microsoft 365/o365_admin_privileges_granted.json`](<Microsoft 365/o365_admin_privileges_granted.json>) |
| O365_Copilot BOT has been created | [`Microsoft 365/o365_copilot_bot_has_been_created.json`](<Microsoft 365/o365_copilot_bot_has_been_created.json>) |
| O365_External Teams Support Impersonation Attempt | [`Microsoft 365/o365_external_teams_support_impersonation_attempt.json`](<Microsoft 365/o365_external_teams_support_impersonation_attempt.json>) |
| O365_Mailbox Rule Creation | [`Microsoft 365/o365_mailbox_rule_creation.json`](<Microsoft 365/o365_mailbox_rule_creation.json>) |
| O365_Massive File Download | [`Microsoft 365/o365_massive_file_download.json`](<Microsoft 365/o365_massive_file_download.json>) |
| O365_Public or External Sharing Link Created | [`Microsoft 365/o365_public_or_external_sharing_link_created.json`](<Microsoft 365/o365_public_or_external_sharing_link_created.json>) |
| O365_Success ADMIN Login Outside Brazil | [`Microsoft 365/o365_success_admin_login_outside_brazil.json`](<Microsoft 365/o365_success_admin_login_outside_brazil.json>) |
| O365_Success Login Outside Brazil | [`Microsoft 365/o365_success_login_outside_brazil.json`](<Microsoft 365/o365_success_login_outside_brazil.json>) |
| O365_Success VIP Login outside Brazil | [`Microsoft 365/o365_success_vip_login_outside_brazil.json`](<Microsoft 365/o365_success_vip_login_outside_brazil.json>) |
| O365_Suspicious External Teams Chat from Known Tenant | [`Microsoft 365/o365_suspicious_external_teams_chat_from_known_tenant.json`](<Microsoft 365/o365_suspicious_external_teams_chat_from_known_tenant.json>) |

### Microsoft Defender

| Rule | Import File |
|---|---|
| DFD_Microsoft 365 Defender Alerts (automatically generated) | [`Microsoft Defender/dfd_microsoft_365_defender_alerts_automatically_generated.json`](<Microsoft Defender/dfd_microsoft_365_defender_alerts_automatically_generated.json>) |

### Microsoft EntraID

| Rule | Import File |
|---|---|
| AZURE_Login Outside Allowed Regions | [`Microsoft EntraID/azure_login_outside_allowed_regions.json`](<Microsoft EntraID/azure_login_outside_allowed_regions.json>) |
| MS_Azure Possible Brute Force - Bad Username Password by IP | [`Microsoft EntraID/ms_azure_possible_brute_force_bad_username_password_by_ip.json`](<Microsoft EntraID/ms_azure_possible_brute_force_bad_username_password_by_ip.json>) |
| MS_CrossTenant Partner Added Success | [`Microsoft EntraID/ms_crosstenant_partner_added_success.json`](<Microsoft EntraID/ms_crosstenant_partner_added_success.json>) |
| MS_EntraID Add User Outside Detected | [`Microsoft EntraID/ms_entraid_add_user_outside_detected.json`](<Microsoft EntraID/ms_entraid_add_user_outside_detected.json>) |
| MS_EntraID Application Creation Detected | [`Microsoft EntraID/ms_entraid_application_creation_detected.json`](<Microsoft EntraID/ms_entraid_application_creation_detected.json>) |
| MS_Multiple User Login Attempt from Same Source - PassSpray | [`Microsoft EntraID/ms_multiple_user_login_attempt_from_same_source_passspray.json`](<Microsoft EntraID/ms_multiple_user_login_attempt_from_same_source_passspray.json>) |
| MS_RiskEvent Anomalous Token Detected | [`Microsoft EntraID/ms_riskevent_anomalous_token_detected.json`](<Microsoft EntraID/ms_riskevent_anomalous_token_detected.json>) |
| MS_RiskEvent AnonymizedIP Login Detected (VPN/TOR) | [`Microsoft EntraID/ms_riskevent_anonymizedip_login_detected_vpn_tor.json`](<Microsoft EntraID/ms_riskevent_anonymizedip_login_detected_vpn_tor.json>) |
| MS_RiskEvent Malicious IP Login Detected | [`Microsoft EntraID/ms_riskevent_malicious_ip_login_detected.json`](<Microsoft EntraID/ms_riskevent_malicious_ip_login_detected.json>) |
| MS_RiskEvent Unfamiliar Features Login Detected | [`Microsoft EntraID/ms_riskevent_unfamiliar_features_login_detected.json`](<Microsoft EntraID/ms_riskevent_unfamiliar_features_login_detected.json>) |
| MS_Suspicious High-Privilege App Role Assignment | [`Microsoft EntraID/ms_suspicious_high_privilege_app_role_assignment.json`](<Microsoft EntraID/ms_suspicious_high_privilege_app_role_assignment.json>) |
| MS_Suspicious UserAgent Login Detected | [`Microsoft EntraID/ms_suspicious_useragent_login_detected.json`](<Microsoft EntraID/ms_suspicious_useragent_login_detected.json>) |
| MS_Users Added to Global or Device Admin Roles | [`Microsoft EntraID/ms_users_added_to_global_or_device_admin_roles.json`](<Microsoft EntraID/ms_users_added_to_global_or_device_admin_roles.json>) |

### OpenCTI

| Rule | Import File |
|---|---|
| CTI_Data Leak Issue Creator | [`OpenCTI/cti_data_leak_issue_creator.json`](<OpenCTI/cti_data_leak_issue_creator.json>) |

### Palo Alto NGFW

| Rule | Import File |
|---|---|
| NGFW_HA Failure | [`Palo Alto NGFW/ngfw_ha_failure.json`](<Palo Alto NGFW/ngfw_ha_failure.json>) |

### SailPoint

| Rule | Import File |
|---|---|
| SLP_IDN Source Created | [`SailPoint/slp_idn_source_created.json`](<SailPoint/slp_idn_source_created.json>) |
| SLP_IDN_Source_Updated | [`SailPoint/slp_idn_source_updated.json`](<SailPoint/slp_idn_source_updated.json>) |
| SLP_VA Cluster Status Change Event | [`SailPoint/slp_va_cluster_status_change_event.json`](<SailPoint/slp_va_cluster_status_change_event.json>) |

### Tenable

| Rule | Import File |
|---|---|
| TNB_EC2 Instance Exposing Secrets Detected | [`Tenable/tnb_ec2_instance_exposing_secrets_detected.json`](<Tenable/tnb_ec2_instance_exposing_secrets_detected.json>) |
| TNB_Public Lambda Function is exposing secrets Detected | [`Tenable/tnb_public_lambda_function_is_exposing_secrets_detected.json`](<Tenable/tnb_public_lambda_function_is_exposing_secrets_detected.json>) |
| TNB_Public Load Balancer Detected | [`Tenable/tnb_public_load_balancer_detected.json`](<Tenable/tnb_public_load_balancer_detected.json>) |
| TNB_Public Storage Account Blob Container Detected | [`Tenable/tnb_public_storage_account_blob_container_detected.json`](<Tenable/tnb_public_storage_account_blob_container_detected.json>) |
| TNB_Public Virtual Machine Created | [`Tenable/tnb_public_virtual_machine_created.json`](<Tenable/tnb_public_virtual_machine_created.json>) |

### Trend Micro

| Rule | Import File |
|---|---|
| TRD_Automatic Alerts | [`Trend Micro/trd_automatic_alerts.json`](<Trend Micro/trd_automatic_alerts.json>) |
| TRD_Ransomware Detection | [`Trend Micro/trd_ransomware_detection.json`](<Trend Micro/trd_ransomware_detection.json>) |
| TRD_VisionOne_Detection_Critical | [`Trend Micro/trd_visionone_detection_critical.json`](<Trend Micro/trd_visionone_detection_critical.json>) |
| TRD_VisionOne_Detection_High | [`Trend Micro/trd_visionone_detection_high.json`](<Trend Micro/trd_visionone_detection_high.json>) |
| TRD_VisionOne_Detection_Medium | [`Trend Micro/trd_visionone_detection_medium.json`](<Trend Micro/trd_visionone_detection_medium.json>) |

### Windows

| Rule | Import File |
|---|---|
| MS_Multiple Kerberos Authentication Failures | [`Windows/ms_multiple_kerberos_authentication_failures.json`](<Windows/ms_multiple_kerberos_authentication_failures.json>) |
| MS_User Added to Monitored Group | [`Windows/ms_user_added_to_monitored_group.json`](<Windows/ms_user_added_to_monitored_group.json>) |
| Multiplas alterações de credenciais | [`Windows/multiplas_alteracoes_de_credenciais.json`](<Windows/multiplas_alteracoes_de_credenciais.json>) |
| THM_Browser Process with suspicious CommandLine | [`Windows/thm_browser_process_with_suspicious_commandline.json`](<Windows/thm_browser_process_with_suspicious_commandline.json>) |
| THM_ClickFix Detection | [`Windows/thm_clickfix_detection.json`](<Windows/thm_clickfix_detection.json>) |
| THM_cmd.exe LNK Execution | [`Windows/thm_cmd_exe_lnk_execution.json`](<Windows/thm_cmd_exe_lnk_execution.json>) |
| THM_Curl with ChatID and Telegram API | [`Windows/thm_curl_with_chatid_and_telegram_api.json`](<Windows/thm_curl_with_chatid_and_telegram_api.json>) |
| THM_Detection of Persistence via Registry Run Key with Suspicious JavaScript | [`Windows/thm_detection_of_persistence_via_registry_run_key_with_suspicious_javascript.json`](<Windows/thm_detection_of_persistence_via_registry_run_key_with_suspicious_javascript.json>) |
| THM_Disable Windows Recovery Environment | [`Windows/thm_disable_windows_recovery_environment.json`](<Windows/thm_disable_windows_recovery_environment.json>) |
| THM_Exposed Passwords in Command Lines | [`Windows/thm_exposed_passwords_in_command_lines.json`](<Windows/thm_exposed_passwords_in_command_lines.json>) |
| THM_Masquerading Word Execution from Downloads | [`Windows/thm_masquerading_word_execution_from_downloads.json`](<Windows/thm_masquerading_word_execution_from_downloads.json>) |
| THM_Nailaolocker Mutex "lockv7" Detected | [`Windows/thm_nailaolocker_mutex_lockv7_detected.json`](<Windows/thm_nailaolocker_mutex_lockv7_detected.json>) |
| THM_Nailaolocker Ransomware Log File Created in ProgramData | [`Windows/thm_nailaolocker_ransomware_log_file_created_in_programdata.json`](<Windows/thm_nailaolocker_ransomware_log_file_created_in_programdata.json>) |
| THM_Powershell Encoded Command Executed | [`Windows/thm_powershell_encoded_command_executed.json`](<Windows/thm_powershell_encoded_command_executed.json>) |
| THM_PureRAT C2 Activity via AddInProcess32 | [`Windows/thm_purerat_c2_activity_via_addinprocess32.json`](<Windows/thm_purerat_c2_activity_via_addinprocess32.json>) |
| THM_SOCKS Proxy in Unusual Location | [`Windows/thm_socks_proxy_in_unusual_location.json`](<Windows/thm_socks_proxy_in_unusual_location.json>) |
| THM_Suspicious ICACLS Permissions Deny | [`Windows/thm_suspicious_icacls_permissions_deny.json`](<Windows/thm_suspicious_icacls_permissions_deny.json>) |
| THM_Unsigned sensapi.dll Sideloaded via usysdiag.exe | [`Windows/thm_unsigned_sensapi_dll_sideloaded_via_usysdiag_exe.json`](<Windows/thm_unsigned_sensapi_dll_sideloaded_via_usysdiag_exe.json>) |
| WIN_AD Multiple User Creations | [`Windows/win_ad_multiple_user_creations.json`](<Windows/win_ad_multiple_user_creations.json>) |
| WIN_AD Multiple User Creations Sailpoint | [`Windows/win_ad_multiple_user_creations_sailpoint.json`](<Windows/win_ad_multiple_user_creations_sailpoint.json>) |
| WIN_AD Multiple User Creations Sailpoint Error | [`Windows/win_ad_multiple_user_creations_sailpoint_error.json`](<Windows/win_ad_multiple_user_creations_sailpoint_error.json>) |
| WIN_AD Multiple User Deletions | [`Windows/win_ad_multiple_user_deletions.json`](<Windows/win_ad_multiple_user_deletions.json>) |
| WIN_AD Multiple Users Disabled | [`Windows/win_ad_multiple_users_disabled.json`](<Windows/win_ad_multiple_users_disabled.json>) |
| WIN_Disable UAC Registry Change | [`Windows/win_disable_uac_registry_change.json`](<Windows/win_disable_uac_registry_change.json>) |
| WIN_Domain Reconnaissance via Net Command Burst | [`Windows/win_domain_reconnaissance_via_net_command_burst.json`](<Windows/win_domain_reconnaissance_via_net_command_burst.json>) |
| WIN_Flag Password Never Expire | [`Windows/win_flag_password_never_expire.json`](<Windows/win_flag_password_never_expire.json>) |
| WIN_GPO Was Created | [`Windows/win_gpo_was_created.json`](<Windows/win_gpo_was_created.json>) |
| WIN_GPO was deleted | [`Windows/win_gpo_was_deleted.json`](<Windows/win_gpo_was_deleted.json>) |
| WIN_GPO Was Modified | [`Windows/win_gpo_was_modified.json`](<Windows/win_gpo_was_modified.json>) |
| WIN_Mass Account Disablement by SailPoint Service Account | [`Windows/win_mass_account_disablement_by_sailpoint_service_account.json`](<Windows/win_mass_account_disablement_by_sailpoint_service_account.json>) |
| WIN_PowerShell Backup & Log Tampering | [`Windows/win_powershell_backup_log_tampering.json`](<Windows/win_powershell_backup_log_tampering.json>) |
| WIN_PowerShell Password Input Window | [`Windows/win_powershell_password_input_window.json`](<Windows/win_powershell_password_input_window.json>) |
| WIN_Process from GitHub Desktop | [`Windows/win_process_from_github_desktop.json`](<Windows/win_process_from_github_desktop.json>) |
| WIN_ShieldBreak Exploitation Behavior | [`Windows/win_shieldbreak_exploitation_behavior.json`](<Windows/win_shieldbreak_exploitation_behavior.json>) |
| WIN_Suspicious Kernel Driver Load from Risky Path | [`Windows/win_suspicious_kernel_driver_load_from_risky_path.json`](<Windows/win_suspicious_kernel_driver_load_from_risky_path.json>) |
| WIN_Suspicious Remote Access Run Key Persistence | [`Windows/win_suspicious_remote_access_run_key_persistence.json`](<Windows/win_suspicious_remote_access_run_key_persistence.json>) |
| WIN_Suspicious Sandboxie DLL Load from Non-Standard Path | [`Windows/win_suspicious_sandboxie_dll_load_from_non_standard_path.json`](<Windows/win_suspicious_sandboxie_dll_load_from_non_standard_path.json>) |
| WIN_VIP Account Disabled | [`Windows/win_vip_account_disabled.json`](<Windows/win_vip_account_disabled.json>) |

### Wiz

| Rule | Import File |
|---|---|
| WIZ - Alerts (automatically generated) | [`Wiz/wiz_alerts_automatically_generated.json`](<Wiz/wiz_alerts_automatically_generated.json>) |

## Rule Format

Each file contains one complete XSIAM correlation object wrapped in a JSON array. The embedded `xql_query` includes a standard header with the rule name, vendor, objective, severity, category, and available MITRE ATT&CK metadata.

## Sanitization

Organization-specific usernames, email addresses, domains, IP addresses, hostnames, cloud resource IDs, internal applications, and personal names are removed or replaced with generic placeholders. Sanitization is designed to preserve the original detection logic.

See [`sanitization_report.md`](sanitization_report.md) for a value-free record of the applied sanitization categories.

## Contributing

- Keep one rule per import JSON file.
- Use lowercase snake case filenames.
- Validate JSON and XQL before submitting changes.
- Never commit credentials, personal data, internal infrastructure identifiers, or customer names.
- Update the manifest, sanitization report, and catalog when adding rules.

## Disclaimer

These rules are community examples provided without warranty. Validate schema compatibility, detection quality, operational impact, and applicable legal or regulatory requirements before production use.
