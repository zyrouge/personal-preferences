# git-bash

## `~/.inputrc`

```bash
set bell-style none

# key bindings
"\e[A": history-search-backward
"\e[B": history-search-forward
```

## `~/.bashrc`

```bash
PROMPT_COMMAND='history -a'
PROMPT_COMMAND=${PROMPT_COMMAND:+"$PROMPT_COMMAND; "}'printf "\e]9;9;%s\e\\" "`cygpath -w "$PWD" -C ANSI`"'

# prompt
COLOR_VIOLET_LIGHT='167;139;250'
COLOR_VIOLET_LIGHTER='196;181;253'
COLOR_VIOLET_LIGHTEST='221;214;254'
COLOR_RESET='\[\033[0m\]'
FG_COLOR_VIOLET_LIGHT="\[\033[38;2;${COLOR_VIOLET_LIGHT}m\]"
FG_COLOR_VIOLET_LIGHTER="\[\033[38;2;${COLOR_VIOLET_LIGHTER}m\]"
FG_COLOR_VIOLET_LIGHTEST="\[\033[38;2;${COLOR_VIOLET_LIGHTEST}m\]"
PS1='\[\033]0;$MSYSTEM:${PWD/#$HOME/\~}\007\]\n' # set window title
PS1="${PS1}${FG_COLOR_VIOLET_LIGHT}"'\u@\h'
PS1="${PS1}${FG_COLOR_VIOLET_LIGHTER}"' \w'
PS1="${PS1}${FG_COLOR_VIOLET_LIGHTEST}"' $'
PS1="${PS1}${COLOR_RESET}"' '

# aliases
# alias code='code-insiders'

# others
export HIST_CONTROL='ignoreboth:erasedups'
```
