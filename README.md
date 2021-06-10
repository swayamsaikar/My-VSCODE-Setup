# My VSCode Settings and Extensions

## Settings

```javascript
{
    "editor.mouseWheelZoom": true,
    "files.autoSave": "afterDelay",
    "files.autoSaveDelay": 10,
    "editor.formatOnSave": true,
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "workbench.iconTheme": "material-icon-theme",
    "tabnine.experimentalAutoImports": true,
    "editor.suggestSelection": "first",
    "vsintellicode.modify.editor.suggestSelection": "automaticallyOverrodeDefaultValue",
    "liveshare.authenticationProvider": "GitHub",
    "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
    "synthwave84.brightness": 1,
    "terminal.integrated.rendererType": "dom",
    "editor.tabCompletion": "on",
    "editor.fontFamily": "Cascadia Code",
    "editor.fontLigatures": true,
    "cSpell.userWords": [
        "ellipsize"
    ],
    "editor.smoothScrolling": true,
    "workbench.editorAssociations": [
        {
            "viewType": "jupyter.notebook.ipynb",
            "filenamePattern": "*.ipynb"
        }
    ],
    "workbench.colorTheme": "Monokai",
    "screencastMode.fontSize": 25,
    "screencastMode.verticalOffset": 1,
    "screencastMode.mouseIndicatorSize": 30,
    "screencastMode.onlyKeyboardShortcuts": true,
    "window.zoomLevel": 1,
}
```

## Extensions

```ps1
$extensions = 
    "almenon.arepl"
    "akamud.vscode-theme-onedark"
    "formulahendry.auto-close-tag"
    "formulahendry.auto-rename-tag"
    "mgmcdermott.vscode-language-babel"
    "aaron-bond.better-comments"
    "coenraads.bracket-pair-colorizer"
    "wesbos.theme-cobalt2"
    "naumovs.color-highlight"
    "msjsdiag.debugger-for-chrome"
    "batisteo.vscode-django"
    "ms-azuretools.vscode-docker"
    "usernamehw.errorlens"
    "dsznajder.es7-react-js-snippets"
    "dbaeumer.vscode-eslint"
    "hasanakg.firebase-snippets"
    "evan-buss.font-switcher"
    "mhutchie.git-graph"
    "donjayamanne.githistory"
    "github.github-vscode-theme"
    "eamodio.gitlens"
    "wix.vscode-import-cost"
    "zignd.html-css-class-completion"
    "xabikos.javascriptsnippets"
    "wholroyd.jinja"
    "ms-toolsai.jupyter"
    "ritwickdey.liveserver"
    "ms-vsliveshare.vsliveshare"
    "ms-vsliveshare.vsliveshare-audio"
    "tyriar.lorem-ipsum"
    "magicstack.magicpython"
    "pkief.material-icon-theme"
    "monokai.theme-monokai-pro-vscode"
    "sdras.night-owl"
    "eg2.vscode-npm-script"
    "zhuangtongfa.material-theme"
    "christian-kohler.path-intellisense"
    "johnpapa.vscode-peacock"
    "webdevsimplified.pizza"
    "esbenp.prettier-vscode"
    "alefragnani.project-manager"
    "ms-python.vscode-pylance"
    "ms-python.python"
    "tht13.python"
    "kevinrose.vsc-python-indent"
    "frhtylcn.pythonsnippets"
    "himanoa.python-autopep8"
    "2gua.rainbow-brackets"
    "jundat95.react-native-snippet"
    "msjsdiag.vscode-react-native"
    "equimper.react-native-react-redux"
    "ms-vscode-remote.remote-ssh"
    "ms-vscode-remote.remote-ssh-edit"
    "ms-vscode-remote.remote-wsl"
    "humao.rest-client"
    "burkeholland.simple-react-snippets"
    "Tabnine.tabnine-vscode"
    "rangav.vscode-thunder-client"
    "wayou.vscode-todo-highlight"
    "visualstudioexptteam.vscodeintellicode"
    "vscode-icons-team.vscode-icons"
    "wakatime.vscode-wakatime"
    "johnpapa.winteriscoming"
    "streetsidesoftware.code-spell-checker"

$cmd = "code --list-extensions"
Invoke-Expression $cmd -OutVariable output | Out-Null
$installed = $output -split "\s"

foreach ($ext in $extensions) {
    if ($installed.Contains($ext)) {
        Write-Host $ext "already installed." -ForegroundColor Gray
    } else {
        Write-Host "Installing" $ext "..." -ForegroundColor White
        code --install-extension $ext
    }
}
```
## Steps To Install these extensions
## for all windows Users
1. Open Notepad and paste the above code
2. save that file with the name :- **cj-vscodeinstall.ps1** 
    (**Do not forget to write .ps1**)
3. double click that file and it will run

