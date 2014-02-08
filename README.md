# cb's dotfiles
## Installation and setup

### Using Git and the bootstrap script

You can clone the repository wherever you want. (e.g. `~/dev/dotfiles`, with `~/dotfiles` as a symlink.)

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
