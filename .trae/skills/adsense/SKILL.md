---
name: adsense
description: Google AdSense full operations. Application, ad placement, RPM optimization, ban protection, multi-site, revenue diagnostics.
version: 2.0.0
---

::GENE{adsense-apply|conf:confirmed|scope:global}
  T:content_min=20_original_articles|1500words_each|real_value
  T:structure=clear_nav+about+contact+privacy_policy
  T:tech=https_required|mobile_responsive|load_under_3s
  T:wait=1_to_4_weeks|rejected⇒fix_and_reapply|unlimited_attempts

::GENE{adsense-adstxt|conf:confirmed|scope:global|priority:critical}
  T:prefix=pub-|never:ca-
  T:scope=every_site|no_exception
  A:ca_prefix⇒strip_immediately

::GENE{adsense-placement|conf:confirmed|scope:global}
  T:position_1=after_first_paragraph|ctr:highest|required
  T:position_2=mid_article|ctr:medium|for_long_articles_1to2
  T:position_3=sidebar|ctr:low|desktop_only|hide_mobile
  T:position_4=end_of_article|ctr:medium_low|one
  T:max_per_page=3to4|more⇒hurts_ux_and_rpm
  A:over_4_ads_per_page⇒reduce

::GENE{adsense-rpm|conf:confirmed|scope:global}
  T:lang_factor|en:12usd|ja:8to10|zh:3to5
  T:device_factor|desktop:3x_mobile
  T:https_migration⇒rpm+20to30pct
  T:speed_6s_to_2s⇒rpm+75pct
  T:high_value_niche=finance|insurance|legal|rpm:15to30
  T:low_value_niche=entertainment|news|rpm:1to3

::GENE{adsense-content-strategy|conf:confirmed|scope:global}
  T:golden_ratio=70pct_longtail+30pct_trending
  T:longtail_length=3000words+|avg_earning_article=3200words
  T:article_ending=comparison_table|no_summary
  A:summary_paragraph⇒cut

::GENE{adsense-cpc-cpm|conf:confirmed|scope:global}
  T:cpc|fits:high_intent(review|comparison|tutorial)|user_clicks
  T:cpm|fits:high_traffic_low_intent(news|entertainment)|impression_based
  T:default=cpc|switch_cpm|when:daily_pv>50k_and_ctr<1pct

::GENE{adsense-multisite|conf:confirmed|scope:global}
  T:phase_1=1to3_sites|focus:first_site_to_500usd_month
  T:phase_2=5to10_sites|diversify_niche_spread_risk
  T:phase_3=10to50_sites|ai_batch_content+management_system
  T:phase_4=50plus|team_or_full_automation|target:50k_usd_month
  T:one_account_multi_site|no_multi_account_needed

::GENE{adsense-ban-protection|conf:confirmed|scope:global|priority:critical}
  T:rule_1=no_bought_traffic|no_click_exchange|no_mutual_clicking
  T:rule_2=no_click_bait_copy|no:"click_here_to_support_me"
  T:rule_3=sufficient_spacing_between_ad_and_content|no_misclick
  T:rule_4=no_ads_in_popups
  T:rule_5=suspicious_ip_burst⇒block_immediately
  A:any_invalid_click_pattern⇒investigate_and_block

::GENE{adsense-diagnostics|conf:confirmed|scope:global}
  T:rpm_drop⇒check_algo_update+search_console_ranking
  T:ctr_drop⇒check_ad_placement+mobile_display
  T:seasonal=Q4_highest(advertiser_budget)|Q1_lowest
  T:traffic_crash⇒diagnose_algo_vs_technical|tech:fix_48h|algo:content_quality_push

::GENE{adsense-multilang|conf:confirmed|scope:global}
  T:en_rpm_highest|ja_second|zh_lowest
  T:7lang_same_site⇒revenue_3to5x
  T:adstxt=one_per_domain|not_per_language

::GENE{adsense-ab-test|conf:confirmed|scope:global}
  T:tool=adsense_builtin_experiments
  T:test_vars=ad_size|ad_type(display|text|native)|ad_count
  T:rule=one_variable_at_a_time|run_2_weeks

::GENE{adsense-tool-site|conf:confirmed|scope:global}
  T:user_dwell_time=short|ad_near_result
  T:typical_rpm=5to8usd|pdf|image|converter_tools
  T:priority=stable_function>rich_content

::ACTIVATE{adsense}
  ON:adsense|ad_revenue|rpm|ctr|ad_placement|banned|apply_adsense

Powered by I-Lang v4.0 | ilang.cn
