# Powershell-Setup

- [oh-my-posh](https://ohmyposh.dev/)

- Terminal

- Powershell

- Use acrylic material in the tab row (requires relaunch)

- One Half Dark (modded) - `"background": "#001B26"`

- Hack Nerd Font [Download](https://github.com/ryanoasis/nerd-fonts/releases/download/v2.1.0/Hack.zip)

```
Set-ExecutionPolicy RemoteSigned
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser

notepad $PROFILE

Import-Module posh-git
Import-Module oh-my-posh
Set-PoshPrompt -Theme sorin

"terminal.integrated.fontFamily": "'Hack NF'",
"terminal.integrated.shellArgs.windows": "-nologo"
```

```
oh-my-posh init pwsh | Invoke-Expression

& ([ScriptBlock]::Create((oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\atomic.omp.json" --print) -join "`n"))

Import-Module -Name Terminal-Icons
Import-Module -Name PSReadLine

Set-PSReadLineOption -PredictionSource History
# Set-PSReadLineOption -PredictionViewStyle ListView
Set-PSReadLineOption -EditMode Windows
```
