---
layout: article
titles:
  # @start locale config
  en      : &EN       About
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

<img src="/pages/about/headshot.jpg" style="width:150px; height:150px; float: right; margin-left: 20px; margin-bottom: 10px;">

I'm a data scientist at Princeton University, formerly in Computer Science and currently in Ecology and Evolutionary Biology. I'm also affiliated with the [Center for Statistics and Machine Learning](https://csml.princeton.edu/).

My interests and expertise are in bioinformatics, software engineering, machine learning, and analyzing large-scale datasets using extensive visualizations. 

As a senior data scientist, I primarily collaborate as an independent contributor, rotating among labs (~4 month terms to maximize diversity) and queueing projects via networking within the department. Additionally, I:

- develop computational workflows that enable or accelerate several projects
- mentor individual students or postdocs
- teach workshops
- serve as consultant


# Highlights

Here, I highlight my technical contributions to selected collaborations in which I take the lead on a modular component. These contributions involve applying my skills mentioned above to various data modalities including spatial transcriptomics, 3D movies of neural activity, and whole-genome sequencing (WGS).


- [GASTON](https://www.biorxiv.org/content/10.1101/2023.10.10.561757v1): deep neural network to segment domains and study continuous variation in gene expression from spatial transcriptomics data
  - refactored code into python package to run at scale and optimize neural network architecture
  - feature-ized histology images (H&E stained) to facilitate tissue segmentation
  - analyzed several colorectal cancer datasets to characterize metabolic gradients and the tumor microenvironment


<!-- Ensure there is a clear separation between HTML and any Markdown elements -->
<div style="text-align: center;">
    <img src="/pages/about/GASTON.png" alt="GASTON" style="width: 800px;">
    <p class="image-caption">(A) H&E stain of a 10x Genomics Visium colorectal tumor sample. (B) Spatial domains learned by GASTON. Domains 1 and 2 are labeled as tumor and tumor-adjacent stroma, respectively, based on the histology image in (A). (C) Spatial gradients learned by GASTON show directions of maximum gene expression changes in tumor and tumor-adjacent stromal domains.</p>
</div>
<!-- Ensure there is a clear separation between HTML and any Markdown elements -->


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
    font-size: 12px;
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



- [HATCHet2](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-024-03267-x): copy-number calling (amplifications/deletions of DNA) for tumor WGS data
    - wrote several modules to phase genotypes into haplotypes using the 1000GP reference panel
    - Docker-ized software for cloud computing on GCP and AWS
    - analyzed large datasets in collaboration with the [Genomic Data Analysis Network](https://docs.gdc.cancer.gov/Encyclopedia/pages/Genomic_Data_Analysis_Network/)
    - gave virtual invited [talk](https://web.inf.ed.ac.uk/cdt/biomedical-ai/events/events-past#uoe_featurebox_e98a5cc58bf69187c764e7147d3f1d965:~:text=Brian%20Arnold%2C%20Senior%20Data%20Scientist%2C%20Princeton%20University.) at University of Edinburgh's biomedical AI seminar


<!-- Ensure there is a clear separation between HTML and any Markdown elements -->
<div style="text-align: center;">
    <img src="/pages/about/HATCHET.png" alt="HATCHET" style="width: 500px;">
    <p class="image-caption">From tumor WGS data, HATCHet2 extracts 2 features that are correlated with copy number: the fractional copy number (rescaled from read depth) and the mirrored B-allele frequency (BAF). For normal diploids, these values should be 2 and 0.5, respectively, which we observe for some genomic regions in this sample (orange dots). However, most tumors exhibit stiking variation in copy-number along the genome. </p>
</div>
<!-- Ensure there is a clear separation between HTML and any Markdown elements -->


- [snpArcher](https://academic.oup.com/mbe/article/41/1/msad270/7466717): workflow to automate variant calling in nonmodel organisms
    - authored original snakemake code and supplementary algorithms to massively parallelize two variant callers


- [Tuskless African elephants](https://www.science.org/doi/10.1126/science.abe7389): poaching drives evolution of tusklessness, a female-specific trait encoded by a male-lethal mutation
    - contributed all genomic analyses as co-first author
    - led to over 411 news stories from 301 media outlets
    - invited guest on the *Nice Genes!* [podcast](https://podcasts.apple.com/ca/podcast/nodding-our-tusks-to-heroic-mutations/id1622851335?i=1000574742314)
