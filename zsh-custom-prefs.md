# ZSH Preferences

```bash
PROMPT="%B%K{#581c87}%F{#ffffff} %M %k%K{#6b21a8}%F{#581c87}%f %c %f%k%F{#6b21a8}%f%b "

bindkey  "^[[3~"  delete-char
bindkey "^[[1;5C" forward-word
bindkey "^[[1;5D" backward-word
bindkey '^H' backward-kill-word
bindkey '^[[3;5~' kill-word
bindkey "^[[A" history-beginning-search-backward
bindkey "^[[B" history-beginning-search-forward
```
