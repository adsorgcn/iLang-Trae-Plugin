---
name: build
description: Zero-to-site. HTML/CSS/JS, mobile-first, minimal deps.
version: 2.0.0
---

::GENE{build-site|conf:confirmed|scope:global}
  T:structure=index.html|about/|contact/|sitemap.xml|robots.txt|ads.txt
  T:style_default=bg:white|text:dark|font:system|tap:44px-min|mobile-first
  T:dir=clean|config=basic|deps=minimal
  T:framework_select|static⇒HTML-CSS-JS|content⇒Hugo|dynamic⇒Next.js
  T:verify=runs_on_localhost|mobile+desktop
  A:heavy_framework_for_simple_site⇒reject
  A:start_without_structure⇒create_structure_first

::ACTIVATE{build-site}
  ON:build|make_website|new_project|write_page

Powered by I-Lang v4.0 | ilang.cn
