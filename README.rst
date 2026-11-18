Shuup
=====

This repository contains Shuup, an open-source e-commerce platform built with
Django and Python. The project includes a storefront, an administration
interface, and an add-on system.

https://shuup.com/

Copyright
---------

Copyright (c) 2012-2021 by Shuup Commerce Inc. <support@shuup.com>

Shuup is International Registered Trademark & Property of Shuup Commerce Inc.,
Business ID: BC1126729,
Business Address: 1500 West Georgia Suite 1300, Vancouver, BC, V6G-2Z6, Canada.

CLA
---

Contributor License Agreement is required for any contribution to this
project.  Agreement is signed as a part of pull request process.  See
the CLA.rst file distributed with Shuup.

License
-------

Shuup is published under Open Software License version 3.0 (OSL-3.0).
See the LICENSE file distributed with Shuup.

Some external libraries and contributions bundled with Shuup may be
published under other compatible licenses. For these, please
refer to VENDOR-LICENSES.md file in the source code tree or the licenses
included within each package.

Chat
----

We have a Gitter chat room for Shuup.  Come chat with us!  |Join chat|

.. |Join chat| image:: https://badges.gitter.im/Join%20Chat.svg
   :target: https://gitter.im/shuup/shuup

Docker quick start
------------------

From the repository root, use `Docker <https://www.docker.com>`_ with the
Compose plugin to start the demo. The bundled Dockerfile installs the published
Shuup package by default. For local source development, see the development
guide below.

1. Run:

   .. code-block:: shell

      docker compose up --build

2. Open `localhost:8000/sa <http://localhost:8000/sa>`_ in a browser,
   sign in with the demo credentials ``admin`` / ``admin``.
   Use these credentials for local testing only.

Full Shuup installation guide
-----------------------------

See `Getting Started
<http://shuup.readthedocs.io/en/latest/howto/getting_started.html>`__.

For simple project example see our `Django-project template <https://github.com/shuup/shuup-project-template>`__.

Getting Started with Shuup development
--------------------------------------

See `Getting Started with Shuup Development
<http://shuup.readthedocs.io/en/latest/howto/getting_started_dev.html>`__.

Contributing to Shuup
---------------------

Interested in contributing to Shuup? Please see our `Contribution Guide
<https://www.shuup.com/contributions/>`__.

Documentation
-------------

Shuup documentation is available online at `Read the Docs
<http://shuup.readthedocs.org/>`__.

Documentation is built with `Sphinx <http://sphinx-doc.org/>`__.

Issue the following commands to build the documentation:

.. code:: sh

    pip install -r requirements-doc.txt
    cd doc && make html

To update the API documentation rst files, e.g. after adding new
modules, use command:

.. code:: sh

    ./generate_apidoc.py

Historical upstream roadmap
---------------------------

v3 (Q4 2021)
###############

* Initial Django 3.x support
* Latest Jinja support
* Deprecate theme folders under Shuup front which are used to override
  individual macros in macro folders. This does not work well with latest
  Jinja and adds extra complexity.

v4 (Q1 2022)
#############

* Move Shuup front, xtheme and theming features to own addons. This so that
  projects not ready for updating theme or front can still get latest Shuup.
* Introduce new default theme and overhaul templates structure to be more
  simple (likely Bootstrap 5 will be used).
* Bump admin Bootstrap version to match with the new front
* Move various other not essential apps in this repository to addons for
  better version management.

Additional Material
-------------------

* `Django-project template <https://github.com/shuup/shuup-project-template>`__. Django-project template.
* `Provides system <https://shuup.readthedocs.io/en/latest/ref/provides.html>`__.
* `Core settings <https://shuup.readthedocs.io/en/latest/api/shuup.core.html#module-shuup.core.settings>`__.
* `Front settings <https://shuup.readthedocs.io/en/latest/api/shuup.front.html#module-shuup.front.settings>`__.
* `Admin settings <https://shuup.readthedocs.io/en/latest/api/shuup.admin.html#module-shuup.admin.settings>`__.
* `Extending Shuup <https://shuup.readthedocs.io/en/latest/#extending-shuup>`__.


Admin Preview
-------------

.. image:: doc/_static/admin_shop_product.png
    :target: doc/_static/admin_shop_product.png
    :height: 300px

.. image:: doc/_static/admin_order_detail.png
    :target: doc/_static/admin_order_detail.png
    :height: 300px
