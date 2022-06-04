# Shell Color Scripts

![Screenshot of shell-color-scripts](https://raw.githubusercontent.com/sethigeet/shell-color-scripts/master/screenshots/01.png)

Based on [shell-color-scripts](https://github.com/sethigeet/shell-color-scripts), only with the set of scripts I prefer. Intended to keep my bin directory clean and not clogged with color scripts by managing those scripts here.   


## Installing shell-color-scripts on Arch Linux

Included is a PKGBUILD that will generate the package, which you can build and install with:

```sh
makepkg -si
```

## Installing shell-color-scripts on other Linux distrtibutions

Download the source code from this repository or use a git clone:

    git clone https://github.com/Thomashighbaugh/colorscripts
    cd colorscripts 
    rm -rf /opt/shell-color-scripts || return 1
    sudo mkdir -p /opt/shell-color-scripts/colorscripts || return 1
    sudo cp -rf colorscripts/* /opt/shell-color-scripts/colorscripts
    sudo cp colorscript.sh /usr/bin/colorscript

    # optional for zsh completion
    sudo cp zsh_completion/_colorscript /usr/share/zsh/site-functions

## Usage

```
colorscript --help
Description: A collection of terminal color scripts.

Usage: colorscript [OPTION] [SCRIPT NAME/INDEX]
  -h, --help, help    	Print this help.
  -l, --list, list    	List all color scripts.
  -r, --random, random	Run a random color script.
  -e, --exec, exec    	Run a spesific color script by SCRIPT NAME or INDEX.
```

## The Scripts Are Located in /opt/shell-color-scripts/colorscripts

The source for shell-color-scripts is placed in:

```sh
/opt/shell-color-scripts/colorscripts
```

To display a random color script each time an interactive terminal opens, enter the following commands, which will append first a label and then the appropriate command to either you `.zshrc`` or `.bashrc``

```sh
# for ZSH
echo "### RANDOM COLOR SCRIPT ###" >> ~/.zshrc 
echo "colorscript random" >> ~/.zshrc 

# for BASH 
echo "### RANDOM COLOR SCRIPT ###" >> ~/.bashrc 
echo "colorscript random" >> ~/.bashrc 
```
