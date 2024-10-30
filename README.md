# Useful Python Environment Aliases

Here are a few helpful BASH terminal aliases to make working with Python virtual environments much easier.

Try adding these simple aliases to your bash `.profile`.
They all assume the use of a folder named `.venvs` in your home directory to store the virtual environments in.


## USE
- `show-envs`       -- Shows a list of available environments
- `open-env NAME`   -- Opens the given environment
- `close-env`       -- Closed the currently open environment
- `make-env NAME`   -- Makes a new environment with the given name


## ALIASES TO ADD
```
alias show-envs="ls -al ~/.venvs"
```

```
open-env(){
    source ~/.venvs/"$1"/bin/activate
}
```

```
alias close-env="deactivate"
```

```
make-env(){
    python3 -m venv ~/.venvs/"$1"
}
```
