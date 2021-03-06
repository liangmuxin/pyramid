.. _setup:

=====
Setup
=====

Pyramid depends on several prominent python packages:

* `Numpy <https://github.com/numpy/numpy>`_
* `SciPy <https://github.com/scipy/scipy>`_
* `Scikit-learn <https://github.com/scikit-learn/scikit-learn>`_ (>= 0.17)
* `Pandas <https://github.com/pandas-dev/pandas>`_
* `Statsmodels <https://github.com/statsmodels/statsmodels>`_ (>=0.9.0)

Install from PyPi
-----------------

Pyramid is on pypi under the package name ``pyramid-arima`` and can be
downloaded via ``pip``:

.. code-block:: bash

    $ pip install pyramid-arima

Pyramid uses Cython, which means there is some C source that was built in
the distribution process. To ensure the package was built correctly, import
the following module in python:

.. code-block:: python

    from pyramid.arima import auto_arima

If you encounter an ``ImportError``, try updating numpy and re-installing. Outdated
numpy versions have been observed to break the Pyramid build.

Build from source
-----------------

If you'd like to install a development or bleeding edge version of Pyramid,
you can always build it from the git source. First clone it from Git:

.. code-block:: bash

    $ git clone https://github.com/tgsmith61591/pyramid.git
    $ cd pyramid

Building the package will require ``gcc`` (unix) or a Windows equivalent, like
``MinGW``. To build in development mode (for running unit tests):

.. code-block:: bash

    $ python setup.py develop

Alternatively, to install the package in your ``site-packages``:

.. code-block:: bash

    $ python setup.py install
