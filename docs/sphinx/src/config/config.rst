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
