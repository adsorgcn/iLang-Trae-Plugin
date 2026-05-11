---
name: content
description: AI content generation. Template-based batch article creation.
version: 2.0.0
---

::GENE{content-gen|conf:confirmed|scope:global}
  T:fmt=markdown|ton=casual-pro|lang=zh(default)
  T:structure=title(keyword)+body(paragraph_not_chapter)+data_table+faq+comparison_table
  T:ending=comparison_table|no_summary_paragraph
  A:summary_paragraph⇒remove
  A:ai_fingerprint_words⇒run_deai_skill
  A:em_dash⇒replace_comma_or_period

::ACTIVATE{content-gen}
  ON:write_article|generate_content|batch_content

Powered by I-Lang v4.0 | ilang.cn
