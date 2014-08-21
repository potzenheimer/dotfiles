# cb's dotfiles
## Installation and setup

In order to use this dotfiles no special steps are needed. Just copy&paste all
data, configuration or files to the corresponding places on your machine.

In order to make the most out of a general dotfile repository it is recommended
to actually use the provided files by either setting up the whole dotfile dir
or by symlinking or copying the desired parts.

```bash
cd ~/path/to/safe/checkout/location
git clone git@github.com:potzenheimer/dotfiles.git
ln -s ~//path/to/safe/checkout/location ~/dotfiles
```

You can clone the repository wherever you want (e.g. `~/dev/dotfiles`, with `~/dotfiles` as a symlink).

Then copy the config files to your home directory, e.g.

```bash
scp ~/dotfiles/.bash_profile ~/.bash_profile
scp ~/dotfiles/.bash_prompt ~/.bash_prompt
```

### Setup

The `.bash_prompt` file automatically loads the following config files, so make
sure you have at least empty versions in your home directory:

- bash_prompt (color console prompt)
- exports (set environment defaults like e.g. default editor)
- aliases (handy shortcuts like e.g `flush` to purge local DNS Cache)
- functions (tools for easier development like e.g. `server` opens a Python Server with the current directory as root for testing static sites)

### Git command promt enhancements

We provide an installation file for git completion setup (not installed by
default when using brew git installations). In order to enable it, you must run

```bash
(sudo) ~/install-git-completion.sh
```

### Extra paths and user specific information

You can add extra paths by editing the `.path` file.

*Note:* you _must_ edit `.extra` to configure your user specific information (
like e.g. github user). Otherwise several services might not work as expected.


## Using Git and the bootstrap script (experimantal)

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
