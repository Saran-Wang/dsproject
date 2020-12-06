---
author-meta:
- Shiyuan Wang
- Weiqi Ni
- Gemma Clark
- Xueao Li
bibliography:
- content/manual-references.json
date-meta: '2020-12-06'
header-includes: '<!--

  Manubot generated metadata rendered from header-includes-template.html.

  Suggest improvements at https://github.com/manubot/manubot/blob/master/manubot/process/header-includes-template.html

  -->

  <meta name="dc.format" content="text/html" />

  <meta name="dc.title" content="Project 5 Pollution Vision" />

  <meta name="citation_title" content="Project 5 Pollution Vision" />

  <meta property="og:title" content="Project 5 Pollution Vision" />

  <meta property="twitter:title" content="Project 5 Pollution Vision" />

  <meta name="dc.date" content="2020-12-06" />

  <meta name="citation_publication_date" content="2020-12-06" />

  <meta name="dc.language" content="en-US" />

  <meta name="citation_language" content="en-US" />

  <meta name="dc.relation.ispartof" content="Manubot" />

  <meta name="dc.publisher" content="Manubot" />

  <meta name="citation_journal_title" content="Manubot" />

  <meta name="citation_technical_report_institution" content="Manubot" />

  <meta name="citation_author" content="Shiyuan Wang" />

  <meta name="citation_author_institution" content="Department of Civil and Environmental, University of Illinois" />

  <meta name="citation_author" content="Weiqi Ni" />

  <meta name="citation_author_institution" content="Department of Civil and Environmental, University of Illinois" />

  <meta name="citation_author_institution" content="Department of Environmental and Resources, Zhejiang University" />

  <meta name="citation_author" content="Gemma Clark" />

  <meta name="citation_author_institution" content="Department of Civil and Environmental, University of Illinois" />

  <meta name="citation_author" content="Xueao Li" />

  <meta name="citation_author_institution" content="Department of Civil and Environmental, University of Illinois" />

  <link rel="canonical" href="https://Saran-Wang.github.io/dsproject/" />

  <meta property="og:url" content="https://Saran-Wang.github.io/dsproject/" />

  <meta property="twitter:url" content="https://Saran-Wang.github.io/dsproject/" />

  <meta name="citation_fulltext_html_url" content="https://Saran-Wang.github.io/dsproject/" />

  <meta name="citation_pdf_url" content="https://Saran-Wang.github.io/dsproject/manuscript.pdf" />

  <link rel="alternate" type="application/pdf" href="https://Saran-Wang.github.io/dsproject/manuscript.pdf" />

  <link rel="alternate" type="text/html" href="https://Saran-Wang.github.io/dsproject/v/f0291635eb5d3183df7e61fde96cd5cd6c040207/" />

  <meta name="manubot_html_url_versioned" content="https://Saran-Wang.github.io/dsproject/v/f0291635eb5d3183df7e61fde96cd5cd6c040207/" />

  <meta name="manubot_pdf_url_versioned" content="https://Saran-Wang.github.io/dsproject/v/f0291635eb5d3183df7e61fde96cd5cd6c040207/manuscript.pdf" />

  <meta property="og:type" content="article" />

  <meta property="twitter:card" content="summary_large_image" />

  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />

  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />

  <meta name="theme-color" content="#ad1457" />

  <!-- end Manubot generated metadata -->'
keywords:
- Pollution vision
- Machine learning
- Imgae processing
lang: en-US
manubot-clear-requests-cache: false
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
title: Project 5 Pollution Vision
...






<small><em>
This manuscript
([permalink](https://Saran-Wang.github.io/dsproject/v/f0291635eb5d3183df7e61fde96cd5cd6c040207/))
was automatically generated
from [Saran-Wang/dsproject@f029163](https://github.com/Saran-Wang/dsproject/tree/f0291635eb5d3183df7e61fde96cd5cd6c040207)
on December 6, 2020.
</em></small>

## Authors



+ **Shiyuan Wang**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [Saran-Wang](https://github.com/Saran-Wang)<br>
  <small>
     Department of Civil and Environmental, University of Illinois
  </small>

+ **Weiqi Ni**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [weiqini](https://github.com/weiqini)<br>
  <small>
     Department of Civil and Environmental, University of Illinois; Department of Environmental and Resources, Zhejiang University
  </small>

+ **Gemma Clark**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [441gclark](https://github.com/441gclark)<br>
  <small>
     Department of Civil and Environmental, University of Illinois
  </small>

+ **Xueao Li**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [XueaoLi](https://github.com/XueaoLi)<br>
  <small>
     Department of Civil and Environmental, University of Illinois
  </small>



## Abstract {.page_break_before}

## Introduction {.page_break_before}

## Literature Review {.page_break_before}
There are many studies using digital camera and advanced algorithm to estimate the concentrations of Particulate Matters. Hong et al. [@doi:10.1016/j.envint.2020.106044] developed a novel method of predicting the concentrations and diameters of outdoor ultrafine particles using street-level images and audio data in Montreal, Canada. Convolutional neural networks, multivariable linear regression and genralized additive models were used to make the predictions.


## Exploratory Data Anlysis {.page_break_before}
1. Variables Explanation
2. Data Cleaning
- Delete the useless columns in the dataset
- Delete the rows with equipment error during sampling
3. Visualization of the distributions of varibales
Figure shows that "Wind_Speed", "Camera_Angle", "Distance_to_Road" and "Elevation" are all in discrete distributions, while "Temp(C)" are in continuous distribution. "Pressure(kPa)" has four clusters. It should also be noted that the "Dead Time" almost shares the same distribution as "Total".
4. Correlations among variables

## Model {.page_break_before}
### Shiyuan's Model {.page_break_before}
My model setup splits into two part, the first is image data extraction, the second is the selection of appropriate model to fit this dataset.

#### Image Extraction

First I want to digitize images by extracting image features, there are mainly 6 features I want to extract: RGB, image luminance, image contrast, image entropy, transmission and amount of haze removed and number of cars on streets.

1. RGB

The RGB color model is one of the most straightforward parameters describing an image. Intuitively, in this case, we may expect more blueness and greenness if the PM concentrations are low since the color of tree and sky would be brighter when the air conditions are good.
For each image, after deriving the RGB of each pixel, we take the average of them, and then divide each value by 255 to normalize it.
The figure below @fig:RGB shows the distributions of RGB in this dataset. We can see that they are nearly normally distributed with mean 0.45, 0.55 and 0.35 respectively. For blueness, we could see a second peak at around 0.42.

![
**RGB Distribution**
](images/RGB.png "Wide image"){#fig:RGB}

 
2. Luminance
3. Contrast
4. Entropy
5. Transmission and amount of haze removed
6. Number of cars on streets




#### Model Selection


### Gemma's Model {.page_break_before}

### Weiqi's Model {.page_break_before}


### Xueao's Model {.page_break_before}
## Conclusion {.page_break_before}


## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
