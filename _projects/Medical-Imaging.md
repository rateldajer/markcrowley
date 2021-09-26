---
layout: page
collection: project
title: Manifold Learning
name: Manifold Learning and Dimensionality Reduction
keywords: Manifold-Learning, Dimensionality-Reduction
Permalink: manifold-learning
status: active
importance: 2
methods: SSIM, PCA, LDA, RDA, QQE, GLLE
description: Exploration of theoretical advances for macnirold learning and uses of these in medical imaging.
publish: false
people: benyaminghojogh,  markcrowley
showtitle: true
---

The recent focus on **Deep Learning** seems to raise the question whether
dedicated research on **[Manifold Learning and Dimensionality Reduction](manifold-learning)** are still required as their own pursuit since some form of Encoder-Decoder neural network could always be devised as a replacement.
While such systems work well, there is also certainly a role to
be played by interpretable models built on solid statistical concepts. 

Extraction of lower-dimensional representations of data can allow more compact storage or transmission and
also improve the performance of other ML tasks such as classification and regres_sion, as the more compact representation
must necessarily encode the most important relationships to maintain accuracy. 

This is an exciting group of work which has published in several good conferences so far {% cite ghojogh2020weighted %}-{% cite ghojogh2019rda %},{% cite ghojogh2019llise %}-{% cite ghojogh2019pcassim %}, and in particular **{% cite ghojogh2018psa %}**:

> {% reference ghojogh2018psa %}


\bla{I am working with my students and collaborators on a journal paper which will unify some of this work and I am also in the process of writing a reference textbook on this topic, in collaboration with two professors in ECE and Statistics covering the latest literature and open questions.}

This work has culiminatedd recently in the completion of my first Doctoral student, [Benyamin Ghojogh]({{ site.data.coauthors[Ghojogh].url }}), in April 2021 with his thesis encompassing many of these advances.
Dr. Ghojogh continues as a postdoc now with my lab and we have an approved book deal with Springer for a textbook due out later in 2021 on "Manifold Learning and Dimensionality Reduction" which we are writing in collaboration with Prof. Ali Gosi andd Prof. Fakhri Karray.

## Bibliography
{% bibliography --cited %}