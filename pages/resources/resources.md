---
layout: article
titles:
  # @start locale config
  en      : &EN       Resources
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN
  zh-Hans : &ZH_HANS  资源资源
  zh      : *ZH_HANS
  zh-CN   : *ZH_HANS
  zh-SG   : *ZH_HANS
  zh-Hant : &ZH_HANT  資源資源 
  zh-TW   : *ZH_HANT
  zh-HK   : *ZH_HANT
  ko      : &KO       자원 
  ko-KR   : *KO
  fr      : &FR       Ressourcess
  fr-BE   : *FR
  fr-CA   : *FR
  fr-CH   : *FR
  fr-FR   : *FR
  fr-LU   : *FR
  # @end locale config
key: page-resources
permalink: /resources/
---

<br />

Under construction.

- [Foundational skills for data science](/resources/datascience/)
  - content/links to learn coding and software management skills useful for any project involving data
- [Learn about Machine Learning!](/resources/machinelearning/)
  - textbook recommendations
- [Graphic design](/resources/graphicDesign/)
  - links for making beautiful figures
- [Managing code with GitHub (templates)](/resources/gitHub/)

<!--- OLD CODE, CYCLES THROUGH _data/resources.yml
<h2> {{ site.data.resources.resource_notes_title }} </h2>
<ul>
{% for item in site.data.resources.resources_notes %}
<li><a href="{{item.url}}" alt="{{item.title}}">{{item.title}}</a></li>
{% endfor %}
</ul>
 --->

