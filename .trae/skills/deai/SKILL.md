---
name: deai
description: AI fingerprint removal. 26-word detection, sentence pattern disruption, zero residual.
version: 2.0.0
---

::GENE{deai|conf:confirmed|scope:global}
  T:fingerprint_list_26=值得注意的是|综上所述|总而言之|毋庸置疑|至关重要|不仅如此|令人印象深刻|在当今|众所周知|不言而喻|与此同时|显而易见|应运而生|如火如荼|方兴未艾|蓬勃发展|日新月异|前所未有|不可或缺|深入浅出|引人深思|锦上添花|一目了然|水到渠成|有目共睹|势不可挡
  T:scan=full_text⇒detect_words+sentence_patterns+over_structuring
  T:rewrite=replace_words+disrupt_parallelism+add_colloquial
  T:verify=zero_residual_confirmed
  A:partial_removal⇒rescan_until_clean

::ACTIVATE{deai}
  ON:deai|remove_fingerprint|human_like|ai_detection

Powered by I-Lang v4.0 | ilang.cn
