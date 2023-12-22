# Language Setting

## NVM Setting (brew, zsh 설치가 된 후)

```sh
    brew install nvm

    mkdir ~/.nvm

    sudo vi ~/.zshrc
    ## nvm setting
    export NVM_DIR=~/.nvm ## added
    source $(brew --prefix nvm)/nvm.sh ## added

    nvm ls
    nvm install 18 # 왠만하면 18 ~ 20 설치 (2023.12.22)
```

## Golang

```
    brew install go
```

## Git

```
    brew install git
```

- global git config
```sh
    ## git config

    git config --global -user.email ~~~
    git config --global -user.name ~~~

    ## git log alias 설정
     
    git config --global alias.hist "log --graph --all --pretty=format:'%C(yellow)[%ad]%C(reset) %C(green)[%h]%C(reset) | %C(white)%s %C(bold red){{%an}}%C(reset) %C(blue)%d%C(reset)' --date=short"

    ## git config global -e

    [user]
	    name = ""
	    email = ""
    [core]
	    precomposeunicode = true
	    quotepath = false
	    editor = code --wait
	    editor = code --wait
	    autocrlf = input
    [diff] (add)
	    tool = vscode
    [difftool "vscode"] (add)
	    cmd = code --wait --diff $LOCAL $REMOTE
    [filter "lfs"]
	    required = true
	    clean = git-lfs clean -- %f
	    smudge = git-lfs smudge -- %f
	    process = git-lfs filter-process
    [merge] (add)
	    tool = vscode
    [mergetool "vscode"] (add)
	    cmd = code --wait $MERGED
    [alias]
	    st = status
	    hist = log --graph --all --pretty=format:'%C(yellow)[%ad]%C(reset) %C(green)[%h]%C(reset) | %C(white)%s %C(bold red){{%an}}%C(reset) %C(blue)%d%C(reset)' --date=short
```