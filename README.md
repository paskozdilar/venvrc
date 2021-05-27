# venvrc
(Probably) POSIX-compliant shell-based Python-venv convenience wrapper.

## Install

```bash
# copy venvrc to home
cp venvrc ~/.venvrc

# source venvrc on startup
echo ". ~/.venvrc" >> ~/.bashrc
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
