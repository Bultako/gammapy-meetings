# Gammapy Telcon

* Friday, November 17, 2017 at 11 am
* CTA eZuce, password "gammapyregular" -> anyone interested welcome to join!

# Agenda

* Installation of a Coordination Committee: Bruno
* Gammapy update: Christoph
  * See info in the "reminder" section below about docs, tutorials, communication channels and private repositories.
    Note that we aim to improve and document our setup in the coming weeks (see comments by Bruno).
  * No v0.7 release yet. Bug report for "classical analysis" (1-dim spectra & 2-dim maps) from CTA analyses
    keep coming in, and are being fixed one by one. These remain: https://github.com/gammapy/gammapy/milestone/10
  * Recent developments:
    * Several PRs with fixes and improvements to `gammapy.maps`
    * Fix for ring background estimation merged 4 days ago: [GH 1204](https://github.com/gammapy/gammapy/pull/1204)
      More work going on to understand background estimation for CTA (see presentation by Fabio)
    * First PR started in the direction of collaboration between Gammapy and ctapipe yesterday: [GH 1211](https://github.com/gammapy/gammapy/pull/1211)
    * Some work re-started on point-like IRFs from CTA by Julien and Tarek:
      * https://github.com/gammapy/gammapy-extra/pull/83
      * https://github.com/open-gamma-ray-astro/gamma-astro-data-formats/issues/88
    * Astropy paper 2 is well-advanced: https://groups.google.com/forum/#!topic/astropy-dev/JNWdWfp2YcU
    * New Astropy APE on shared WCS that Matthew and I should look and see if it's relevant for the `WCSGeom`
      class in `gammapy.maps`: https://github.com/astropy/astropy-APEs/pull/34
  * Generally: there's a lot of work to be done. If you have time, please get in touch.
    If you're already a Gammapy contributor, please focus on https://github.com/gammapy/gammapy/milestone/10
    and on finishing up pull requests if you have any open.
* 1DC User feedbacks:
    * PeVatron: Cyril Trichard 
    * DC1 & RXJ : Fabio Acero
    * AoB?
* AoB (questions and discussion)
    * PSF for use with Sherpa (Yves Gallant)

## Reminder

A summary / reminder of what we have for the Gammapy project today.
This is just listing Gammapy things, in addition there are web pages, issue trackers, forums in CTA, HESS, ...

### Documentation and tutorials

* Gammapy docs: https://gammapy.readthedocs.io/
  * Contributions to improve the Gammapy documentation are welcome any time!
    The process is the same as for Gammapy code contributions, except that instead of editing
    `.py` Python files in the [gammapy](https://github.com/gammapy/gammapy/tree/master/gammapy) folder
    you edit `.rst` reStructuredText files in the [docs](https://github.com/gammapy/gammapy/tree/master/docs)
    folder. As an example: the page http://docs.gammapy.org/en/latest/maps/index.html is generated by Sphinx
    from this RST page: https://raw.githubusercontent.com/gammapy/gammapy/master/docs/maps/index.rst
    To build the documentation locally, use `python setup.py build_docs && open docs/_build/html/index.html`.
* Gammapy tutorials:
  * Here: https://nbviewer.jupyter.org/github/gammapy/gammapy-extra/blob/master/index.ipynb
  * Now also a copy is integrated into the Sphinx docs: http://docs.gammapy.org/en/latest/notebooks.html
* Gammapy webpage:
  * We have a domain registered: http://gammapy.org/
  * Currently just showing the Gammapy logo and if you click, leads to https://gammapy.readthedocs.io/
  * Needs some discussion what to put there and someone to work on it.
    Note that some projects (Astropy, sunpy) have such a webpage that's separate from the docs page,
    and other projects (e.g. scikit-learn, scikit-image, ctools) don't, they keep everything in one Sphinx docs page.
  * See https://github.com/gammapy/gammapy/issues/623

We need some re-organisation of content in the docs, as well as a lot of work on the docs to make
them better step by step.

### Communication channels

* Gammapy mailing list: https://groups.google.com/forum/#!forum/gammapy
  * It is used for announcements, user support and developer discussion.
  * It is public, anyone on the internet can read the content.
  * The rate of emails isn't very high (~ 1 per week)
  * You can sign up yourself.
* The Gammapy slack is at https://gammapy.slack.com (and they also have a nice app)
  * Used for text (or now also audio) chat by Gammapy users and developers
  * To sign up email one of the Gammapy developers (e.g. Roberta, Christoph, Bruno, Julien, Fabio)
  * Similar to Skype, but has channels (if they have that as well, then it's very similar)
  * Mostly used for 1:1 chat about git, Python, conda, issues, analysis results, ...
  * Discussion on code should mostly go in issues and pull requests on Github.
    But it's good to keep the discussion there focused and not e.g. sidetracked by git questions.
    And it's good to have a place to chat about e.g. private analysis results that doesn't lead
    to a permanent record in a mailing list.

We need to document that Slack exists and how to sign up in a prominent place.
We probably need to set up private mailing lists for Gammapy coordinators.
For CTA user support it's unclear if we should set up a private mailing list or forum,
or if the existing forums and mailing lists in CTA are sufficient or can be expanded.
See https://forge.in2p3.fr/projects/data-challenge-1-dc-1/wiki#Simulation-and-analysis-tools
and https://forge.in2p3.fr/projects/data-challenge-1-dc-1/wiki#Sharing-of-analysis-results

### Private repositories

We have some private repositories to collaborate on HESS & CTA analyses.

E.g. if you have a CTA DC-1 analysis with a bad result from Gammapy, please share your script
or notebook that lets us Gammapy developers reproduce the issue by making a new folder there
and putting your script or notebook. This is much more efficient than bug report that describe
with text what the issue is, without giving us a way to reproduce the issue. If you don't want
to use Git, you can also email us the files.

* https://github.com/gammasky/cta-analyses - CTA analyses and checks
* https://github.com/gammasky/cta-dc1-gps-analysis - CTA DC1 GPS analysis
* https://github.com/gammasky/hess-host-analyses - HESS FITS exporter issues
* https://github.com/gammasky/HESS-DL3-DR1 - HESS FITS test data release

To get access: contact one of the Gammay developers via Slack or email (e.g. Roberta, Christoph, Bruno, Julien, Fabio)