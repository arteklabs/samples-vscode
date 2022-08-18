extensio: `tomsaunders.vscode-workspace-explorer`  

create folder ``vscode-workspaces`` with files `*.code-workspace` with contents:

```json
{
        "folders": [
                {
                        "name": "org",
                        "path": "../src/lifespline-org"
                },
        ]
}
```

Add to `settings.json`:

```json
"workspaceExplorer.workspaceStorageDirectory": "vscode-workspaces"
```