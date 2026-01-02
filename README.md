# iterm2-oh-my-zsh-powerlevel10k
Setup new mac / terminal 

## brew

```bash
mkdir ~/.homebrew
curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C ~/.homebrew
echo 'export PATH="$HOME/homebrew/bin:$PATH"' >> ~/.zshrc
brew --version
```

## iterm2

```bash
brew reinstall iterm2
```

## powerlevel10k

[install fonts](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#fonts) and reconfigure iterm2 accordingly

```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/.powerlevel10k
echo 'source ~/.powerlevel10k/powerlevel10k.zsh-theme' >> ~/.zshrc
```

## oh-my-zsh

[install oh-my-zsh](https://ohmyz.sh/#install) and then install powerlevel10k theme

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"

vi ~/.zshrc # and replace ZSH_THEME="robbyrussell" with ZSH_THEME="powerlevel10k/powerlevel10k"

source ~/.zshrc # and follow powerlevel10k steps...
```
