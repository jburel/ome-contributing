Code contributions
==================

In order to expedite the contribution of code to the OME project,
whether individual files or entire modules such as a service or web
application, we have put together the following guidelines. If you have
issues with any of the below, please let us know.

File headers
------------

The official `header templates`_ for each file type (Java, Python,
HTML, etc.)  can be found in the docs/headers.txt file of the source
repository. The correct template should be applied at the top of all
newly created files. The header of existing files should not be
modified without previous discussion except with regard to keeping the
year line up to date, for example changing "2008-2011" to "2008-2013".

Character encoding
------------------

OME Python and Java source files are all encoded in UTF-8.

Code style and linting
----------------------

Code styling can be a matter of intense debate.
We are in the process of introducing auto-formatters to most of our repositories to reduce the time wasted on formatting code or discussing code styles.
Where possible `pre-commit`_ is used to manage auto-formatters such as `black (Python)`_, as well as linters such as `flake8 (Python)`_.

Copyrights
----------

The copyright line for a newly created file is based on the
institution of the creator of the file and will remain unchanged even
if copied or moved.  Before redistribution of code can take place, an
agreement must be reached between the OME team and the copyright
holder.

Licenses
--------

The licenses of any files intended for redistribution with OME must be
compatible with the GPL and more restrictively for the web components
with the AGPL. Some files in the code-base (the schema, etc.) are
released under more liberal licenses but are still compatible with the
GPL.

Distribution
------------

For a block of work to be considered for redistribution with OME, the
code must further be made available in one of the following formats.

Patches/Pull requests
^^^^^^^^^^^^^^^^^^^^^

Smaller changes to the existing code base can be submitted to the team
either as patches, or preferably as pull requests on GitHub. You can
read more about pull requests on the :doc:`using-git` page.
The idea is that such smaller changes are reviewed line-by-line and
then maintained by the core team.

Submodules
^^^^^^^^^^

Larger submissions, which cannot be effectively reviewed so
intensively, should be submitted as `git submodules`_. Such submodules
provide a unique way to describe to a component version, which becomes
linked into the main codebase. During checkout, all submodules are
downloaded into the OME directory; and during the build process,
submodules are compiled into the official distribution.

The OME team cannot maintain or ship code which is only available as a
long-living branch (a fork) of the code base, and we would encourage
submitters to use one of the above methods.

Procedure for accepting code contributions
------------------------------------------

External contributors will need to sign our
:doc:`Contributor License Agreement <cla>` in order to get their pull requests
reviewed.

External pull requests will get an initial review to identify if they are suitable to pass into our
:doc:`continuous integration system <continuous-integration>` for building and
testing. We try to do this within 2 days of submission but please be patient
if we are busy and it takes longer.

If there are any obvious issues, we will comment and wait for you to fix
them. Once we are confident the PR contains no obvious errors, an "include"
label will be added which means the PR will be included in the merge build
jobs for the appropriate branch.

Build failures will then be noted on the PR and we will either submit a
patch or provide sufficient information for you to fix the problem yourself.
The "include" label will be removed until this is completed. The PR will be
merged once all the builds are green with the "include" label added.

If the code you wish to submit is large enough to require its own submodule,
you should :community:`contact us <>` to discuss how we might
incorporate your work into the official distribution.

Examples of contribution templates
----------------------------------

There are any number of other projects which have set up similar
practices for code contributions. If you would like to read more on
the rationale, please see:

* https://incubator.apache.org/
* https://www.apache.org/foundation/how-it-works.html

.. seealso::

	https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
		Best practices for git commit message formatting
	
	https://en.wikipedia.org/wiki/Technical_debt
		Wikipedia article on Technical debt

	https://prettier.io/docs/en/why-prettier.html
		Benefits of using an auto-formatter to avoid debates on style

.. _header templates: https://github.com/ome/openmicroscopy/blob/develop/docs/headers.txt
.. _git submodules: https://git-scm.com/book/en/Git-Tools-Submodules
.. _pre-commit: https://pre-commit.com/
.. _black (Python): https://black.readthedocs.io/
.. _flake8 (Python): https://flake8.pycqa.org/
