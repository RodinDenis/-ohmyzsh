# Моя конфигурация zsh

## Установка

Установка zsh как дефолтного shell

```sh
sudo apt update
sudo apt install zsh -y
chsh -s $(which zsh)
```

Установка ohmyzsh

```sh
sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
```

Установка Auto-Suggestions

```sh
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Установка Syntax Highlighting

```sh
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Скопируйте .zshrc в домашний каталог.

## Изменения в .zshrc

Применена тема. Альтернативные темы можно посмотреть [Oh My Zsh GitHub theme page.](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)

```sh
ZSH_THEME="af-magic"
```

Активированы плагины. Альтернативные плагины можно посмотреть здесь [Oh My Zsh GitHub plugins page.](https://github.com/ohmyzsh/ohmyzsh/wiki/Plugins)

```sh
plugins=(git zsh-autosuggestions zsh-syntax-highlighting colored-man-pages colorize)
```

Для локальной работы я предпочитаю nvim

```sh
if [[ -n $SSH_CONNECTION ]]; then
   export EDITOR='vim'
 else
   export EDITOR='mvim'
 fi
```


