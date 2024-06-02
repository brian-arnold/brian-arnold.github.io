---
layout: article
titles:
  # @start locale config
  en      : &EN       About (under construction 6/2/24)
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN
  zh-Hans : &ZH_HANS  关于
  zh      : *ZH_HANS
  zh-CN   : *ZH_HANS
  zh-SG   : *ZH_HANS
  zh-Hant : &ZH_HANT  關於
  zh-TW   : *ZH_HANT
  zh-HK   : *ZH_HANT
  ko      : &KO       소개
  ko-KR   : *KO
  fr      : &FR       À propos
  fr-BE   : *FR
  fr-CA   : *FR
  fr-CH   : *FR
  fr-FR   : *FR
  fr-LU   : *FR
  # @end locale config
key: page-about
permalink: /about/
aside:
    toc: true
---

<img align="right" src="/pages/about/headshot.jpg" style="width:150px;height:150px;">

I'm a data scientist at Princeton University, formerly in Computer Science and currently in Ecology and Evolutionary Biology. 

My interests and expertise are in software engineering, statistics, machine learning, and analyzing large datasets ***carefully***, using numerous sanity checks such as data visualizations and software tests. 


As a departmental data scientist, I primarily do collaborative research, rotating among labs and queueing projects via networking within the department. Additionally, I 

- teach workshops
- mentor individual students or postdocs
- serve as consultant
- develop computational workflows that enable or accelerate several projects


I am also affiliated with the [Center for Statistics and Machine Learning](https://csml.princeton.edu/), which creates inter-departmental connections between scientists at Princeton.


# Highlights

Here I highlight my technical contributions to selected projects, which typically involve collaborations in which I take the lead on a modular component. These contributions involve applying my skills I mentioned above to various data modalities including 3D movies of neural activity, spatial transcriptomics, and whole-genome sequencing (WGS).

- [3D movie analysis](https://github.com/brian-arnold/whole_AL_segmentation): image segmentation to decode neural activity in the mosquito antennal lobe (AL)
  - created python workflows to measure activity of the entire AL
  - discovered technical batch effects and used the experimental design to correct them via custom statistical models
  - segmented individual glomeruli (clusters of nerve endings) via nonnegative matrix factorization (Figure)

<img align="left" src="/pages/about/raw.gif" style="width:400px;height:400px;">
<img align="right" src="/pages/about/timetrace.gif" style="width:400px;height:400px;">



- As a former data scientist in Princeton's Computer Science department, I [discuss](https://csml.princeton.edu/news/videos-datax-data-scientists-discuss-their-role-and-impact-research) my role in the larger academic community.

- [Here](https://web.inf.ed.ac.uk/cdt/biomedical-ai/events/events-past#uoe_featurebox_e98a5cc58bf69187c764e7147d3f1d965:~:text=Brian%20Arnold%2C%20Senior%20Data%20Scientist%2C%20Princeton%20University.) is a talk of my work on "Learning mixtures and DNA copy-numbers from bulk sequencing of tumor samples" 

- I was an invited guest on the *Nice Genes!* [podcast](https://podcasts.apple.com/ca/podcast/nodding-our-tusks-to-heroic-mutations/id1622851335?i=1000574742314) for our work on tuskless African elephants.

# Background

For the past 5 years, I have worked as a staff scientist in academia. 

Two of those years I spent at [Harvard Informatics](https://informatics.fas.harvard.edu/pages/about.html), creating workflows for analyzing genomic datasets, researching with faculty, and  teaching introductory workshops on bioinformatics. 

I then moved to Princeton University where I spent 3 years as a biomedical data scientist as part of the [DataX](https://csml.princeton.edu/datax-home) initiative. At Princeton, I worked in the Computer Science department doing research on cancer genomics and teaching workshops on software engineering and machine learning. Through these experiences, I learned to think about data in more general ways beyond my specialization in genomics. I now have a broad interest in algorithms, statistics, and machine learning, and I'm interested in applying these skills to ***any*** kind of data that could be useful to address important questions. However, while data science skills are incredibly transferable, it's always best to work with someone who has domain expertise in the data you're analyzing!
