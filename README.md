# dotfiles
...

## vim

1. See `vim/.vimrc`
      - Sources
          - https://www.freecodecamp.org/news/vimrc-configuration-guide-customize-your-vim-editor
          - https://www.dunebook.com/best-vim-plugins/

## zsh

1. Installed oh-my-zsh
      - `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
2. Installed powerline10k
      - Downloaded MesloLGS fonts in `zsh/fonts`
        - Install is platform specific (double click + Terminal settings)
      -  `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k`
      -  Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`
      -  `source ~/.zshrc`
      -  (Optional) `p10k configure`
3. Added following key bindings in `~/.zshrc` (after `oh-my-zsh.sh` is sourced, in user config area)
      - ```
        bindkey -v  # vi mode
        bindkey '^I^I' autosuggest-accept
        bindkey -M vicmd '/' history-incremental-pattern-search-backward
        ``` 
4. Added the following plugins (add plugin name to array of plugins in `~/.zshrc`):
      - zsh-autosuggestions
          - `git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions`
      - zsh-syntax-higlighting
          - `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting`
5. Added battery icon in the first line in `~/.p10k.zsh`