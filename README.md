# nvim-setup

nvim lua configs

# To Setup

1. Clone repo:

```
gh repo clone EthanHofton/nvim-setup
```

2. copy nvim folder to ~/.config/nvim (nvim must be installed)

```
rm -rf ~/.config/nvim
cp -r nvim-setup/nvim ~/.config/nvim
```

3. open nvim

```
nvim
```

4. Install tmux

```
brew install tmux
```

5. copy .tmux.conf to ~/

```
cp nvim-conf/.tmux.conf ~/
```

6. Install tpm

```
git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
```

7. Start new tmux session

```
tmux new -s session
```

8. Source new tmux config

```
tmux source ~/.tmux.conf
```

8. b fix 127 error

add line before `run-shell` if getting `... returned 127` when trying to resource
```
set-environment -g PATH "/opt/homebrew/bin:/usr/local/bin:/bin:/usr/bin"
```

9. Install plugins

```
<C-R> I
```

# Terminal Setup:

1. Install Iterm2

```
brew install --cask iterm2
```

2. Install OhMyZSH

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

3. Install custom colors

```
curl https://raw.githubusercontent.com/josean-dev/dev-environment-files/main/coolnight.itermcolors --output ~/Downloads/coolnight.itermcolors
```

Then open Iterm2 Preferences>Profiles>Colors>Import and set new colors

4. Install Powerlevel10k

```
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

5. Edit .zshrc to use powerlevel10k

modify `ZSH_THEME`
```
ZSH_THEME="powerlevel10k/powerlevel10k"
```

6. resource

```
source ~/.zshrc
```

7. configure powerlevel10k

```
p10k configure
```

8. Install zsh plugins

```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

9. use plugins

modify `.zshrc` plugins line (use `/plugins` to find in vim)
```
plugins=(git zsh-autosuggestions zsh-syntax-highlighting web-search)
```

10. resource

```
source ~/.zshrc
```

# Refs

[https://www.josean.com/posts/terminal-setup](terminal setup blog post)
[https://www.youtube.com/watch?v=CF1tMjvHDRA](terminal setup youtube turorial)

[https://github.com/josean-dev/dev-environment-files](nvim setup code repo)
[https://www.youtube.com/watch?v=vdn_pKJUda8](nvim setup youtube turotial)

[https://www.josean.com/posts/tmux-setup](tmux setup blog post)
[https://www.youtube.com/watch?v=U-omALWIBos](tmux setup youtube tutorial)
