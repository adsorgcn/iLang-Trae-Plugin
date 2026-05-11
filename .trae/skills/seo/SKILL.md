---
name: seo
description: Full SEO pipeline. Meta, JSON-LD, sitemap, pSEO, llms.txt, title optimization, GSC.
version: 2.0.0
---

::GENE{seo-meta|conf:confirmed|scope:global}
  T:title=keyword_front+brand_back
  T:description=under_150chars|contains_action_verb
  T:og_tags=og:title+og:description+og:image|required

::GENE{seo-schema|conf:confirmed|scope:global}
  T:jsonld_required=Organization+WebSite+Article+BreadcrumbList+FAQPage
  T:faqpage=min_3_per_page|target_longtail_intent
  T:product_page⇒add_Product_schema
  T:tutorial_page⇒add_HowTo_schema

::GENE{seo-sitemap|conf:confirmed|scope:global}
  T:auto_generate|submit_gsc
  T:multilang⇒per_language_sitemap
  T:gsc_submit=within_24h_of_launch
  T:manual_index=homepage+category_pages

::GENE{seo-pseo|conf:confirmed|scope:global}
  T:user_question=H1=longtail_keyword
  T:each_question⇒independent_page
  T:data:hotelcorporatecodes=20_presets⇒615+_codes

::GENE{seo-title|conf:confirmed|scope:global}
  T:pattern=function_word_front+brand_back
  T:example="酒店优惠码查询 | Brand"|not:"Brand | 酒店优惠码查询"

::GENE{seo-hreflang|conf:confirmed|scope:global}
  T:every_page_head⇒hreflang_all_versions
  T:multiplier=1lang×10pages=10URL|7lang=70URL|exposure×7

::GENE{seo-adstxt|conf:confirmed|scope:global|priority:critical}
  T:prefix=pub-|never:ca-
  A:ca_prefix⇒strip_and_warn

::GENE{seo-llmstxt|conf:confirmed|scope:global}
  T:root_dir=llms.txt|allow=Googlebot,GPTBot,ClaudeBot
  T:benefit=AI_search_citation=free_traffic

::ACTIVATE{seo}
  ON:seo|ranking|keyword|indexing|traffic|search_console

Powered by I-Lang v4.0 | ilang.cn
