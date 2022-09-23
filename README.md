# Summary

This repository contains instructions and files for setting up a new dev machine with my preferences. Right now it assumes a dev machine with Windows 10 or 11.

## Step 1: Get this repository

### Install Winget

Download from winget [releases](https://github.com/microsoft/winget-cli/releases).

### Install git

```
winget install --id Git.Git -e --source winget
```

### Set up private key for github

See [here](https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) for an example.

1. Generate a key: `ssh-keygen`
2. List keys: `ssh-add -l`
3. Delete a key: `ssh-add -D`
4. Add the key: `ssh-add ~/.ssh/id_rsa`
5. Start the agent:

```
eval `ssh-agent -s`
```

Copy the contents of the .pub file to the server key field.

### Clone this repository

```
git clone git@github.com:keith-anders/setup.git
```

## Step 2: Set up terminal

### Install Windows Terminal

```
winget install "Windows Terminal" -s winget
```

### Download Fonts

Download cool fonts from [nerdfonts](https://www.nerdfonts.com/font-downloads).

In particular, [Cascadia Code](https://github.com/microsoft/cascadia-code/releases/tag/v2111.01).

Also get FiraCode and Caskaydia Cove.

Install the OTF rather than the ttf if possible.

Change the Windows Terminal default profile font to be a PowerLine-compatible font.

### Terminal Niceties

In powershell, run:

```powershell
winget install JanDeDobbeleer.OhMyPosh -s winget
Install-Module posh-git -Scope CurrentUser
notepad $profile
```

Let notepad create the powershell profile if it does not exist. Replace its contents with this:

```
Install-Module posh-git -Scope CurrentUser
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\aliens.omp.json" | Invoke-Expression
```

You may need to `Set-ExecutionPolicy Unrestricted`

## Step 3: Install IDE(s)

### Visual Studio Code

```
winget install "Microsoft Visual Studio Code" -s winget
```

### Visual Studio Pro

### Python

## Step 4: Organize Taskbar

1. Visual Studio
2. Windows Explorer
3. Browser (Firefox or Edge)
4. VS Code
5. Windows Terminal
6. Note-taking software (Notion or OneNote)
7. Chatting software (Discord or Teams)
8. Outlook

Others: RDC, ILSpy, 


## Others

- Docker
- AutoHotKey
- DebugDiag
- Dia
- Fiddler
- NSSM
- nvm
- OpenSSL-Win64
- Pencil
- ProcExp
- Windirstat
- Sysinternals
- Python
- nuget.exe
- Notepad++
- Windbg
- Putty and Puttygen
- 7zip
- grepwin
- BeyondCompare
- paint.net
- postman
- HxD
- Sizer
- HashTab
- 