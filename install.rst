=========
 Install
=========

To install Choreonoid editor plugin, you first have to install Choreonoid.

Install Choreonoid editor from ppa (recommended)
================================================

We recommend installing Choreonoid from ppa.

.. code-block:: bash

   $ sudo add-apt-repository ppa:hrg/daily
   $ sudo apt-get update
   $ sudo apt-get install choreonoid-editor

Install Choreonoid editor from source
=====================================

Install Choreonoid from ppa
---------------------------

We recommend installing Choreonoid from ppa.

.. code-block:: bash

   $ sudo add-apt-repository ppa:hrg/daily
   $ sudo apt-get update
   $ sudo apt-get install choreonoid libcnoid-dev

Install Choreonoid from source
------------------------------

.. warning::

   Source based installation is hard way.
   ppa based installation is highly recommended.

If you want to install Choreonoid from source, please follow following instructions:

Instructions in Japanese:
 http://choreonoid.org/ja/manuals/1.5/install/build-ubuntu.html

Instructions in English:
 https://github.com/s-nakaoka/choreonoid/blob/master/INSTALL


Install Choreonoid Editor Plugin
--------------------------------

Clone most recent source from github.

.. code-block:: bash

   $ git clone https://github.com/fkanehiro/choreonoid-editor.git

Then, run cmake.

.. code-block:: bash

   $ cd choreonoid-editor
   $ cmake .

Then, run following commands to compile, install and run.

.. code-block:: bash

   $ make
   $ sudo make install
   $ choreonoid
