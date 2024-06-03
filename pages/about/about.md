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

Here I highlight my technical contributions to selected collaborations in which I take the lead on a modular component. These contributions involve applying my skills I mentioned above to various data modalities including 3D movies of neural activity, spatial transcriptomics, and whole-genome sequencing (WGS).

- [3D movie analysis](https://github.com/brian-arnold/whole_AL_segmentation): image segmentation to decode neural activity in the mosquito antennal lobe (AL)
  - created python workflows to measure activity of the entire AL
  - discovered technical batch effects and used the experimental design to correct them via custom statistical models
  - segmented individual glomeruli (clusters of nerve endings) within the AL via nonnegative matrix factorization (NMF)


<!-- Ensure there is a clear separation between HTML and any Markdown elements -->
<style>
.container {
    display: flex;
    justify-content: center;  /* Align items to the center horizontally */
    align-items: flex-start;  /* Align items to the top vertically */
    flex-wrap: nowrap;  /* Prevents the items from wrapping */
}

.image-container {
    width: 400px; /* Updated width according to your new image size */
    text-align: center;
    margin: 10px;  /* Adds margin to create some space between the image containers */
}

.image-container img {
    display: block;
    width: 100%;  /* Image will scale with the container */
    height: auto;
}

.image-caption {
    color: #666;
    font-style: italic;
    margin-top: 8px;
}
</style>


<div class="container">  <!-- Parent container to hold both image containers -->
    <div class="image-container">
        <img src="/pages/about/raw.gif" alt="Neural activity visualization">
        <p class="image-caption">2D max projection of raw data from the AL of a mosquito that recieved an odor puff. These data are noisy even after median filtering.</p>
    </div>

    <div class="image-container">
        <img src="/pages/about/timetrace.gif"  alt="Neural activity visualization">
        <p class="image-caption">Custom visualization of NMF segmentation shows spatial positions and activity traces of glomeruli.</p>
    </div>
</div>
<!-- Ensure there is a clear separation between HTML and any Markdown elements -->


- [GASTON](https://www.biorxiv.org/content/10.1101/2023.10.10.561757v1): deep neural network to segment tissues from spatial transcriptomics data
  - refactored code into python package to run at scale and optimize neural network architecture
  - feature-ized histology images (H&E stained) to facilitate tissue segmentation
  - analyzed several colorectal cancer datasets to characterize tumor microenvironments


<!-- Ensure there is a clear separation between HTML and any Markdown elements -->
<div style="text-align: center;">
    <img src="/pages/about/GASTON.png" alt="GASTON" style="width: 800px;">
    <p class="image-caption">(A) H&E stain of a 10x Genomics Visium colorectal tumor sample. (B) Spatial domains learned by GASTON. Domains 1 and 2 are labeled as tumor and tumor-adjacent stroma, respectively, based on the histology image in (A). (C) Spatial gradients learned by GASTON show directions of maximum gene expression changes in tumor and tumor-adjacent stromal domains.</p>
</div>
<!-- Ensure there is a clear separation between HTML and any Markdown elements -->


- [HATCHet2](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-024-03267-x): copy-number calling for tumor WGS data
    - wrote several [modules](https://github.com/raphael-group/hatchet/blob/master/src/hatchet/utils/phase_snps.py) to phase genotypes into haplotypes using the 1000GP reference panel
    - Docker-ized software for cloud computing on GCP and AWS
    - analyzed large datasets in collaboration with the [Genomic Data Analysis Network](https://docs.gdc.cancer.gov/Encyclopedia/pages/Genomic_Data_Analysis_Network/)
    - gave virtual invited [talk](https://web.inf.ed.ac.uk/cdt/biomedical-ai/events/events-past#uoe_featurebox_e98a5cc58bf69187c764e7147d3f1d965:~:text=Brian%20Arnold%2C%20Senior%20Data%20Scientist%2C%20Princeton%20University.) at University of Edinburgh's biomedical AI seminar


- [snpArcher](https://academic.oup.com/mbe/article/41/1/msad270/7466717): workflow to automate variant calling in nonmodel organisms
    - authored original snakemake code and supplementary algorithms to massively parallelize two variant callers


- [Tuskless African elephants](https://www.science.org/doi/10.1126/science.abe7389): poaching drives evolution of tusklessness, a female-specific trait encoded by a male-lethal mutation
    - contributed all genomic analyses as co-first author
    - led to over 411 news stories from 301 media outlets
    - invited guest on the *Nice Genes!* [podcast](https://podcasts.apple.com/ca/podcast/nodding-our-tusks-to-heroic-mutations/id1622851335?i=1000574742314)


# Background

For the past 6 years, I have worked as a staff scientist in academia. 

Two of those years I spent at [Harvard Informatics](https://informatics.fas.harvard.edu/pages/about.html), creating workflows for analyzing genomic datasets, researching with faculty, and teaching introductory workshops on bioinformatics. 

I then moved to Princeton University where I spent 3 years as a biomedical data scientist as part of the [DataX](https://csml.princeton.edu/datax-home) initiative. At Princeton, I worked in the Computer Science department doing research on cancer genomics and teaching workshops on software engineering and machine learning. Through these experiences, I learned to think about data in more general ways beyond my specialization in genomics. 

I now have a broad interest in algorithms, statistics, and machine learning. As a departmental data scientist in Ecology and Evolutionary Biology, I'm interested in applying these skills to ***any*** kind of data that could be useful to address interesting questions. 
