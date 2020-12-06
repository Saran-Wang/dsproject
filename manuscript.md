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

  <link rel="alternate" type="text/html" href="https://Saran-Wang.github.io/dsproject/v/9276bbe764bdcb09aa2203c039cbbaafaf526b3e/" />

  <meta name="manubot_html_url_versioned" content="https://Saran-Wang.github.io/dsproject/v/9276bbe764bdcb09aa2203c039cbbaafaf526b3e/" />

  <meta name="manubot_pdf_url_versioned" content="https://Saran-Wang.github.io/dsproject/v/9276bbe764bdcb09aa2203c039cbbaafaf526b3e/manuscript.pdf" />

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
([permalink](https://Saran-Wang.github.io/dsproject/v/9276bbe764bdcb09aa2203c039cbbaafaf526b3e/))
was automatically generated
from [Saran-Wang/dsproject@9276bbe](https://github.com/Saran-Wang/dsproject/tree/9276bbe764bdcb09aa2203c039cbbaafaf526b3e)
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

| Data Fields | Explanation | 
|:-----------------:|:-------------|
|Temp(C)  |ambient temperature  |
|Pressure(kPa) |air pressure | 
| Rel. Humidity | relative humidity | 
| Errors | if the air measurement equipment has error during sampling (0=no) | 
| Alarm Triggered | if any instrumental warning shows during sampling (0=no) | 
| Dilution Factor | an instrumental parameter (should close to 1) | 
| Dead Time |another instrumental parameter (ideally close to 0)  | 
| Median, Mean, Geo. Mean, Mode, and Geo. St. Dev. | parameters describe particle sizes, which can be ignored | 
| Total Conc. | an output variable from the instrument that should not be used | 
| image_file | the visual information of the traffic condition, corresponding to an image in the "frames" directory | 
| Wind_Speed |  the wind velocity during sampling| 
| Distance_to_Road | the distance between camera and road | 
| Camera_Angle | the angle of incidence between the camera and the road | 
| Elevation | the elevation between the camera and the breathing zone | 
| Total | the total measured particle number concentration (# / cm3) This is the dependent variable | 

Table: Variables Explanation
{#tbl:Explanation}

2. Data Cleaning
- Delete the useless columns in the dataset
- Delete the rows with equipment error during sampling
3. Visualization of the distributions of varibales
Figure @fig:Distributions shows that "Wind_Speed", "Camera_Angle", "Distance_to_Road" and "Elevation" are all in discrete distributions, while "Temp(C)" are in continuous distribution. "Pressure(kPa)" has four clusters. It should also be noted that the "Dead Time" almost shares the same distribution as "Total".

![
**Variables Distribution**
](images/Distributions.png "Wide image"){#fig:Distributions width=7in}

4. Correlations among variables
From the correlation map @fig:Correlations we could see that "Dead Time" are extremely correlated with "Total", with a coefficient of 1, followed by  "Camera_Angle", "Pressure(kPa)" and "Distance_to_Road", with coefficient of 0.52, 0.49, 0.44 respectively. Here you may be curious why "Dead Time" could be so closely related to "Total", and there is one possible explanation: Actually, "Dead Time" is an instrument parameter, and if there are more PM concentrations in the air, the instrument need more time to process, and vice versa. 

![
**Variables Correlations**
](images/Correlation.png "Wide image"){#fig:Correlations height=3in}

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

Like RGB, luminance is also a very basic parameter describing an image, which could be an indicator of how bright the image will appear. The luminance of each image is calculated by taking the average of the luminance intensity of each pixel. 
From figure @fig:Luminance we could also see that it’s also normally distributed with a mean of around 130.

![
**Luminance Distribution**
](images/Luminance.png "Wide image"){#fig:Luminance height=3in}


3. Contrast
$$Absolute Contrast = \frac{I(i_{max}, j_{max}) - I(i_{min}, j_{min})}{I(i_{max}, j_{max})+ I(i_{min},  j_{min})}$$ {#eq:absolute-contrast}
$$RMS of Contrast = \sqrt{\frac{1}{MN}\sum{i=1}{N}\sum{j=1}{M}(I(i,j)-avg(I))^2}$$ {#eq:RMS-contrast}
where I(i,j) is luminance intensity at (i,j) pixel.






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
