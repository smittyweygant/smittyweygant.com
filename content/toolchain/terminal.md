---
title: 'Terminal and zsh Configuration'
date: 2025-02-04T10:00:00+07:00
draft: false
description: 'Setup iTerm2 and configure zsh'
menus:
  toolchain:
---
Setup iTerm2 and configure zsh

## iTerm2

* Make iterm2 the default terminal application
  <!--more-->
* Preferences \-\>  
  * General \-\> Window  
    * unselect "Native full screen windows"  
    * select "close windows when closing an app"  
  * Appearance \-\>  
    * Windows  
      * select "Hide scrollbars"  
    * Tabs  
      * unselect "Show tab bar in fullscreen"  
    * Dimming  
      * Unselect all dimming  
  * Profiles \-\> Window  
    * Transparency: 15  
    * ~~Style: Full Screen~~  
    * ~~Screen: Main Screen~~  
  * Profiles \-\> Advanced  
    * Semantic History \-\> Open with editor ... \-\> VS Code  
  * [Open new split pane with current directory](https://apple.stackexchange.com/a/337386)  
  * [Natural Text Editing](https://apple.stackexchange.com/a/293988)  
* Bring it to fullscreen Command \+ Enters

## Zsh

Customize ZSH environment. I am using Oh My ZSH and Powerlevel10K. 

### Install [Oh My Zsh](https://ohmyz.sh/) 

Oh My zsh provides plugins, themes,etc. 

    sh \-c "$(curl \-fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"  

Update Oh My Zsh to the lastest version:  

    omz update  

Reload shell:  

    source \~/.zshrc   

### Oh My Zsh Theme \+ Fonts:

Use Powerlevel10K as the theme  

MesloLGS NF Font

Use the new font in iTerm2: Preferences \-\> Profile \-\> Text

### Configure ZSH

\# Standard plugins can be found in $ZSH/plugins/  
\# Custom plugins may be added to $ZSH\_CUSTOM/plugins/

\.zshrc

    # Enable Powerlevel10k instant prompt.
    # Code requiring console input must go above this block
    if [[ -r "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh" ]]; then
      source "${XDG_CACHE_HOME:-$HOME/.cache}/p10k-instant-prompt-${(%):-%n}.zsh"
    fi

    # Profile ZSH
    # zmodload zsh/zprof

    # Specify plugins
    plugins=(
      zsh-nvm
      git
      aws
      npm
      zsh-autocomplete
      zsh-autosuggestions
      zsh-syntax-highlighting
    )

    # Set environment variables
    export ZSH="$HOME/.oh-my-zsh"
    export NVM_LAZY_LOAD=true
    export NVM_COMPLETION=true
    export ZSH_THEME="powerlevel10k/powerlevel10k"

    source "$ZSH/oh-my-zsh.sh"

    # Enable pyenv
    export PYENV_ROOT="$HOME/.pyenv"
    [[ -d $PYENV_ROOT/bin ]] && export PATH="$PYENV_ROOT/bin:$PATH"
    eval "$(pyenv init - zsh)"

    # Profile ZSH
    # zprof

    # Load Powerlevel10k
    # To customize prompt, run `p10k configure` or edit ~/.p10k.zsh.
    [[ ! -f ~/.p10k.zsh ]] || source ~/.p10k.zsh

## Handy Aliases

\# get machine's ip address  

    alias ip="ipconfig getifaddr en0"

\# edit global zsh configuration  

    alias zshconfig="vim \~/.zshrc"

\# navigate to global ssh directory  

    alias sshhome="cd \~/.ssh"  
\# edit global ssh configuration  

    alias sshconfig="vim \~/.ssh/config"

\# edit global git configuration

    alias gitconfig="vim \~/.gitconfig"

\# git aliases  

    alias gits="git status"  
    alias gitd="git diff"  
    alias gitl="git lg"  
    alias gita="git add ."  
    alias gitc="cz commit"