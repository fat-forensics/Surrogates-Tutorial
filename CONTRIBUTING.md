# Contributing Guide #

Thank you for considering contributing to our training materials.
This guide offers general information about the structure of the project as well as a high-level overview of a workflow that is put in place to streamline the contribution process.

## Communication and Support ##

[![Chat via Slack](https://img.shields.io/badge/slack-chat-yellow.svg?logo=slack)][slack]
[![Join Mailing List](https://img.shields.io/badge/google%20groups-discuss-orange.svg?logo=googlenews)][google_group]
[![Send an Email](https://img.shields.io/badge/email-ask-green.svg?logo=mail.ru)][email]
[![Open GitHub Issue](https://img.shields.io/badge/github-report%20issue-blue.svg?logo=github)][gh_issue]

If you want to get in touch, choose one of the following methods based on the problem that you are facing:

- reach out via [Slack][slack] to chat about the contents of this repository or seek support;
- join the [Google Group][google_group] to stay up to date with the project and discuss any of its aspects;
- drop us an [email][email] if you need to ask a private question or raise a concern; and
- open a [GitHub issue][gh_issue] to report a problem with this learning resource.

---

For problems related to the underlying software -- the [FAT Forensics][fatf_home] Python package -- please raise issues and contribute pull requests in its dedicated GitHub repository [fat-forensics/fat-forensics][fatf_gh].

## Project Structure ##

The main educational component is a collection of Jupyter Notebooks that can be found in the [`notebooks`](notebooks) directory.
They are prefixed with a number (`#-xxx.ipynb`) specifying their order.
The notebooks are complemented by:

- [`README.md`](notebooks/README.md) -- describes the notebooks and auxiliary files;
- [`requirements.txt`](notebooks/requirements.txt) -- captures the Python packages and their versions required to execute the notebooks; and
- [`fatf_ecml.py`](notebooks/fatf_ecml.py) -- implements bespoke Python functions to streamline the contents of the notebooks.

Additionally, the notebooks offer badges/buttons to launch them through [Binder][binder] and [Colab][colab].
The former copies the entire GitHub repository, hence no additional environment setup is needed;
however, the latter only grabs the selected notebook, therefore the `fatf_ecml.py` script has to be downloaded explicitly, and the `fatf_ecml.initialise_colab` function called to configure the execution environment.

---

Non-computational resources supporting this training module are:

- video recordings of the tutorial published as a [YouTube playlist][youtube]; and
- slides provided as a collection of [PDFs](JOSE/slides).

See the dedicated [webpage][events_page] for more details.

---

[![Text Licence](https://img.shields.io/badge/licence--text-CC%20BY--NC--SA%204.0-red)](LICENCE)
[![Code Licence](https://img.shields.io/badge/licence--code-new%20BSD-red)](LICENCE-code)

Note that code is licenced under *BSD 3-Clause*, and
text is licenced under *CC BY-NC-SA 4.0*.

## Contribution Workflow ##

[![Open GitHub Issue](https://img.shields.io/badge/github-report%20issue-blue.svg?logo=github)][gh_issue]

Before contributing to the repository, please open an [issue][gh_issue] to report and discuss the problem you encounter.
Please include the versions of your *operating system*, *Python* and *packages* (`pip list`) to make the debugging easier.
If possible, include the error trace and a minimal example that can be used to reproduce the problem.

[![Open GitHub Pull Request](https://img.shields.io/badge/github-open%20pull%20request-blue.svg?logo=github)][gh_pr]

Contribute your changes to a dedicated branch in a fork of the repository.
When ready, open a [pull request][gh_pr] to initiate the process of integrating your contributions into the codebase.
Please note that the notebooks are tested with a [GitHub Action][tests];
it checks whether the output of the notebook cells can be reproduced by executing them.

[slack]: https://fat-forensics.slack.com/
[google_group]: https://groups.google.com/forum/#!forum/fat-forensics
[email]: mailto:ask@fat-forensics.org
[gh_issue]: https://github.com/fat-forensics/Surrogates-Tutorial/issues
[gh_pr]: https://github.com/fat-forensics/Surrogates-Tutorial/pulls
[fatf_home]: https://fat-forensics.org/
[fatf_gh]: https://github.com/fat-forensics/fat-forensics
[binder]: https://mybinder.org/
[colab]: https://research.google.com/colaboratory/
[youtube]: https://www.youtube.com/playlist?list=PLgdhPOmeUNm0H2XTQECK3wabnDohZURLK
[events_page]: https://events.fat-forensics.org/2020_ecml-pkdd
[tests]: https://github.com/fat-forensics/Surrogates-Tutorial/actions/workflows/tests.yml
