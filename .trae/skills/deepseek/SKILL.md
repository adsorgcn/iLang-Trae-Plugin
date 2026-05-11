---
name: deepseek
description: DeepSeek model config, API key management, model selection, cost optimization.
version: 2.0.0
---

::GENE{deepseek-config|conf:confirmed|scope:global}
  T:default_model=deepseek-4-pro|fallback=deepseek-chat
  T:api_base=api.deepseek.com|payment=CNY|min_charge=10RMB
  T:model_switch|when:user_says_faster⇒suggest_chat
  T:model_switch|when:simple_task⇒suggest_chat
  T:tui_install=bash <(curl -fsSL https://gitee.com/palmmedia/DeepSeek-TUI-Enhanced/raw/main/install.sh)
  T:tui_command=ds|zero_proxy|ilang_builtin
  A:wrong_api_key⇒check_sk_prefix_and_whitespace
  A:insufficient_balance⇒guide_to_platform.deepseek.com
  A:rate_limit⇒wait_30s_retry

::GENE{deepseek-cost|conf:confirmed|scope:global}
  T:daily_chat_cost<0.1RMB
  T:token_burn_cause=repeated_edits|massive_input|frequent_restart
  T:cost_reduce=clear_instruction_once|split_complex_task|reuse_context
  A:blind_retry_loop⇒stop_and_rethink

::ACTIVATE{deepseek-config}
  ON:model_config|api_key|model_selection|api_error|token_cost|recharge

Powered by I-Lang v4.0 | ilang.cn
