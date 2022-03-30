---
title: |
  What and How of Machine Learning Transparency:
  Building Bespoke Explainability Tools with Interoperable Algorithmic Components
tags:
  - Transparency
  - Explainability
  - Interpretability
  - Surrogate Explainers
  - Tabular Data
  - Artificial Intelligence
  - Machine Learning
  - Hands-on
  - Tutorial
authors:
  - name: Kacper Sokol
    orcid: 0000-0002-9869-5896
    affiliation: 1
  - name: Alexander Hepburn
    affiliation: 2
  - name: Raul Santos-Rodriguez
    orcid: 0000-0001-9576-3905
    affiliation: 2
  - name: Peter Flach
    orcid: 0000-0001-6857-5810
    affiliation: 1
affiliations:
  - name: Department of Computer Science, University of Bristol
    index: 1
  - name: Department of Engineering Mathematics, University of Bristol
    index: 2
date: 01 April 2022
bibliography: paper.bib
---

# Summary #

Explainability techniques for data-driven predictive models based on
artificial intelligence and machine learning algorithms allow us to
better understand the operation of such systems and hold them
accountable [@sokol2021explainability].
New transparency approaches are therefore developed at breakneck speed
to peer inside these black boxes and interpret their decisions.
Many of these techniques are introduced as monolithic tools, giving the
impression of one-size-fits-all and end-to-end algorithms with limited
customisability.
However, such algorithms are often composed of multiple interchangeable
modules that need to be tuned to the problem at hand to produce meaningful
explanations [@sokol2019blimey].
This paper introduces a collection of [hands-on training materials][github] --
slides, video recordings and Jupyter Notebooks -- that guide through the process
of building and evaluating bespoke modular surrogate explainers of tabular data.
These resources cover the three core building blocks of this technique
introduced by the bLIMEy meta-algorithm: interpretable representation
composition, data sampling and explanation generation [@sokol2019blimey].

[github]: https://github.com/fat-forensics/Surrogates-Tutorial

# Modular Surrogate Explainers #

<!-- learning objectives -->
The training materials introduce the concept of modular explainability
algorithms using the example of surrogate explainers for tabular data.
This separation of functionally independent building blocks allows us to
consider the influence of each component, and their interdependence, on the
robustness and faithfulness of the final explainer.
To this end, we overview a collection of techniques to evaluate the quality
of its modules and its overall effectiveness.
Moreover, these metrics can guide the parameterisation of the entire
explainability algorithm, providing an opportunity to tune it to the problem
at hand.
All of these insights demonstrate that while surrogate explainers are
model-agnostic and post-hoc -- i.e., they work with any black box and
can be retrofitted into pre-existing predictive models, making them a
popular choice for explaining black-box predictions [@ribeiro2016should] --
using off-the-shelf explainability approaches may result in subpar
performance for individual use cases.
Therefore, understanding how to build a bespoke surrogate explainer
that is suitable for a particular situation is a prerequisite for
trustworthy and meaningful explainability of data-driven systems
and their decisions.

<!-- contents summary -->
Prior to diving into the practicalities of composing surrogate explainers,
the training materials introduce the concept of algorithmic explainability
and discuss the fundamental ideas behind surrogates for text,
image and tabular data.
This theoretical overview is followed by a brief presentation of the software
used for the hands-on modules;
`FAT Forensics`^[https://fat-forensics.org] is an open source Python package
designed for inspecting selected fairness, accountability and *transparency*
aspects of data (and their features), *models* and *predictions*
[@sokol2019fatf; @sokol2020fatf].
Having covered the basics, the practical coding resources focus on the three
building blocks of surrogate explainers for tabular data identified by the
bLIMEy -- build LIME yourself [@sokol2019blimey] -- meta-algorithm:

* interpretable (data) representation composition;
* data sampling; and
* explanation generation (interpretable feature selection,
  data sample weighting, surrogate model training and explanation extraction).

These learning modules show some of the interoperable algorithmic components
available at each step, discuss their pros and cons for a range of applications,
guide through their optimal selection strategies and propose suitable
evaluation criteria -- see the figure below.
In particular, interpretable representations are built with
quartile discretisation and decision trees [@sokol2020towards];
data are generated with Gaussian and mixup sampling
[@zhang2018mixup; @sokol2019blimey]; and
explanations are extracted from linear and tree-based
surrogate models [@sokol2020limetree].
Notably, these choices influence the type and quality of the resulting
explanations produced for black-box predictions.
Therefore, these hands-on materials illustrate how such atomic functional
blocks behave in various scenarios and demonstrate how to use these
components to configure robust explainers with well-known properties and
failure modes based on first-hand observations and a collection of
quantitative evaluation metrics and validation techniques.

![Modularity of surrogate explainers, listing components specific to tabular data.](modular_surrogates.pdf){width=65%}

<!-- instructional design -->
The introduction to algorithmic explainability; the theoretical overview of
surrogate explainers for text, image and tabular data; and the outline of
`FAT Forensics` are presented in a collection of *slides* and
*instructional video recordings*.
The hands-on materials are delivered with *Jupyter Notebooks* that interweave
textual guidance, code examples and informative plots.
All the insights learnt throughout the practical exercises enable the tutees to
build robust surrogate explainers of an arbitrary black-box predictive model
for their own tabular data set.
The training resources are designed to appeal and be accessible to an audience
with a wide range of backgrounds and experiences.
Active participation in the hands-on part requires basic familiarity with
Python programming and access to a computer connected to the Internet, which
enables execution of the Jupyter Notebooks online without installing any
software on a personal machine.

<!-- experience of use in teaching and learning situations -->
These training materials were used to deliver a hands-on tutorial -- of
the same title -- at the 2020 European Conference on Machine Learning and
Principles and Practice of Knowledge Discovery in Databases
(ECML-PKDD)^[https://events.fat-forensics.org/2020_ecml-pkdd],
the recordings of which are available on
YouTube^[https://www.youtube.com/playlist?list=PLgdhPOmeUNm0H2XTQECK3wabnDohZURLK].
Moreover, they inspired a number of interactive sessions at various
summer schools aimed at doctoral students in artificial intelligence and
machine learning, as well as undergraduate lectures, academic
presentations and invited talks.
The slides, additional hands-on resources and video recordings of some of
these events are available on the FAT Forensics Events
website^[https://events.fat-forensics.org].

# Statement of Need #

<!-- how these contribute to computationally enabled teaching and learning
     how they might be adopted by others -->
The training materials introduce a novel learning paradigm for algorithmic
explainability of data-driven predictive systems based on artificial
intelligence and machine learning techniques.
Instead of treating these tools as end-to-end, monolithic entities whose
configuration is only facilitated through the parameters exposed by
their developers, these educational resources look into their modularity to
identify atomic and interoperable functional building blocks.
By decomposing explainers into their core elements we can better understand
their role and configure them for the application at hand.
In this purview, such techniques are diagnostic tools that *only* become
explainers when their properties and interpretation of their outputs
are well understood.
Therefore, to engender trust in data-driven predictive systems, the employed
explainability approaches must be trustworthy themselves in
the first place -- the learning objective underlying the interactive
coding exercises.
Notably, the modularity and diversity of these training materials -- slides,
video recordings and Jupyter Notebooks -- allow them to be adapted or
directly incorporated into a course on explainable artificial intelligence
and interpretable machine learning, or form the basis of a range of
educational resources such as practical training sessions and conference
tutorials.

# References #
