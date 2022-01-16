---
title: 'VEST: Video event segmentation tool for qualitative event annotations'
tags:
  - Javascript
  - Psychology
  - Video
  - time series
  - soical intearctions
authors:
  - name: Jin Hyun Cheong # note this makes a footnote saying 'co-first author'
    orcid: 0000-0002-9255-1648
    affiliation: 1 # (Multiple affiliations must be quoted)
affiliations:
 - name: Psychological and Brain Sciences, Dartmouth College
   index: 1
date: 13 January 2021
bibliography: paper.bib
---

# Summary

Researchers have used video recordings of human and animal behaviors to analyze social and psychological phenomena for decades. Recent advances in computer vision and machine learning have facilitated automated coding in some domains, but human input is still ubiquitiously required for training new models and identifying novel or complex behaviors. Software to code events and behaviors, however, are often proprietary, require complex installation steps, or too domain specific for general use. The Video Event Segmentation Tool (VEST) enables users to easily code meanignful behaviors using both video and audio features from a free, lightweight browser interface that does not require installation. Sample use cases of VEST include coding for when and who is speaking in conversations, annotating complex facial expressions, and social behaviors. 

# Statement of need

`VEST` is a video event segmentation toolbox for qualitative event segmentation and annotations of video clips. Analyzing video recordings of human and animal behaviors is a fundamental research tool used across disciplines [@chartrand1999chameleon; @Chen:2019; @Cheong:2020; masataka2009free; @karashchuk2021dannce; @dunn2021geometric]. This approach has been greatly facilitated by recent advances in computer vision and machine learning which can identify facial expressions, body poses, and vocal features. However, accuracy can be limited in certain domains manual human codings can be still required to identify novel and complex phenomena. 

Selection of tools to identiy segment events in videos are limited. Especially for qualitative coding of videos, most tools are proprietary, require installation, and difficult to use [@hellwig2007eudico; @Wikipedia:2022]. VEST offers significant improvement in these domains. First, VEST is free and open-source. Users can simply use the browser interface or modify it to suit there needs. Second, VEST does not require installation nor a license subscription. Lastly, VEST is easy to use. Users can load a video which will automatically render with audio waveforms utilizing the peak.js [@peakjs] framework. Users can then add buttons with custom labels for creating segmentations as they watch the video. The audio waveform helps demarcate the start and end points of each event segment with greater precision (Figure 1). 

![Figure 1. Screenshot of VEST in action. Labels for event segmentations can be customized by users.](figure.png){ width=60% }

The simplicity of the tools allows it to be used in diverse ways. To name a few ideas: 
- Segment who is speaking and when in conversation videos to compare speech durations, gaps in conversations, and overlapping speech.
- Label occurence of complex social behaviors such as agreement, disagreement, or alienating an individual.
- Label facial expressions from face video recordings.
- Segment the start and end times of animal behaviors such as grooming, socializing, and feeding.


# Figures

Figures can be included like this:
![Caption for example figure.\label{fig:example}](figure.png)
and referenced from text using \autoref{fig:example}.

Figure sizes can be customized by adding an optional second parameter:
![Caption for example figure.](figure.png){ width=20% }

# References