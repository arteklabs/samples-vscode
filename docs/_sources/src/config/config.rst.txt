========
Settings
========

Display terminal in editor window
---------------------------------

.. code-block:: json

   {
      "terminal.integrated.defaultLocation": "editor"
   }

Open ``bash`` as the default terminal
-------------------------------------

.. code-block:: json

   {
      "terminal.integrated.defaultProfile.linux": "bash"
   }

Create multiple workspaces
--------------------------

Create a directory ``vscode-workspaces`` with files ``*.code-workspace`` with contents:

.. code-block:: json

   {
       "folders": [
           {
               "name": "samples-vscode",
               "path": "../src/samples-vscode"
           },
       ]
   }

Add to ``settings.json``:

.. code-block:: json

   {
      "workspaceExplorer.workspaceStorageDirectory": "vscode-workspaces"
   }

extension: ``tomsaunders.vscode-workspace-explorer``

Docstring Format
----------------

Specify a docstring format when adding docstrings with ``Ctrl+Shift+2`` under a signature.

.. code-block:: json

    {
        // docstring format
        "autoDocstring.docstringFormat": "sphinx"
    }

extension: ``njpwerner.autodocstring``

Sync Settings
-------------

Login to vscode with your profile. Your settings ``settings.json`` and ``extensions`` will sync automatically.

Project settings
----------------

The project settings are specified at `.vscode/settings.json` and extend/overwrite the workspace settings at `settings.json`.

Typescript
----------

.. code-block:: json

   {
      // inline count of reference for classes, interfaces, methods, properties, 
      // and exported objects
      "typescript.referencesCodeLens.enabled": true,

      // displays the number of implementors of an interface
      "typescript.implementationsCodeLens.enabled": true,

      "typescript.referencesCodeLens.showOnAllFunctions": true,
   }

Select Python Interpreter
-------------------------

Each project has its own python interpreter in its python virtual environment. To execute a python file from the project interpreter, open the file on the editor and select the interpreter from the status bar or from ``Ctrl+Shift+P``:

.. code-block:: bash

   > Python: Select Interpreter

Having chosen the project in the workspace folder, search for the interpreter path in the project:

.. code-block:: bash

   > Enter interpreter path...

Or if the python virtual environment is at the root of the project, simply select the recommended path ``./.env/bin/python``.

.. note::

   It can happen that vscode doesn't change interpreters. It seems to have worked to delete some of the existing python virtual environments in different projects. VSCode was then able to select the correct interpreter.