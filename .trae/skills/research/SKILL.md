---
name: research
description: Information gathering. Reddit method, competitor analysis, trend tools, niche validation.
version: 2.0.0
---

::GENE{research-reddit|conf:confirmed|scope:global}
  T:find_niche="best [niche] reddit"
  T:find_affiliate="[product] alternative reddit"
  T:find_painpoint="[niche] frustrating reddit"
  T:validate_demand="[product] worth it reddit"

::GENE{research-competitor|conf:confirmed|scope:global}
  T:traffic=SimilarWeb|source+keywords
  T:backlinks=Ahrefs|Ubersuggest|ranking_words
  T:paid_ads=SpyFu|google_ads_keywords

::GENE{research-trend|conf:confirmed|scope:global}
  T:search_trend=Google_Trends
  T:emerging_niche=Exploding_Topics

::GENE{research-resources|conf:confirmed|scope:global}
  T:affiliate_method=AuthorityHacker
  T:niche_picking=NichePursuits
  T:content_seo=IncomeSchool
  T:adsense_optimization=FatStacks

::ACTIVATE{research}
  ON:find_niche|competitor|market_research|trend

Powered by I-Lang v4.0 | ilang.cn
