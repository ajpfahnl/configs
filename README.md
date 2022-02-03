# configs
Config options for various programs
## .vimrc
```
syntax on

set wrap
set autoindent
  
set tabstop=4
set shiftwidth=4
set softtabstop=4
"" set expandtab
```
## .gitignore
```
.DS_Store
```
## .ssh/config
```
Host pi
    HostName 192.168.1.96
    User pi

Host beagle
    HostName 192.168.7.2
    User root

Host rhel8
    HostName 127.0.0.1
    User ajp
    Port 2200
```
## git and oh-my-zsh
Disable tracking with oh-my-zsh to speed things up. Add `--global` option to apply to all repos.
```
git config --add oh-my-zsh.hide-status 1
git config --add oh-my-zsh.hide-dirty 1
```

## VSCode `settings.json`
```json
{
    "latex-workshop.view.pdf.viewer": "tab",
    "window.zoomLevel": 0,
    "latex-workshop.latex.recipes":[
      {
        "name": "latexmk 🔃",
        "tools": [
          "latexmk"
        ]
      },
      {
        "name": "pdflatex ➞ bibtex ➞ pdflatex × 2",
        "tools": [
          "pdflatex",
          "bibtex",
          "pdflatex",
          "pdflatex"
        ]
      },
      {
        "name": "lualatex",
        "tools": [
          "lualatex"
        ]
      },
      {
        "name": "lualatex->biber->lualatex",
        "tools": [
          "lualatex",
          "biber",
          "lualatex"
        ]
      },
      {
        "name": "Compile Rnw files",
        "tools": [
          "rnw2tex",
          "latexmk"
        ]
      },
      {
        "name": "Compile Jnw files",
        "tools": [
          "jnw2tex",
          "latexmk"
        ]
      },
      {
        "name": "tectonic",
        "tools": [
          "tectonic"
        ]
      }
    ],
    "latex-workshop.latex.tools": [
      {
        "name": "latexmk",
        "command": "latexmk",
        "args": [
          "-synctex=1",
          "-interaction=nonstopmode",
          "-file-line-error",
          "--shell-escape",
          "-pdf",
          "%DOC%"
        ]
      },
      {
        "name": "lualatex",
        "command": "lualatex",
        "args": [
          "--synctex=1",
          "--interaction=nonstopmode",
          "--file-line-error",
          "--pdf",
          "%DOC%"
        ]
      },
      {
        "name": "pdflatex",
        "command": "pdflatex",
        "args": [
          "--shell-escape",
          "-synctex=1",
          "-interaction=nonstopmode",
          "-file-line-error",
          "%DOC%"
        ]
      },
      {
        "name": "bibtex",
        "command": "bibtex",
        "args": [
          "%DOCFILE%"
        ],
        "env": {}
      },
      {
        "name": "biber",
        "command": "biber",
        "args": [
          "%DOCFILE%"
        ]
      }
    ],
    "workbench.editorAssociations": {
      "*.ipynb": "jupyter-notebook"
    },
    "workbench.activityBar.visible": true,
    "workbench.colorTheme": "Monokai",
    "terminal.integrated.inheritEnv": false,
    "editor.suggestSelection": "first",
    "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
    "files.exclude": {
      "**/.classpath": true,
      "**/.project": true,
      "**/.settings": true,
      "**/.factorypath": true
    },
    "terminal.integrated.tabs.enabled": true,
    "python.pythonPath": "/usr/local/bin/python3",
    "notebook.cellToolbarLocation": {
      "default": "right",
      "jupyter-notebook": "left"
    },
    "python.defaultInterpreterPath": "/usr/local/bin/python3",
    "omnisharp.path": "latest",
    "omnisharp.useGlobalMono": "always"
}
```
