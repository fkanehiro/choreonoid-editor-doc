=========
 Install
=========

Install from source
===================

Clone most recent source from github.

.. code-block:: bash

   $ git clone https://github.com/fkanehiro/choreonoid-editor.git

First, install depending libraries.

.. code-block:: bash

   $ cd choreonoid-editor
   $ ./misc/script/install-requisites-ubuntu-14.04.sh

Then, run cmake or ccmake.

If you use cmake, please specify following option on the command line.

.. code-block:: bash

   $ cmake -DBUILD_MODELEDIT_PLUGIN=ON .

If you use ccmake, please turn setting of "BUILD_MODELEDIT_PLUGIN" item to "ON".

.. image:: ccmake-option.png

Then, run following commands to compile and run.

.. code-block:: bash

   $ make
   $ ./bin/choreonoid
