#####Python Version Management
```bash
~ » brew update
~ » brew install pyenv

~ » pyenv install 2.7.10
~ » pyenv install 3.6.5

~ » pyenv versions                                                                                        z048659@9801a79ac68f
  system
  2.7.10
* 3.6.5 (set by /Users/xxxxxx/.pyenv/version)
```

##### Python Virtual Environment
```bash
~ » brew install pyenv-virtualenv
```

Modify ~/.zshrc. Add
```bash
eval "$(pyenv init -)"
eval "$(pyenv virtualenv-init -)"
```

```bash
~ » exec "$SHELL"
```

Add Virtual Environment
```bash
~ » pyenv virtualenv 3.6.5 myenv1
~ » pyenv versions                                                                                        z048659@9801a79ac68f
  system
* 2.7.10 (set by /Users/xxxxxx/.pyenv/version)
* 3.6.5 (set by /Users/xxxxxx/.pyenv/version)
  3.6.5/envs/myenv1
  myenv1
```
Use Virtual Environment
```bash
~ » pyenv activate myenv1
pyenv-virtualenv: prompt changing will be removed from future release. configure `export PYENV_VIRTUALENV_DISABLE_PROMPT=1' to simulate the behavior.
(myenv1) ------------------------------------------------------------
```

Delete a Virtual Environment
```bash
~ » pyenv uninstall myenv1
```
