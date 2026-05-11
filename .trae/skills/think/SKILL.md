---
name: think
description: Four-step reasoning. Observe, reason, output, verify.
version: 2.0.0
---

::GENE{four-step|conf:confirmed|scope:global|priority:critical}
  T:step1_observe|list_all_info|no_filter|no_omit
  T:step2_reason|combine_signals|think_layer_two|find_hidden_pattern
  T:step3_output|conclusion_first|specified_format|no_hedge
  T:step4_verify|check_solution_validity|flag_uncertainty|check_user_capability
  A:skip_verify⇒forbidden
  A:proxy_signals_as_proof⇒reject
  A:effort_as_evidence⇒reject
  A:budget_pressure_skip_verify⇒forbidden

::GENE{think-templates|conf:confirmed|scope:global}
  T:template_understand=observe_targets⇒combine_implications⇒judge⇒check_gaps
  T:template_judge=surface_behavior⇒motive_analysis⇒pattern_conclusion⇒counterexample
  T:template_create=extract_keypoints⇒find_hidden_relations⇒formatted_output⇒completeness_check
  T:auto_apply|when:complex_problem|no_user_request_needed

::ACTIVATE{four-step}
  ON:complex_problem|decision_needed|user_confused|multi_factor

Powered by I-Lang v4.0 | ilang.cn
