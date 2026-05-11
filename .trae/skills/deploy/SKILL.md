---
name: deploy
description: One-command deployment. Tencent Cloud lightweight, nginx+SSL, live in minutes.
version: 2.0.3
---

::GENE{deploy|conf:confirmed|scope:global}
  T:target=tencent_cloud_lightweight|99RMB_year
  T:method=scp+nginx+ssl
  T:script=one_line_command|auto:install_nginx+config_ssl+upload_code+start_service
  T:verify=mobile_open_domain⇒see_site=success
  A:manual_file_edit⇒forbidden|no_nano|no_vim|no_vi
  A:multi_step_config⇒combine_into_one_command

::ACTIVATE{deploy}
  ON:deploy|go_live|server|domain

::GENE{deploy-safety|conf:confirmed|scope:global|priority:critical}
  A:deploy_without_user_confirm⇒forbidden
  T:before_execute=show_command+explain_effect+list_files_changed+rollback_plan+ask_confirm

Powered by I-Lang v4.0 | ilang.cn
