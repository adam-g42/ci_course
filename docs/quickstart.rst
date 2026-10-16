Quickstart
==========

This example loads the sample data that comes with the package, summarises
each column, and writes a report.

Load the data
-------------

.. code-block:: python

   import ci_course

   data = ci_course.load_measurements()

``data`` is a dictionary mapping each column name (``temperature_c`` and
``mass_g``) to an array of values. Missing values are ``nan``. To load your
own CSV file instead, pass its path: ``ci_course.load_measurements("my_data.csv")``.

Summarise it
------------

.. code-block:: python

   summaries = ci_course.summarise_all(data)
   print(summaries["temperature_c"])

Each summary gives the number of values present, and their mean, standard
deviation, minimum and maximum. Missing values are ignored.

Write a report
--------------

.. code-block:: python

   ci_course.write_report(summaries, "report.txt")

``report.txt`` then contains:

.. code-block:: text

   Measurement summary
   ===================
   temperature_c: n=7 mean=20.871 sd=0.862 min=19.800 max=22.300
   mass_g: n=7 mean=1.443 sd=0.050 min=1.380 max=1.510

From the command line
---------------------

The same summary is available without writing any Python:

.. code-block:: bash

   ci-course
