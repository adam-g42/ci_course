Installation
============

You need Python 3.12 or later.

Clone the repository, then from inside it create and activate a virtual
environment:

.. code-block:: bash

   python3 -m venv .venv
   source .venv/bin/activate

On Windows, activate it with ``.venv\Scripts\activate`` instead.

Install the package:

.. code-block:: bash

   python -m pip install -e ".[dev,docs]"

The ``dev`` extra adds the testing and linting tools, and ``docs`` adds
Sphinx. If you only want to use the package, ``python -m pip install .`` is
enough.

Check it worked by running the tests:

.. code-block:: bash

   pytest
