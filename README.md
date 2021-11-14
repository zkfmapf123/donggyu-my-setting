# 환경 구축하기

## 1. oh my zsh 설치 및 세팅

https://medium.com/harrythegreat/oh-my-zsh-iterm2%EB%A1%9C-%ED%84%B0%EB%AF%B8%EB%84%90%EC%9D%84-%EB%8D%94-%EA%B0%95%EB%A0%A5%ED%95%98%EA%B2%8C-a105f2c01bec

## 2. vsCode 터미널 path 설정하기

```
    명령 팔레트 -> shell -> code path
```

## 3. utility 설치

### visual stuiod code

```
    https://code.visualstudio.com/
```

### homebrew

```
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

    brew install cask

    brew update
```

### git

```
    brew install git
```

### nodejs

```
    brew install node@14
```

### git configuration

```
    - git config

    git config --global -user.email ~~~
    git config --global -user.name ~~~

    - git log alias 설정
     
    git config --global alias.hist "log --graph --all --pretty=format:'%C(yellow)[%ad]%C(reset) %C(green)[%h]%C(reset) | %C(white)%s %C(bold red){{%an}}%C(reset) %C(blue)%d%C(reset)' --date=short"

    - git config global -e

    [user]
	    name = zkfmapf123
	    email = 47292546+zkfmapf123@users.noreply.github.com
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