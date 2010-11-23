ez_setup
========

**Problem**: ``setup.py`` of several Python projects blindly import the
setutools bootstrap module ``ez_setup.py`` without realizing that it is usually
not installed in the user's machine.
`This causes much trouble <http://www.google.ca/search?sourceid=chrome&ie=UTF-8&q=%22ImportError:+No+module+named+ez_setup%22&qscrl=1>`_.

**Workaround**: Include ``ez_setup.py`` (and ``distribute_setup.py``) as a
installable Python package so users can do
``easy_install ez_setup troublesome_package`` as a workaround.

**Note**: The ``ez_setup.py`` file being distributed is simply a copy of
``distribute_setup.py`` from the `Distribute`_
project (a setuptools fork); this is
to remain compatible with several Python distributors opting to use Distribute
instead of Setuptools -- examples: Debian, ActiveState, and so on.

Credits
-------

- `Distribute`_
- `modern-package-template`_

.. _Distribute: http://code.activestate.com/pypm/distribute/
.. _`modern-package-template`: http://code.activestate.com/pypm/modern-package-template/
