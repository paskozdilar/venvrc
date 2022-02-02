# venvrc

Bash-based Python-venv convenience wrapper.


## Demo

![](https://github.com/paskozdilar/venvrc/blob/master/venvrc.gif)


## Install

Copy `venvrc` file to `~/.venvrc`, and add the following line to your
`~/.bashrc` file:

```bash
# source .venvrc on startup
. ~/.venvrc
```

Restart your shell and `venv` will be available as a command.


## Configuration

When creating virtual environments, `venvrc` scans for the `VENV_INSTALL`
environment variable - if it's set, all the packages specified in it, separated
by whitespace, are installed/upgraded on virtual environment creation.

For example, to upgrade `pip` and `wheel` packages on each venv creation, add
the following line to your `~/.bashrc`:

```bash
VENV_INSTALL="pip wheel"
```


## Usage

    venv c[reate] [ENVIRONMENT]
    venv r[emove] [ENVIRONMENT]
    venv a[ctivate] [ENVIRONMENT]
    venv d[eactivate]
    venv l[ist]

- If `[ENVIRONMENT]` is not specified, the current directory's name is taken as
environment name

- If `venv activate` is called for an environment that doesn't exist, it will be
automatically created


### NOTE

Since commands contain no common prefix, they can be specified through the
prefix, i.e. `venv c` is equivalent to `venv cre`, which is equivalent to
`venv create`
