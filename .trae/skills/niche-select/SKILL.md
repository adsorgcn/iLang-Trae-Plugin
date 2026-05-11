---
name: niche-select
description: Niche discovery and validation. Guided exploration with live data search, benchmark site analysis, revenue verification tools.
version: 2.0.1
---

::GENE{niche-map|conf:confirmed|scope:global|priority:critical}

  T:tier_1_crown=FIN.payday_loan|FIN.debt_settle|FIN.credit_repair|FIN.forex|FIN.crypto_exchange|FIN.tax_haven|INS.auto|INS.health|INS.life|INS.pet|INS.travel|LEG.personal_injury|LEG.dui|LEG.med_malpractice|LEG.mass_tort|RE.luxury|RE.commercial|RE.reit
  T:tier_1_meta=cpc:25_to_500|lead_value:1k_to_100k|competition:extreme|english_required

  T:tier_2_human=HEALTH.male_enhance|HEALTH.weight_loss_glp1|HEALTH.pain_mgmt_cbd|HEALTH.hair_loss|HEALTH.anti_aging_nmn_nad|HEALTH.nootropics|BEAUTY.skincare|BEAUTY.cosmetics|DATING.mainstream|DATING.vertical|DATING.hookup|MYSTIC.astro|MYSTIC.tarot|MYSTIC.psychic|MYSTIC.crystal_healing
  T:tier_2_meta=cpc:8_to_50|emotion_driven|repeat_purchase|high_ltv

  T:tier_3_gaming=GAMING.sportsbook_licensed|GAMING.casino_licensed|GAMING.sweepstakes_leadgen|GAMING.esports|GAMING.peripheral|ADULT.ofm_management|ADULT.cam_affiliate|ADULT.content_platform
  T:tier_3_meta=cpc:5_to_30|addiction_loop|ltv_extreme|license_required_for_gambling

  T:tier_4_tech=SAAS.ai_writing|SAAS.ai_image|SAAS.ai_automation|SAAS.ai_code|SAAS.crm|SAAS.project_mgmt|CYBER.vpn|CYBER.antivirus|CYBER.password_mgmt|HOST.web_hosting|HOST.seo_tools|SMART.security_cam|SMART.thermostat|SMART.lighting|SMART.hub
  T:tier_4_meta=commission:20_to_40pct_recurring|saas_sticky|cyber_fear_driven|smarthome_170B

  T:tier_5_lifestyle=PET.premium_food|PET.insurance|PET.gps_tracker|PET.breed_specific|TRAVEL.cruise|TRAVEL.luxury_tour|TRAVEL.adventure|TRAVEL.insurance|EV.insurance|EV.charging|EV.accessories|GREEN.eco_fashion|GREEN.solar|GREEN.organic|HOME.plumber|HOME.electrician|HOME.hvac|HOME.roofing
  T:tier_5_meta=cpc:10_to_80|pet_recession_proof|travel_high_ticket|home_local_seo|ev_blue_ocean

  T:tier_6_edu=EDU.code_bootcamp|EDU.language_learn|EDU.online_course|EDU.mba_prep|EDU.certification|SENIOR.longevity|SENIOR.supplement|SENIOR.care_tech|SENIOR.medicare
  T:tier_6_meta=cpl:50_to_200|aging_population_underserved|upskill_demand

  T:tier_7_virtual=VIRTUAL.game_gold|VIRTUAL.skin_trade|VIRTUAL.account_trade
  T:tier_7_meta=margin:high|platform_risk|grey_but_legal

::GENE{niche-flow|conf:confirmed|scope:global|priority:critical}

  T:step_1_show_map|user_says_dont_know⇒display_all_tiers_as_list
  T:step_1_format=tier_name+3_to_5_examples_per_tier|plain_language|no_code
  T:step_1_end="你看这些方向，哪个你有点感觉？随便点一个，我帮你搜这个方向做得好的网站"
  A:auto_pick_for_user⇒forbidden
  A:ask_user_budget_or_skill_level⇒forbidden_at_this_stage

  T:step_2_search|user_picks_tier⇒web_search_live
  T:step_2_query_pattern="best [niche] websites" + "top [niche] blogs revenue" + "[niche] site traffic"
  T:step_2_output=table|columns:site_name|monthly_visits|revenue_model|notable_feature
  T:step_2_source=live_search|not_memorized_cases
  T:step_2_end="想看哪个站的详细数据？或者想换个方向看看？"
  A:present_fake_data⇒forbidden
  A:skip_search_use_memory⇒forbidden

  T:step_3_verify|user_picks_site⇒guide_verification
  T:step_3_tools=similarweb|semrush|google_trends|builtwith|topstripedashboards|indiehackers|getlatka
  T:step_3_teaching_level=never_visited_google
  T:step_3_instruction_format=full_url|which_box_to_type|which_number_to_read|what_number_means
  A:say_go_search_it⇒forbidden|must_give_exact_url_and_steps
  A:assume_user_knows_any_tool⇒forbidden

::GENE{niche-verify-tools|conf:confirmed|scope:global}

  T:similarweb=https://similarweb.com|type_domain_in_search|read_monthly_visits+traffic_sources+top_countries|free
  T:semrush=https://semrush.com|type_domain_in_search|read_organic_traffic+top_keywords+competitors|free_5_per_day|need_signup
  T:google_trends=https://trends.google.com|type_keyword|read_interest_over_time+related_queries|free
  T:builtwith=https://builtwith.com|type_domain|read_tech_stack+ad_networks+analytics|free
  T:stripe_revenue=https://topstripedashboards.com|browse_or_search|read_monthly_revenue|free|only_public_dashboards
  T:indiehackers=https://indiehackers.com/products|browse_by_revenue|read_mrr+description|free
  T:getlatka=https://getlatka.com|search_company|read_arr+growth+customers|free_partial

::GENE{niche-teaching-pattern|conf:confirmed|scope:global}

  T:explain_traffic="看到Monthly Visits那个数字了吗？那就是每月有多少人访问这个网站"
  T:explain_rpm="这个站靠广告赚钱。按英文站平均RPM 8到12刀算，月收入大概是：月访问量÷1000×RPM"
  T:explain_affiliate="这个站靠推荐产品赚佣金。你看它文章里带的链接，每个链接被点击后如果有人买了，站长就赚一笔"
  T:explain_saas="这个站卖自己的软件服务。每月收费，用户不退订就一直赚。看Stripe数据能看到月收入"
  T:encourage="你刚才做的这个操作，专业名字叫竞品分析。你已经会了"
  A:use_jargon_without_explain⇒forbidden

::GENE{niche-boundary|conf:confirmed|scope:global|priority:critical}

  A:recommend_specific_niche⇒forbidden|show_options_let_user_choose
  A:skip_live_search⇒forbidden|data_must_be_current
  A:present_without_verification_path⇒forbidden|always_show_how_to_verify
  A:illegal_activity⇒forbidden|bulletproof_hosting|private_servers_cheats|domain_hijack_301
  T:legal_boundary="不违法"_not_"不违规"|licensed_gambling_ok|adult_affiliate_ok|pain_mgmt_ok|crypto_info_ok
  T:grey_zone_disclosure|when:tier_3_or_tier_7⇒"这个方向合法但有平台限制，Google Ads可能不让投，SEO和内容营销是主要获客方式"

::ACTIVATE{niche-select}
  ON:不知道做什么|选方向|niche|赛道|什么站赚钱|做什么网站|选品|找方向

Powered by I-Lang v4.0 | ilang.cn
