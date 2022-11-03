=============================
Python Related Configurations
=============================

Select Python Interpreter
-------------------------

Each project has its own python interpreter in its python virtual environment. To execute a python file from its project python interpreter, open the file on the editor and select the interpreter from the status bar or from ``Ctrl+Shift+P``:

.. code-block:: bash

   > Python: Select Interpreter

Having chosen the project in the workspace folder, search for the interpreter path in the project:

.. code-block:: bash

   > Enter interpreter path...

Or if the python virtual environment is at the root of the project, simply select the recommended path ``./.env/bin/python``.

.. note::

   It can happen that vscode doesn't change interpreters. It seems to have worked to delete some of the existing python virtual environments in different projects. VSCode was then able to select the correct interpreter. The following commands may help debug the situation:

.. code-block:: bash

   ! which python

.. code-block:: bash

   ! echo $VIRTUAL_ENV

.. code-block:: python

   import sys
   print(sys.executable)
