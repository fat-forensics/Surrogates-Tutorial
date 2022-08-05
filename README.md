[![Read More](https://img.shields.io/badge/read-more-blue)](https://events.fat-forensics.org/2020_ecml-pkdd)
[![Text Licence](https://img.shields.io/badge/licence--text-CC%20BY--NC--SA%204.0-red)](LICENCE)
[![Code Licence](https://img.shields.io/badge/licence--code-new%20BSD-red)](LICENCE-code)  
[![JOSE DOI](https://jose.theoj.org/papers/d58625bd4c600da866522c879986b18f/status.svg)](https://jose.theoj.org/papers/d58625bd4c600da866522c879986b18f)
[![ZENODO DOI](https://zenodo.org/badge/472186940.svg)](https://zenodo.org/badge/latestdoi/472186940)
[![GitHub Release](https://img.shields.io/github/v/release/fat-forensics/Surrogates-Tutorial?display_name=tag&logo=github)](https://github.com/fat-forensics/Surrogates-Tutorial/releases/latest)  
[![Tests Status](https://github.com/fat-forensics/Surrogates-Tutorial/actions/workflows/tests.yml/badge.svg)](https://github.com/fat-forensics/Surrogates-Tutorial/actions/workflows/tests.yml)  
[![Open in Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fat-forensics/Surrogates-Tutorial/master?filepath=notebooks)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/fat-forensics/Surrogates-Tutorial/blob/master/)

# What and How of Machine Learning Transparency #
## Building Bespoke Explainability Tools with Interoperable Algorithmic Components ##

Explainability techniques for data-driven predictive models based on
artificial intelligence and machine learning algorithms allow us to
better understand the operation of such systems and hold them
accountable[^1].
New transparency approaches are therefore developed at breakneck speed
to peek inside these black boxes and interpret their decisions.
Many of these techniques are introduced as monolithic tools, giving the
impression of one-size-fits-all and end-to-end algorithms with limited
customisability.
However, such approaches are often composed of multiple interchangeable
modules that need to be tuned to the problem at hand to produce meaningful
explanations[^2].
This repository holds a collection of interactive, hands-on training materials
(offered as Jupyter Notebooks) that provide guidance through the process of
building and evaluating bespoke modular surrogate explainers for black-box
predictions of tabular data.
These resources cover the three core building blocks of this technique
introduced by the bLIMEy meta-algorithm: interpretable representation
composition, data sampling and explanation generation[^2].

The following materials are available
(follow the links to see their respective descriptions):

* Hands-on Resources (Jupyter Notebooks) – [notebooks](notebooks) directory.
* Presentation Slides – [slides](slides) directory.
* Video Recordings – [YouTube][yt] playlist.

These resources were used to deliver a [hands-on tutorial][tut] at
*ECML-PKDD 2020*;
see <https://events.fat-forensics.org/2020_ecml-pkdd> for more details.
Alternatively, see the [paper][jose] published in the
*Journal of Open Source Education*.
The notebooks can either be launched online
(via [MyBinder][binder] or [Google Colab][colab]) or on a personal machine
(Python 3.7 or higher is required).
The latter can be achieved with the following steps:

1. Clone this repository.
   ```bash
   git clone --depth 1 https://github.com/fat-forensics/Surrogates-Tutorial.git
   ```
2. Install Python dependencies.
   ```bash
   pip install -r notebooks/requirements.txt
   ```
3. Launch Jupyter Lab.
   ```bash
   jupyter lab
   ```
4. Navigate to the [notebooks](notebooks) directory and
   open the desired notebook.

Note that code is licenced under *[BSD 3-Clause](LICENCE-code)*, and
text is covered by *[CC BY-NC-SA 4.0](LICENCE)*.
The [CONTRIBUTING.md](CONTRIBUTING.md) file provides contribution guidelines.
To reference this repository and the training materials it provides please use:
```bibtex
@misc{sokol2020what,
  author       = {Sokol, Kacper and
                  Hepburn, Alexander and
                  Santos-Rodriguez, Raul and
                  Flach, Peter},
  title        = {{W}hat and How of Machine Learning Transparency:
                  {B}uilding Bespoke Explainability Tools with
                  Interoperable Algorithmic Components},
  month        = sep,
  year         = 2020,
  publisher    = {Zenodo},
  version      = {2020-ecml-pkdd},
  doi          = {10.5281/zenodo.6395490},
  url          = {https://doi.org/10.5281/zenodo.6395490}
}
```
or refer to the [CITATION.cff](CITATION.cff) file.

[yt]: https://www.youtube.com/playlist?list=PLgdhPOmeUNm0H2XTQECK3wabnDohZURLK
[tut]: https://events.fat-forensics.org/2020_ecml-pkdd
[binder]: https://mybinder.org/v2/gh/fat-forensics/Surrogates-Tutorial/master?filepath=notebooks
[colab]: https://colab.research.google.com/github/fat-forensics/Surrogates-Tutorial/blob/master/
[jose]: https://jose.theoj.org/papers/d58625bd4c600da866522c879986b18f
[^1]: Sokol, K., & Flach, P. (2021). *Explainability is in the mind of the beholder: Establishing the foundations of explainable artificial intelligence*. arXiv Preprint arXiv:2112.14466. <https://doi.org/10.48550/arXiv.2112.14466>
[^2]: Sokol, K., Hepburn, A., Santos-Rodriguez, R., & Flach, P. (2019). *bLIMEy: Surrogate prediction explanations beyond LIME*. Workshop on Human-Centric Machine Learning (HCML 2019) at the 33rd Conference on Neural Information Processing Systems (NeurIPS). <https://doi.org/10.48550/arXiv.1910.13016>
