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

    venv create [ENVIRONMENT]
    venv remove [ENVIRONMENT]
    venv activate [ENVIRONMENT]
    venv deactivate
    venv list

- If `[ENVIRONMENT]` is not specified, the current directory's name is taken as
environment name

- If `venv activate` is called for an environment that doesn't exist, it will be
automatically created
