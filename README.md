# WyPosh<!-- omit in toc -->

* [Install on Linux](#install-on-linux)
* [Install on Windows](#install-on-windows)
  * [1. Install Oh My Posh](#1-install-oh-my-posh)
  * [2. Install fonts on computer](#2-install-fonts-on-computer)
  * [3. Update Windows Terminal](#3-update-windows-terminal)
  * [4. Update $PROFILE](#4-update-profile)

## Install on Linux

```bash
sudo apt install curl
sudo apt install unzip
sudo curl -s https://ohmyposh.dev/install.sh | sudo bash -s

```

Add this to `~/.bashrc`
```bash
eval "$(oh-my-posh init bash --config https://raw.githubusercontent.com/jwyckoff/WyPosh/main/wyckoff.json)"
```

or
```bash
echo 'eval "$(oh-my-posh init bash --config https://raw.githubusercontent.com/jwyckoff/WyPosh/main/wy-linux.json)"' >> ~/.bashrc
. ~/.bashrc

```


## Install on Windows


### 1. Install Oh My Posh


```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

### 2. Install fonts on computer

### 3. Update Windows Terminal

Update settings to use the nerd font.

```json
"profiles": {
        "defaults": {
            "startingDirectory": "d:\\repos",
            // add this font section 
            "font": {
                "face": "MesloLGM Nerd Font",
                "size": 10
            }
        },
}
```
### 4. Update $PROFILE

```powershell
notepad $PROFILE
```

Contents:
```
$themePath = "https://raw.githubusercontent.com/jwyckoff/WyPosh/be5ecafe11bc82f5351a8df97979159fe6808699/wyckoff.json"
oh-my-posh init pwsh --config $themePath | Invoke-Expression
```
