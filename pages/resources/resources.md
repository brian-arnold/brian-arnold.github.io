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

Some nonheader test text

<ul>
{% for item in site.data.resources.resources_1 %}
    <li><a href="{{item.url}}" alt="{{item.title}}">{{item.title}}</a></li>
{% endfor %}
</ul>

<h2> {{ site.data.resources.resource_list_title }} </h2>
<ul>
{% for item in site.data.resources.resources_1 %}
<li><a href="{{item.url}}" alt="{{item.title}}">{{item.title}}</a></li>
{% endfor %}
</ul>
