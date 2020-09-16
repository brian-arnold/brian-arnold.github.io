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

<!--- Personal Notes, taken from _data/resources.yml --->

<h2> {{ site.data.resources.resource_notes_title }} </h2>
<ul>
{% for item in site.data.resources.resources_notes %}
<li><a href="{{item.url}}" alt="{{item.title}}">{{item.title}}</a></li>
{% endfor %}
</ul>


<!--- Free Online Classes, taken from _data/resources.yml --->

<h2> {{ site.data.resources.resource_classes_title }} </h2>
When your job involves staring at text all day (like mine), it's relaxing to learn by just listening. 
<ul>
{% for item in site.data.resources.resources_classes %}
<li><a href="{{item.url}}" alt="{{item.title}}">{{item.title}}</a></li>
{% endfor %}
</ul>
