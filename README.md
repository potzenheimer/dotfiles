# cb's dotfiles
## Installation and setup

In order to use this dotfiles no special steps are needed. Just copy&paste all
data, configuration or files to the corresponding places on your machine.

In order to make the most out of a general dotfile repository it is recommended
to actually use the provided files by either setting up the whole dotfile dir
or by symlinking or copying the desired parts.

You can clone the repository wherever you want. (e.g. `~/dev/dotfiles`, with `~/dotfiles` as a symlink.)

Then copy the config files to your home directory, e.g.

```bash
scp ~/dotfiles/.bash_profile ~/.bash_profile
scp ~/dotfiles/.bash_prompt ~/.bash_prompt
```

The `.bash_prompt` file automatically loads the following config files, so make
sure you have at least empty versions in your home directory:

- bash_prompt (color console prompt)
- exports (set environment defaults like e.g. default editor)
- aliases (handy shortcuts like e.g `flush` to purge local DNS Cache)
- functions (tools for easier development like e.g. `server` opens a Python Server with the current directory as root for testing static sites)


### Using Git and the bootstrap script (experimantal)

The bootstrapper script will pull in the latest version and copy the files to your home folder.

```bash
git clone https://github.com/potzenheimer/dotfiles.git && cd dotfiles && source bootstrap.sh
```

To update, `cd` into your local `dotfiles` repository and then:

```bash
source bootstrap.sh
```

Alternatively, to update while avoiding the confirmation prompt:

```bash
set -- -f; source bootstrap.sh
```
