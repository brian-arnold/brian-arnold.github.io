---
layout: article
key: page-resources-bioinfoTools
permalink: /resources/datascience/
---

Back to [Resources](/resources/)

# Key concepts in Data Science

This page contains brief explanations of elementary but important concepts in Data Science (statistical analysis and interpretation). While these concepts are discussed many placesr, for pedagogical reasons and for my own memory, I like creating (or collecting from elsewhere) exceptionally simple, clear explanations with visualizations that can immensely help understanding. When I explain myself I try to provide code so that you can verify everything yourself!


- [coefficient of determination](/resources/datascience/coeffDeter/)
- [regression to the mean](/resources/datascience/regressionToMean/)
- model (over)fitting, training, and testing; two lectures, [part 1](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0002-introduction-to-computational-thinking-and-data-science-fall-2016/lecture-videos/lecture-9-understanding-experimental-data/) and [part 2](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0002-introduction-to-computational-thinking-and-data-science-fall-2016/lecture-videos/lecture-10-understanding-experimental-data-cont./), from 6.0002 MIT class
    - *cross validation*: train model with one dataset, test with another; assess sensitivity (recall) and specificity (precision), positive and predictive values, accuracy, or composite of these with F1-score
- intro to machine learning
    - infer process that generated training data or extract underlying structure of data 
        - *supervised learning*: given training data with features (simple summaries, e.g. weight, limb length) and group labels (e.g. predator, prey), infer function that generated labels; [MIT 6.0002 lect. 13](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0002-introduction-to-computational-thinking-and-data-science-fall-2016/lecture-videos/lecture-13-classification/)
            - regression, *classification* to predict label given features
        - *unsupervised learning*: given training data with features and ***no*** group labels, cluster data into groups; [MIT 6.0002 lect. 12](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-0002-introduction-to-computational-thinking-and-data-science-fall-2016/lecture-videos/lecture-12-clustering/)
            - hierarchical clustering, K-means clustering
    - use inference/structure to predict test data (to assess model) and then future data 

