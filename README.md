# WyPosh


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

```powershell
Install-Module posh-git -Scope CurrentUser
Install-Module oh-my-posh -Scope CurrentUser
```

### Windows Terminal
Update settings to use the nerd font.

```json
"profiles": {
        "defaults": {
            "startingDirectory": "d:\\repos",
            "font": {
                "face": "MesloLGM Nerd Font",
                "size": 10
            }
        },
}
```

```powershell
notepad $PROFILE
```

Contents:
```
$themePath = "https://raw.githubusercontent.com/jwyckoff/WyPosh/be5ecafe11bc82f5351a8df97979159fe6808699/wyckoff.json"
oh-my-posh init pwsh --config $themePath | Invoke-Expression
```
