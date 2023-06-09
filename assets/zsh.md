# Zsh & Starship in Windows Git Bash

## Install Zsh

1. Download MSYS2 zsh package, it's named like [zsh-5.9-2-x86_64.pkg.tar.zst](https://mirror.msys2.org/msys/x86_64/zsh-5.9-2-x86_64.pkg.tar.zst). [MSYS2 package repository](https://packages.msys2.org/package/zsh?repo=msys&variant=x86_64) is here.
2. PeaZip or 7-Zip Beta to open ZST extension's file.
3. Extract zsh compression into Git Bash installation directory. `C:\Program Files\Git` is usually path. Windows may prompt if merge contents, select yes.
4. Open Git Bash, run `zsh` to confirm zsh has been installed correctly.
5. To set up Zsh as the default shell, edit `~/.bashrc` file:

   ```bash
   if [ -t 1 ]; then
     exec zsh
   fi

   ```

## Install oh-my-zsh

In the Zsh shell and run:

```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

```

## Install Plugins

In the Zsh shell and run:

```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-completions ${ZSH_CUSTOM:-${ZSH:-~/.oh-my-zsh}/custom}/plugins/zsh-completions
git clone https://github.com/zdharma-continuum/fast-syntax-highlighting.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/plugins/fast-syntax-highlighting

```

## Install Starship

In the Zsh shell and run:

```bash
curl -sS https://starship.rs/install.sh | sh -s -- --bin-dir ~/.config/starship

```

Edit `~/.zshrc` file:

```plaintext
eval "$(starship init zsh)"
```

Restart zsh and enjoy it.

## Recommand Starship Presets

Select an [Presets](https://starship.rs/presets/) to custom Starship.

## Reference

[Installing Zsh (and oh-my-zsh) in Windows Git Bash](https://dominikrys.com/posts/zsh-in-git-bash-on-windows/)

[linux-like-windows-terminal](https://github.com/Kyza/linux-like-windows-terminal)
